# AI Context - BlueprintJSONExporter

Questo documento e la memoria rapida per future sessioni AI. Descrive solo lo stato attuale del codice in `BJE21Clean`.

## Scopo

BlueprintJSONExporter e un plugin Unreal Editor per UE 5.4. Esporta asset supportati in file testuali leggibili da strumenti AI, GitHub e Obsidian, senza modificare asset di gioco.

Asset supportati dal codice:

| Asset | Stato |
|---|---|
| `UBlueprint` | supportato |
| Widget Blueprint | supportato come `UBlueprint`, con dati UMG specifici solo parziali |
| Actor Blueprint | supportato come `UBlueprint` |
| Component Blueprint | supportato come `UBlueprint` |
| Animation Blueprint | supportato come `UBlueprint` |
| `UDataTable` | supportato |
| `UUserDefinedStruct` | supportato |
| `UUserDefinedEnum` | supportato |

## Filosofia

- Editor-only.
- Export sola lettura.
- Nessun salvataggio o modifica di `.uasset`.
- Output testuale UTF-8.
- Workflow Git opzionale.
- AI Context e indici generati da dati statici.

## File principali

| File | Ruolo |
|---|---|
| `Private/BlueprintJSONExporter.cpp` | orchestrazione export, menu editor, export asset base, test automation |
| `Private/AIReadableBlueprintPackExporter.cpp` | genera `BlueprintExports/` con indici, jsonl, summary, graph e flow |
| `Private/AIContextExporter.cpp` | genera cartella `AI_Context/` |
| `Private/GitExportWorkflow.cpp` | change report, semantic diff, git add/commit/push |
| `Private/SemanticSummaryBuilder.cpp` | summary semantico per asset |
| `Private/AssetSystemClassifier.cpp` | classificazione asset per sistema |
| `Public/BlueprintJSONExporterSettings.h` | settings editor/config |
| `Private/ExportModels.h` | modelli condivisi |

## Workflow breve

Content Browser selection o folder selection

↓

`ExecuteExport`

↓

`ExportAssetsToSavedJson` oppure `ExportAssetsToObsidianVault`

↓

`ExportAsset`

↓

`ExportBlueprint`, `ExportDataTable`, `ExportUserStruct`, `ExportUserEnum`

↓

`SaveJsonObject`, `FAIContextExporter::Generate`, `FAIReadableBlueprintPackExporter::Generate`

↓

`FinalizePostExport`

↓

opzionale `FGitExportWorkflow::Run`

## Dove scrive

Stato aggiornato 2026-07-10:

- export canonico AI: `<OutputDirectory>/Exported_Files_forAI/`;
- documentazione nel repository AI: `<GitRepositoryPath>/Plugin_Documentation/`;
- export nel repository AI: `<GitRepositoryPath>/Exported_Files_forAI/`;
- cache e report locali: `<OutputDirectory>/AI_Context/` e `<OutputDirectory>/.AIExportCache/`;
- JSON legacy in root: disabilitati di default (`bIncludeLegacyRootJson=false`) e non cancellati automaticamente.

Default:

```text
<ProjectSavedDir>/BlueprintAIExports/
```

Se `OutputDirectory` e configurato:

```text
<OutputDirectory>/
```

Il pack AI-readable viene scritto sempre in:

```text
<RootDirectory>/BlueprintExports/
```

Obsidian viene scritto in:

```text
<VaultDirectory>/Unreal Blueprint Export/
```

## Output principali

Il workflow Git pubblica solo le due cartelle gestite `Plugin_Documentation` e `Exported_Files_forAI`. Non usa piu' `git add -A` sulla root del repository.


| Output | Generatore |
|---|---|
| JSON completo pretty per asset | `SaveJsonObject` in `BlueprintJSONExporter.cpp` |
| `manifest.json` | `MakeManifest` |
| `AI_Context/*` | `FAIContextExporter` |
| `BlueprintExports/*` | `FAIReadableBlueprintPackExporter` |
| Markdown Obsidian | `MakeMarkdown`, `MakeIndex` |
| `.canvas` | `MakeBlueprintCanvas` |
| Git report/diff/summary | `GitExportWorkflow.cpp` |

## Naming

Aggiornamento 2026-07-10:

- I nomi salvati nei contenuti JSON (`assetName`, `eventName`, `graphName`, titoli nodo) restano originali.
- Solo i componenti usati nel filesystem passano da `FFilenameSanitizer::MakeSafeComponent`.
- Newline, carriage return, tab, caratteri di controllo e caratteri Windows non validi vengono trasformati in `_`.
- Esempio flow: `UpdatePrompt\nCustom_Event` + `F8E3B2BE` diventa `UpdatePrompt_Custom_Event__F8E3B2BE__FLOW.txt`.

- JSON completo classico: `MakeExportFilename`.
- Asset key AI-readable: path Unreal normalizzato in `MakeAssetKey`.
- Graph key: `MakeGraphKey`.
- Flow: `<EntryName>__<ShortGuid>__FLOW.txt/json`.

## Punti critici

- `FAIReadableBlueprintPackExporter` cancella `RootDirectory/BlueprintExports` prima di rigenerarlo.
- L'export classico non cancella la root, quindi file vecchi possono restare fuori da `BlueprintExports`.
- Widget tree designer reale non viene letto da API UMG dedicate: il file widget tree e inferito dai nodi.
- Componenti, funzioni ed eventi nel pack AI-readable sono in parte inferiti dai nodi.
- I flow includono tutti i nodi del graph, non un traversal exec completo.
- `memberName`, `functionName`, `variableName`, `targetClass` sono campi presenti ma valorizzati a stringa vuota nell'export base.

## Errori comuni da evitare

- Non usare copie dentro progetti Unreal come fonte primaria del codice.
- Non assumere che `BlueprintExportsRepo` sia sempre la root export: il codice usa `OutputDirectory`, poi aggiunge `BlueprintExports`.
- Non rimuovere export classico: il pack AI-readable e affiancato.
- Non fare `git push` dal plugin se Git non e configurato.
- Non modificare asset Unreal: il plugin e sola lettura.
