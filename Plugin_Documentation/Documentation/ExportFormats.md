# Export Formats

## JSON completo per asset

| Campo | Valore |
|---|---|
| Formato | JSON pretty |
| Percorso JSON export | `<OutputDirectory>/<AssetFilename>.json` |
| Percorso Obsidian | `<Vault>/Unreal Blueprint Export/JSON/<Category>/<AssetFilename>.json` |
| Generatore | `ExportAsset` + `SaveJsonObject` |

Campi comuni:

```text
schemaVersion
unrealEngineVersion
name
path
assetName
assetPath
assetKey
generatedAt
assetType
unrealClass
dependencies
relations
semanticSummary
```

## Blueprint JSON

Campi specifici:

```text
mainClass
parentClass
compileStatus
implementedInterfaces
variables[]
graphs[]
```

Ogni graph:

```text
name
type
nodes[]
links[]
```

Ogni node:

```text
nodeGuid
class
title
comment
x
y
memberName
functionName
variableName
targetClass
pins[]
```

Ogni pin:

```text
pinId
name
direction
type
defaultValue
```

Ogni link:

```text
fromNodeGuid
fromPinId
fromPinName
toNodeGuid
toPinId
toPinName
```

## DataTable JSON

Campi:

```text
rowStruct
columns[]
rowCount
rows[]
```

Ogni row contiene:

```text
name
data
fields[]
```

## Struct JSON

Campi:

```text
status
guid
sizeBytes
fields[]
```

## Enum JSON

Campi:

```text
values[]
```

Ogni value:

```text
index
value
name
authoredName
displayName
hidden
```

## Manifest

`EXPORT_MANIFEST.json` nel pacchetto canonico `Exported_Files_forAI` contiene:

- `schemaVersion`
- `pluginVersion`
- `unrealEngineVersion`
- `generatedAt`
- `complete`
- conteggi asset/file/grafi/nodi/edge/split
- `errors`

Il campo `complete` viene usato da `FAIExportPackageValidator` per bloccare la pubblicazione quando `bRequireCompleteExportBeforePublish=true`.

## JSONL canonici

I file `.jsonl` del pacchetto AI sono validati riga per riga. Ogni riga non vuota deve essere un oggetto JSON valido.


| Campo | Valore |
|---|---|
| File | `manifest.json` oppure `JSON/manifest.json` in Obsidian |
| Formato | JSON pretty |
| Generatore | `MakeManifest` |

Contiene:

```text
schemaVersion
unrealEngineVersion
outputDirectory
assetsExported
assetsWithErrors
assets[]
aiContext
```

## AI Context

| File | Formato | Generatore |
|---|---|---|
| `AI_Context/AI_Context.md` | Markdown | `FAIContextExporter` |
| `AI_Context/AI_Instructions.md` | Markdown | `FAIContextExporter` |
| `AI_Context/AssetIndex.md` | Markdown | `FAIContextExporter` |
| `AI_Context/BlueprintSummaries.md` | Markdown | `FAIContextExporter` |
| `AI_Context/ChangeReport.md` | Markdown | `FChangeReportWriter` |
| `AI_Context/CompileStatus.md` | Markdown | `FAIContextExporter` |
| `AI_Context/DataModel.md` | Markdown | `FAIContextExporter` |
| `AI_Context/DependencyMap.md` | Markdown | `FAIContextExporter` |
| `AI_Context/ExportSummary.md` | Markdown | `FExportSummaryWriter` |
| `AI_Context/LargeGraphs.md` | Markdown | `FAIContextExporter` |
| `AI_Context/ProjectOverview.md` | Markdown | `FAIContextExporter` |
| `AI_Context/SemanticDiff.json` | JSON pretty | `FSemanticDiffBuilder` |
| `AI_Context/SemanticSummary.json` | JSON pretty | `FAIContextExporter` |
| `AI_Context/SystemMap.md` | Markdown | `FAIContextExporter` |

## BlueprintExports

Root:

```text
<RootDirectory>/BlueprintExports/
```

Global:

| File | Tipo |
|---|---|
| `GLOBAL_INDEX.json` | JSON index |
| `GLOBAL_SEARCH.jsonl` | JSONL search |
| `GLOBAL_SYMBOL_INDEX.jsonl` | JSONL symbol index |
| `GLOBAL_ASSET_INDEX.md` | Markdown index |

Per asset:

| File | Tipo |
|---|---|
| `<AssetKey>__FULL.pretty.json` | JSON pretty completo |
| `<AssetKey>__INDEX.json` | JSON index |
| `<AssetKey>__SUMMARY.md` | Markdown |
| `<AssetKey>__VARIABLES.json` | JSON |
| `<AssetKey>__COMPONENTS.json` | JSON parziale/inferito |
| `<AssetKey>__WIDGET_TREE.json` | JSON parziale/inferito |
| `<AssetKey>__FUNCTIONS.json` | JSON parziale/inferito |
| `<AssetKey>__EVENTS.json` | JSON parziale/inferito |
| `<AssetKey>__NODES.jsonl` | JSONL |
| `<AssetKey>__EDGES.jsonl` | JSONL |
| `<AssetKey>__SEARCH.jsonl` | JSONL |

Per graph:

```text
graphs/<GraphName>__INDEX.json
graphs/<GraphName>__SUMMARY.md
graphs/<GraphName>__NODES.jsonl
graphs/<GraphName>__EDGES.jsonl
```

Per flow:

```text
flows/<GraphName>/<EntryName>__<ShortGuid>__FLOW.txt
flows/<GraphName>/<EntryName>__<ShortGuid>__FLOW.json
```

## Canvas

| Campo | Valore |
|---|---|
| File | `Canvas/<Asset>.canvas` |
| Formato | JSON canvas |
| Generatore | `MakeBlueprintCanvas` |
| Stato | completato ma semplice |
