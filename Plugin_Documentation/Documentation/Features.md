# Features

## Pipeline AI canonica

Aggiornamento 2026-07-10:

- genera `Exported_Files_forAI` come pacchetto principale;
- include asset Blueprint, DataTable, Struct ed Enum;
- crea manifest, status, indici globali e file per asset con nomi stabili;
- valida JSON/JSONL prima della pubblicazione se `bValidateBeforePublish=true`;
- sincronizza nel repository Git solo `Plugin_Documentation` e `Exported_Files_forAI`;
- usa `git add -A -- "Plugin_Documentation" "Exported_Files_forAI"` invece di `git add -A` sulla root;
- conserva il BAT come fallback, senza dipendenza operativa primaria.

## Filename sicuri per output AI-readable

Aggiornamento 2026-07-10:

- `FFilenameSanitizer` centralizza la generazione dei componenti filename.
- Gestisce newline, tab, caratteri di controllo, caratteri Windows vietati, nomi vuoti e nomi riservati.
- Mantiene GUID breve nei Flow per distinguere entry con stesso nome.
- Non modifica i nomi originali memorizzati nei JSON o nei testi dei Flow.


| Funzionalita | Stato | Classe/funzione responsabile | Note |
|---|---|---|---|
| Export Blueprint JSON | completata | `ExportBlueprint` | Include graph, nodes, pins, links, variables, dependencies |
| Export DataTable JSON | completata | `ExportDataTable` | Include columns, row struct, rows |
| Export User Defined Struct | completata | `ExportUserStruct` | Include fields, status, guid, size |
| Export User Defined Enum | completata | `ExportUserEnum` | Include values, display names, hidden |
| Pretty JSON | completata | `SaveJsonObject` | Usa `TPrettyJsonPrintPolicy` |
| Manifest | completata | `MakeManifest` | Include stats, paths, errors, AI context section |
| AI Context | completata | `FAIContextExporter` | Produce Markdown e JSON semantico |
| Semantic summary per asset | completata | `FSemanticSummaryBuilder` | Attacca `semanticSummary` al JSON |
| Obsidian export | completata | `ExportAssetsToObsidianVault` | Crea vault `Unreal Blueprint Export` |
| Canvas Obsidian | completata | `MakeBlueprintCanvas` | Canvas JSON con nodi e link |
| Git add/commit/push | completata | `FGitExportWorkflow` | Condizionato da settings/azione menu |
| Change report | completata | `FChangeReportWriter` | Markdown |
| Semantic diff | completata | `FSemanticDiffBuilder` | JSON diff se baseline presente |
| Export summary | completata | `FExportSummaryWriter` | Markdown |
| Test Git | completata | `FGitExportWorkflow::TestGit` | Mostra stato repo/git |
| Menu Content Browser asset | completata | `RegisterMenus` | Asset context |
| Menu Content Browser folder | completata | `RegisterMenus` | Folder context |
| Output `BlueprintExports` | completata | `FAIReadableBlueprintPackExporter` | Cartella rigenerata da zero |
| GLOBAL_SEARCH JSONL | completata | `FAIReadableBlueprintPackExporter` | Basato su variabili e nodi |
| GLOBAL_SYMBOL_INDEX JSONL | completata | `FAIReadableBlueprintPackExporter` | Basato su variabili e nodi |
| Flow txt/json | parziale | `FlowText`, `FlowJson` | Include tutti i nodi del graph, non traversal exec completo |
| Graph split JSONL | parziale | `SaveJsonLinesMaybeSplit` | Split generico per file oltre limite |
| Widget tree designer | parziale | `AIReadableBlueprintPackExporter` | Inferito da nomi/nodi, non da UMG designer tree |
| Component export dettagliato | parziale | `AIReadableBlueprintPackExporter` | Inferito da nodi, non da SCS completo |
| Function/event index | parziale | `AIReadableBlueprintPackExporter` | Inferito da graph/nodi |
| `memberName/functionName/variableName` accurati | parziale | `ExportBlueprint` | Campi creati ma vuoti nel JSON base |
| Custom details panel | non implementata | nessuna | Non presente nel codice |
| Commandlet dedicato | non implementata | nessuna | Non presente nel codice |
| Toolbar dedicata | non implementata | nessuna | Solo menu Content Browser |
