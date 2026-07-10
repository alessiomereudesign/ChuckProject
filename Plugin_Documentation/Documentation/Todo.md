# Todo

Questa checklist deriva dai limiti osservati nel codice. Non e una richiesta di modifica corrente.

## Alta priorita

- Verificare manualmente in Unreal Editor il flusso completo `Esporta e pubblica repository AI` su un repository di prova con remote/upstream configurati.
- Aggiungere, in una modifica futura separata, una azione di pulizia legacy con dry-run e doppia conferma prima di cancellare JSON in root.

| Punto | Classe/file | Difficolta |
|---|---|---|
| Popolare `memberName`, `functionName`, `variableName`, `targetClass` da nodi K2 specifici | `ExportBlueprint` | media |
| Implementare traversal exec reale per flow | `FAIReadableBlueprintPackExporter` | alta |
| Estrarre data dependency nodes in modo corretto | `FAIReadableBlueprintPackExporter` | alta |
| Estrarre widget tree UMG reale | `FAIReadableBlueprintPackExporter` o exporter dedicato | alta |
| Estrarre component hierarchy/SCS reale | nuovo exporter componenti | alta |

## Media priorita

- Estendere il validatore con controlli di coerenza sui riferimenti interni tra indici globali, asset index e file grafi.


| Punto | Classe/file | Difficolta |
|---|---|---|
| Separare exporter per asset type da `BlueprintJSONExporter.cpp` | architettura | media |
| Creare writer utility condiviso | nuovo file writer | bassa |
| Aggiungere schema version separato per pack AI-readable | `ExportModels.h`/pack | bassa |
| Rendere configurabile pulizia `BlueprintExports` | settings + pack | media |
| Migliorare deduplica funzioni/eventi inferiti | pack | media |

## Bassa priorita

| Punto | Classe/file | Difficolta |
|---|---|---|
| Uniformare lingua messaggi UI/docs | vari | bassa |
| Aggiungere documentazione inline mirata | vari | bassa |
| Esporre summary pack in dialog finale | `ShowSummary` | bassa |
| Aggiungere commandlet dedicato | nuovo commandlet | media |
| Aggiungere custom details panel | settings UI | media |
