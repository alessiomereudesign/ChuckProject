# Outputs

## Root JSON export

Percorso:

```text
GetOutputDirectory()
```

Regola:

```text
se OutputDirectory e vuoto:
  FPaths::ProjectSavedDir() / "BlueprintAIExports"
altrimenti:
  OutputDirectory normalizzato
```

Contenuto:

```text
<Asset>.json
manifest.json
AI_Context/
BlueprintExports/
.AIExportCache/
```

Chi crea:

- `ExportAssetsToSavedJson`
- `FAIContextExporter`
- `FAIReadableBlueprintPackExporter`
- `FGitExportWorkflow`

Pulizia:

- la root non viene pulita.
- `BlueprintExports/` viene cancellata e rigenerata.
- `.AIExportCache/` viene aggiornata.

## Obsidian export

Percorso:

```text
<VaultDirectory>/Unreal Blueprint Export/
```

Cartelle create:

```text
Blueprints/
DataTables/
Structs/
Enums/
JSON/Blueprints/
JSON/DataTables/
JSON/Structs/
JSON/Enums/
Canvas/
AI_Context/
BlueprintExports/
```

Pulizia:

- la root Obsidian non viene pulita.
- `BlueprintExports/` viene cancellata e rigenerata.

## Exported_Files_forAI

Stato aggiornato 2026-07-10: il pacchetto canonico per l'uso AI viene generato in:

`<OutputDirectory>/Exported_Files_forAI/`

Struttura principale:

- `README.md`
- `EXPORT_MANIFEST.json`
- `EXPORT_STATUS.md`
- `GLOBAL_INDEX.json`
- `GLOBAL_SEARCH.jsonl`
- `GLOBAL_SYMBOL_INDEX.jsonl`
- `GLOBAL_ASSET_INDEX.md`
- `Assets/Blueprints/<AssetKey>/`
- `Assets/DataTables/<AssetKey>/`
- `Assets/Structs/<AssetKey>/`
- `Assets/Enums/<AssetKey>/`

Per ogni asset il pacchetto usa nomi stabili come `FULL.pretty.json`, `INDEX.json`, `SUMMARY.md`, `SEARCH.jsonl`, `NODES.jsonl`, `EDGES.jsonl`.

I componenti di filename generati dal plugin sono sanitizzati con `FFilenameSanitizer`: i nomi originali restano nei contenuti JSON, ma i path su disco non contengono newline, tab, caratteri di controllo o caratteri non validi su Windows.

## BlueprintExports

`BlueprintExports` e' il nome storico del pacchetto AI-readable. Non e' piu' il percorso canonico della pipeline corrente.

Percorso reale:

```text
<RootDirectory>/BlueprintExports/
```

Chi la crea:

```text
FAIReadableBlueprintPackExporter::Generate
```

Quando:

- dopo JSON classico.
- dopo Obsidian.
- solo per input Blueprint esportati con successo.

Pulizia:

```text
IFileManager::Get().DeleteDirectory(*PackRoot, false, true)
```

Quindi viene pulita solo questa cartella.

## Gestione overwrite

| Area | Comportamento |
|---|---|
| JSON classico | sovrascrive file con stesso nome |
| Manifest | sovrascrive |
| AI_Context | sovrascrive file noti |
| BlueprintExports | cancella cartella e rigenera |
| Obsidian Markdown | sovrascrive file con stesso nome |
| Canvas | sovrascrive file con stesso nome |
| `.AIExportCache` | aggiorna baseline |

## File obsoleti

I JSON legacy nella root di `OutputDirectory` sono disabilitati di default tramite `bIncludeLegacyRootJson=false`. Se presenti da esportazioni precedenti vengono solo rilevati e segnalati: non vengono cancellati automaticamente.


- In `BlueprintExports` non dovrebbero restare file obsoleti, perche la cartella viene cancellata.
- Nella root JSON classica possono restare file di export vecchi se asset non viene piu esportato.
- In Obsidian possono restare note/canvas vecchi fuori da `BlueprintExports`.

## Manifest

Il manifest descrive export corrente, ma non elimina automaticamente file vecchi fuori da `BlueprintExports`.
