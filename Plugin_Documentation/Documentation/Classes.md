# Classes

## Inventario

| Nome | Tipo | File | Responsabilita |
|---|---|---|---|
| `BlueprintJSONExporter` | `ModuleRules` | `BlueprintJSONExporter.Build.cs` | dipendenze build |
| `FBlueprintJSONExporterModule` | module class | `Public/BlueprintJSONExporter.h`, `Private/BlueprintJSONExporter.cpp` | lifecycle modulo e menu |
| `UBlueprintJSONExporterSettings` | `UDeveloperSettings` | `Public/BlueprintJSONExporterSettings.h` | settings editor/config |
| `FRelMaps` | struct locale | `AIContextExporter.cpp` | mappe relazioni AI context |
| `FAIContextExporter` | class | `AIContextExporter.h/.cpp` | generazione AI Context |
| `FReadableBlueprintInput` | struct | `AIReadableBlueprintPackExporter.h` | input pack AI-readable |
| `FReadableBlueprintPackResult` | struct | `AIReadableBlueprintPackExporter.h` | risultato pack AI-readable |
| `FAIReadableBlueprintPackExporter` | class | `AIReadableBlueprintPackExporter.h/.cpp` | generazione `Exported_Files_forAI` |
| `FAIExportPackageValidator` | class | `AIExportPackageValidator.h/.cpp` | validazione pacchetto AI canonico |
| `FAssetSystemClassifier` | class | `AssetSystemClassifier.h/.cpp` | classificazione sistema asset |
| `EGitExportAction` | enum class | `ExportModels.h` | azione Git richiesta |
| `FAssetRelation` | struct | `ExportModels.h` | relazione asset |
| `FExportStats` | struct | `ExportModels.h` | statistiche export |
| `FSemanticGraph` | struct | `ExportModels.h` | summary graph |
| `FSemanticAssetRecord` | struct | `ExportModels.h` | record semantico asset |
| `FAIContextResult` | struct | `ExportModels.h` | risultato AI context |
| `FGitCommandResult` | struct | `GitExportWorkflow.h` | output comando git |
| `FGitWorkflowResult` | struct | `GitExportWorkflow.h` | output workflow git |
| `FExportPostProcessInput` | struct | `GitExportWorkflow.h` | input post-process |
| `FExportPostProcessResult` | struct | `GitExportWorkflow.h` | risultato post-process |
| `FGitCommandRunner` | class | `GitExportWorkflow.h/.cpp` | esecuzione comandi Git |
| `FExportChangeTracker` | class | `GitExportWorkflow.h/.cpp` | baseline e file attesi |
| `FSemanticDiffBuilder` | class | `GitExportWorkflow.h/.cpp` | diff semantico |
| `FChangeReportWriter` | class | `GitExportWorkflow.h/.cpp` | report Markdown |
| `FExportSummaryWriter` | class | `GitExportWorkflow.h/.cpp` | summary Markdown |
| `FGitExportWorkflow` | class | `GitExportWorkflow.h/.cpp` | orchestrazione Git |
| `FSemanticSummaryBuilder` | class | `SemanticSummaryBuilder.h/.cpp` | costruzione semantic summary |

## Metodi principali

### `FBlueprintJSONExporterModule`

Pubblici:

- `StartupModule`
- `ShutdownModule`
- `RegisterMenus`

Privati/statici collegati nel `.cpp`:

- `ExecuteExport`
- `ExportAssetsToSavedJson`
- `ExportAssetsToObsidianVault`
- `ChooseOutputDirectory`
- `TestGitConfiguration`

### `FAIContextExporter`

Pubblici:

- `Generate`
- `AddManifestSection`

Responsabilita:

- scrive file `AI_Context`
- produce `SemanticSummary.json`
- registra errori e file generati

### `FAIReadableBlueprintPackExporter`

Pubblico:

- `Generate`

Helper interni importanti:

- `MakeAssetKey`
- `MakeGraphKey`
- `SaveJsonLinesMaybeSplit`
- `CloneNodeForJsonl`
- `MakeSearchEntry`
- `MakeSymbolEntry`
- `FlowText`
- `FlowJson`

Responsabilita:

- pulisce `Exported_Files_forAI`
- genera indici globali
- genera file per asset/graph/flow
- produce JSONL e pretty JSON
- include Blueprint, DataTable, Struct ed Enum nel pacchetto canonico

### `FAIExportPackageValidator`

Pubblico:

- `Validate`

Responsabilita:

- verifica `EXPORT_MANIFEST.json`, `EXPORT_STATUS.md`, `GLOBAL_INDEX.json`, `GLOBAL_SEARCH.jsonl`
- valida JSON e JSONL
- segnala `complete=false` quando la pubblicazione richiede un export completo

### `FGitExportWorkflow`

Pubblici:

- `Run`
- `TestGit`

Classi di supporto:

- `FGitCommandRunner::Run`
- `FExportChangeTracker::EnsureGitIgnore`
- `FSemanticDiffBuilder::Build`
- `FChangeReportWriter::BuildMarkdown`
- `FExportSummaryWriter::BuildMarkdown`

Responsabilita aggiornata:

- sincronizza solo `Plugin_Documentation` e `Exported_Files_forAI`
- non modifica `.git`, root README, `.gitignore`, `LICENSE` o altri file root del repository
- usa pathspec Git limitati alle cartelle gestite

### `UBlueprintJSONExporterSettings`

Metodi:

- costruttore con default
- `GetCategoryName`
- `GetSectionText`

Campi:

- `OutputDirectory`
- `DocumentationSourceDirectory`
- impostazioni Git
- impostazioni AI Context
- impostazioni validazione/pubblicazione AI
