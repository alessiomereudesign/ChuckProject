# Workflow

## Entry point UI

Azioni aggiornate 2026-07-10:

- `Imposta cartella export...`: salva `OutputDirectory`.
- `Imposta cartella Documentation...`: salva `DocumentationSourceDirectory`.
- `Imposta repository Git...`: salva `GitRepositoryPath`.
- `Esporta file per AI`: genera il pacchetto canonico `Exported_Files_forAI`.
- `Verifica pacchetto AI`: esegue `FAIExportPackageValidator` senza sync e senza Git.
- `Test configurazione Git`: controlla `git`, repository e configurazione base.
- `Pubblica repository AI`: pubblica il pacchetto gia' generato.
- `Esporta e pubblica repository AI`: esporta, valida, sincronizza e poi esegue commit/push se richiesto.

Il plugin registra menu nel Content Browser tramite:

```text
FBlueprintJSONExporterModule::StartupModule
  ↓
UToolMenus::RegisterStartupCallback
  ↓
FBlueprintJSONExporterModule::RegisterMenus
```

Voci create:

| Menu | Azione |
|---|---|
| Esporta asset per IA (JSON) | export JSON + AI context + pack AI-readable |
| Export + Commit | export + commit Git se configurato |
| Export + Commit + Push | export + commit + push |
| Test Git | verifica git/repo configurato |
| Esporta asset per Obsidian | export in root Obsidian |
| Imposta cartella di esportazione | salva `OutputDirectory` |

## Raccolta asset

Asset singoli:

```text
AssetsFromAssetContext
  ↓
AddUniqueSupportedAsset
```

Cartelle:

```text
AssetsFromFolderContext
  ↓
GetSupportedAssetsInPaths
  ↓
AddUniqueSupportedAsset
```

Filtro supportato:

```text
UBlueprint
UDataTable
UUserDefinedStruct
UUserDefinedEnum
```

## Export JSON normale

La pipeline normale genera il pacchetto canonico in `<OutputDirectory>/Exported_Files_forAI/`. I JSON legacy nella root vengono scritti solo se `bIncludeLegacyRootJson=true`.

Prima della pubblicazione Git, il workflow:

1. valida `Exported_Files_forAI`;
2. copia `DocumentationSourceDirectory` in `<GitRepositoryPath>/Plugin_Documentation/`;
3. copia `<OutputDirectory>/Exported_Files_forAI/` in `<GitRepositoryPath>/Exported_Files_forAI/`;
4. esegue `git status`, `git add`, `git commit` e `git push` solo sulle cartelle gestite.


```text
ExecuteExport(..., bObsidian=false)
  ↓
ExportAssetsToSavedJson
  ↓
GetOutputDirectory
  ↓
per ogni asset:
    ExportAsset
    FSemanticSummaryBuilder::BuildAndAttach
    SaveJsonObject
  ↓
FAIContextExporter::Generate
  ↓
MakeManifest
  ↓
FAIContextExporter::AddManifestSection
  ↓
FAIReadableBlueprintPackExporter::Generate
  ↓
FinalizePostExport
  ↓
ShowSummary
```

## Export Obsidian

```text
ExecuteExport(..., bObsidian=true)
  ↓
ExportAssetsToObsidianVault
  ↓
RootDirectory = VaultDirectory / "Unreal Blueprint Export"
  ↓
crea cartelle Blueprints, DataTables, Structs, Enums, JSON, Canvas
  ↓
per ogni asset:
    ExportAsset
    FSemanticSummaryBuilder::BuildAndAttach
    SaveJsonObject in JSON/<Category>
    MakeBlueprintCanvas per Blueprint
    MakeMarkdown
  ↓
AI_Context
  ↓
manifest in JSON/manifest.json
  ↓
Index.md
  ↓
BlueprintExports
  ↓
Git workflow opzionale
```

## Export asset

```text
ExportAsset
  ├─ UBlueprint -> ExportBlueprint
  ├─ UDataTable -> ExportDataTable
  ├─ UUserDefinedStruct -> ExportUserStruct
  └─ UUserDefinedEnum -> ExportUserEnum
```

## Blueprint

```text
ExportBlueprint
  ↓
FillCommonAssetFields
  ↓
parent class, generated class, compile status, interfaces
  ↓
NewVariables
  ↓
GetAllGraphs
  ↓
nodes, pins, links
  ↓
FillDependenciesAndRelations
```

Il codice salva `nodeGuid`, `pinId`, pin direction, pin type, default value e link deduplicati.

## DataTable

```text
ExportDataTable
  ↓
FillCommonAssetFields
  ↓
rowStruct
  ↓
columns da ExportStructFields
  ↓
rows con data strutturata e valueText
  ↓
dependencies/relations
```

## Struct

```text
ExportUserStruct
  ↓
status, guid, sizeBytes
  ↓
fields con type/default/metadata
```

## Enum

```text
ExportUserEnum
  ↓
values con index, value, name, authoredName, displayName, hidden
```

## AI Context

```text
FAIContextExporter::Generate
  ↓
ProjectOverview.md
AssetIndex.md
DependencyMap.md
SystemMap.md
BlueprintSummaries.md
DataModel.md
LargeGraphs.md
CompileStatus.md
AI_Instructions.md
AI_Context.md
SemanticSummary.json
```

## AI-readable pack

```text
FAIReadableBlueprintPackExporter::Generate
  ↓
DeleteDirectory(<Root>/BlueprintExports)
  ↓
GLOBAL_INDEX / SEARCH / SYMBOL_INDEX / ASSET_INDEX
  ↓
assets/<AssetKey>/*
  ↓
graphs/*
  ↓
flows/*
```

Il pack viene rigenerato pulendo prima solo `BlueprintExports`.

## Git workflow

```text
FinalizePostExport
  ↓
FGitExportWorkflow::Run
  ↓
EnsureGitIgnore
  ↓
SemanticDiff / ChangeReport / ExportSummary
  ↓
git add/commit/push secondo settings o azione menu
```
