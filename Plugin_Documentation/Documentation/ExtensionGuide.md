# Extension Guide

Questa sezione spiega dove intervenire se in futuro si vuole estendere il plugin. Non descrive funzionalita gia implementate se non come punto di aggancio.

## Aggiungere un nuovo asset type

File da modificare:

```text
Private/BlueprintJSONExporter.cpp
Private/ExportModels.h se servono nuovi campi stats
Private/SemanticSummaryBuilder.cpp se serve summary
Private/AIContextExporter.cpp se serve AI context dedicato
```

Punti:

1. aggiungere classe al `FARFilter` in `GetSupportedAssetsInPaths`.
2. aggiornare `GetSupportedAssetType`.
3. aggiornare `CategoryForType`.
4. creare `ExportNewAssetType`.
5. aggiungere branch in `ExportAsset`.
6. aggiornare manifest e AI context se necessario.

## Aggiungere un nuovo formato output

Se parte dal JSON gia prodotto:

```text
creare nuova classe exporter in Private/
chiamarla da ExportAssetsToSavedJson e/o ExportAssetsToObsidianVault
```

Pattern esistente:

```text
FAIReadableBlueprintPackExporter::Generate(RootDirectory, Inputs)
```

## Aggiungere un nuovo indice

Punto consigliato:

```text
AIReadableBlueprintPackExporter.cpp
```

Motivo: quel file gia aggrega asset, graph, nodes, edges, search e symbols.

## Aggiungere un nuovo writer

Punti:

- `SaveString`
- `SaveJsonObject`
- helper locali `SaveJsonFile`, `SaveJsonLinesMaybeSplit`

Regola attuale:

- JSON completo: pretty.
- JSONL: un JSON compatto per riga.
- Markdown: stringhe UTF-8.

## Aggiungere nuova configurazione

File:

```text
Public/BlueprintJSONExporterSettings.h
```

Poi leggere il valore dove serve:

```text
GetDefault<UBlueprintJSONExporterSettings>()
GetMutableDefault<UBlueprintJSONExporterSettings>()
```

Se modifica via UI:

```text
Settings->SaveConfig()
```

## Aggiungere nuovo menu o pulsante

File:

```text
Private/BlueprintJSONExporter.cpp
```

Funzione:

```text
FBlueprintJSONExporterModule::RegisterMenus
```

Pattern:

```text
FToolMenuEntry::InitMenuEntry
FToolUIActionChoice
FToolMenuExecuteAction::CreateLambda
```

## Aggiungere workflow Git

Regole correnti:

- usare sempre `GitRepositoryPath` come repository di pubblicazione;
- sincronizzare solo cartelle gestite (`Plugin_Documentation`, `Exported_Files_forAI`);
- non usare `git add .` o `git add -A` sulla root;
- non modificare `.git`, root README, `.gitignore`, `LICENSE` o file root estranei;
- validare `Exported_Files_forAI` prima della pubblicazione quando `bValidateBeforePublish=true`.


File:

```text
Private/GitExportWorkflow.cpp
Private/GitExportWorkflow.h
```

Tenere separati:

- command execution in `FGitCommandRunner`
- stato/report in `FGitExportWorkflow`
- report Markdown in writer dedicati.
