# Generated Changelog

Storico tecnico ricostruito dal codice, senza Git.

## Fase 1 - Export JSON base

Componenti:

- modulo editor `BlueprintJSONExporter`
- menu Content Browser
- export JSON per Blueprint
- export DataTable
- export User Defined Struct
- export User Defined Enum
- manifest

Caratteristiche:

- asset discovery tramite AssetRegistry.
- output in `Saved/BlueprintAIExports` se non configurato.

## Fase 2 - Obsidian

Componenti:

- `ExportAssetsToObsidianVault`
- `MakeMarkdown`
- `MakeIndex`
- `MakeBlueprintCanvas`

Output:

- `Unreal Blueprint Export/`
- note Markdown per asset
- JSON categorizzati
- canvas per Blueprint

## Fase 3 - AI Context e semantica

Componenti:

- `FSemanticSummaryBuilder`
- `FAIContextExporter`
- `FAssetSystemClassifier`

Output:

- `AI_Context`
- `SemanticSummary.json`
- Markdown di overview, asset index, dependency map, system map, compile status.

## Fase 4 - Git workflow

Componenti:

- `FGitCommandRunner`
- `FExportChangeTracker`
- `FSemanticDiffBuilder`
- `FChangeReportWriter`
- `FExportSummaryWriter`
- `FGitExportWorkflow`

Funzionalita:

- `.gitignore`
- baseline cache
- semantic diff
- change report
- export summary
- add/commit/push opzionale

## Fase 5 - AI-readable Blueprint pack

Componenti:

- `FAIReadableBlueprintPackExporter`
- `FReadableBlueprintInput`
- `FReadableBlueprintPackResult`

Output:

- `BlueprintExports/GLOBAL_INDEX.json`
- `GLOBAL_SEARCH.jsonl`
- `GLOBAL_SYMBOL_INDEX.jsonl`
- `GLOBAL_ASSET_INDEX.md`
- asset folders
- graph folders
- flow txt/json
- JSONL nodes/edges/search

Stato:

- implementato e integrato nel workflow.
- alcuni dati sono euristici/parziali.

## Componenti incompleti o parziali

- widget tree reale UMG.
- component hierarchy reale.
- flow traversal exec.
- campi K2 specializzati (`memberName`, `functionName`, `variableName`).

## Componenti deprecati

Nessun componente marcato come deprecato nel codice.

