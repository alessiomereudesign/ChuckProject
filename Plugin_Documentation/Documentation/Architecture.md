# Architecture

## Modulo

Il plugin contiene un solo modulo Unreal:

```text
BlueprintJSONExporter
```

Tipo modulo: `Editor`.

Loading phase: `Default`.

Dipendenze da `BlueprintJSONExporter.Build.cs`:

```text
AssetRegistry
BlueprintGraph
ContentBrowser
Core
CoreUObject
DesktopPlatform
DeveloperSettings
Engine
Json
JsonUtilities
Slate
SlateCore
ToolMenus
UnrealEd
```

Non risultano librerie esterne custom.

## Cartelle

```text
BJE21Clean/
  BlueprintJSONExporter.uplugin
  Source/BlueprintJSONExporter/
    BlueprintJSONExporter.Build.cs
    Public/
      BlueprintJSONExporter.h
      BlueprintJSONExporterSettings.h
    Private/
      BlueprintJSONExporter.cpp
      ExportModels.h
      AIContextExporter.*
      AIReadableBlueprintPackExporter.*
      AssetSystemClassifier.*
      GitExportWorkflow.*
      SemanticSummaryBuilder.*
```

## Diagramma generale

```text
Content Browser
  ↓
FBlueprintJSONExporterModule::RegisterMenus
  ↓
ExecuteExport
  ↓
ExportAssetsToSavedJson / ExportAssetsToObsidianVault
  ↓
ExportAsset
  ↓
ExportBlueprint / ExportDataTable / ExportUserStruct / ExportUserEnum
  ↓
SaveJsonObject / FAIContextExporter / FAIReadableBlueprintPackExporter
  ↓
Files
  ↓
FinalizePostExport
  ↓
FGitExportWorkflow
```

## Classi e responsabilita

Aggiornamento 2026-07-10:

- `FAIReadableBlueprintPackExporter`: genera il pacchetto canonico `Exported_Files_forAI` con asset Blueprint, DataTable, Struct ed Enum.
- `FAIExportPackageValidator`: valida presenza e leggibilita' di manifest, status, JSON e JSONL prima della pubblicazione.
- `FGitExportWorkflow`: sincronizza solo `Plugin_Documentation` e `Exported_Files_forAI` nel repository Git configurato e usa pathspec Git limitati.
- `UBlueprintJSONExporterSettings`: espone sorgente Documentation, validazione, legacy root JSON, Obsidian opzionale e fallback BAT.


| Classe/struct | Responsabilita | Dipendenze | Usata da |
|---|---|---|---|
| `BlueprintJSONExporter` | ModuleRules Build.cs | UnrealBuildTool | build UE |
| `FBlueprintJSONExporterModule` | startup/shutdown e menu editor | `UToolMenus`, Slate | Unreal module system |
| `UBlueprintJSONExporterSettings` | settings editor/config | `UDeveloperSettings` | exporter e Git workflow |
| `FExportStats` | statistiche asset export | `FAssetRelation` | manifest, AI context, Git report |
| `FSemanticAssetRecord` | record semantico per AI context | `FExportStats`, `FSemanticGraph` | `FAIContextExporter`, diff |
| `FAIContextResult` | risultato AI context | stringhe path/errori | manifest |
| `FAIContextExporter` | genera `AI_Context` | record semantici | export principale |
| `FAIReadableBlueprintPackExporter` | genera `BlueprintExports` | JSON asset, stats | export principale |
| `FReadableBlueprintInput` | input pack AI-readable | `FExportStats`, `FJsonObject` | pack exporter |
| `FReadableBlueprintPackResult` | metriche pack AI-readable | array errori | export principale |
| `FAssetSystemClassifier` | classifica asset in sistema probabile | asset path, classi | semantic summary |
| `FSemanticSummaryBuilder` | crea summary semantico asset | JSON asset, stats | export principale |
| `FGitCommandRunner` | esegue comandi git | `FPlatformProcess` | workflow Git e test |
| `FExportChangeTracker` | `.gitignore`, baseline manifest/summary | file system, JSON | workflow Git |
| `FSemanticDiffBuilder` | semantic diff tra baseline e corrente | semantic summary | workflow Git |
| `FChangeReportWriter` | Markdown change report | stats/diff | workflow Git |
| `FExportSummaryWriter` | Markdown summary export | stats/Git | workflow Git |
| `FGitExportWorkflow` | orchestrazione post-export Git | settings, command runner | `FinalizePostExport` |

## Relazioni

```text
BlueprintJSONExporter.cpp
  ├─ usa ExportModels.h
  ├─ chiama FSemanticSummaryBuilder
  ├─ chiama FAIContextExporter
  ├─ chiama FAIReadableBlueprintPackExporter
  └─ chiama FGitExportWorkflow

GitExportWorkflow.cpp
  ├─ usa UBlueprintJSONExporterSettings
  ├─ usa FExportStats / FSemanticAssetRecord
  └─ scrive AI_Context extra e usa git

AIReadableBlueprintPackExporter.cpp
  ├─ legge JSON gia prodotto da ExportBlueprint
  ├─ non legge asset Unreal direttamente
  └─ scrive output piccoli in BlueprintExports
```

## API Unreal usate

| Area | API |
|---|---|
| Asset discovery | `AssetRegistry`, `FARFilter`, `FAssetData` |
| Blueprint graph | `UBlueprint`, `UEdGraph`, `UEdGraphNode`, `UEdGraphPin`, `UK2Node_Event`, `UK2Node_CustomEvent`, `UK2Node_FunctionEntry` |
| Data assets | `UDataTable`, `UUserDefinedStruct`, `UUserDefinedEnum` |
| JSON | `FJsonObject`, `FJsonSerializer`, `TJsonWriterFactory`, `TPrettyJsonPrintPolicy`, `TCondensedJsonPrintPolicy` |
| File system | `FFileHelper`, `IFileManager`, `FPaths` |
| UI editor | `UToolMenus`, `FToolMenuEntry`, `FMessageDialog`, `FScopedSlowTask`, `FDesktopPlatformModule` |
| Settings | `UDeveloperSettings`, `EditorPerProjectUserSettings` |
| Automation | `IMPLEMENT_SIMPLE_AUTOMATION_TEST` |
