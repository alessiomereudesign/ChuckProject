# Known Issues

## TODO/FIXME/HACK/TEMP

Ricerca stretta nel codice:

```text
0 occorrenze
```

## Limitazioni reali

- Risolto 2026-07-10: i Flow AI-readable potevano fallire su Windows se il titolo entry point conteneva newline, tab o caratteri non validi. La correzione generale e' `FFilenameSanitizer`.

- La rimozione dei JSON legacy dalla root non e' automatica: la pipeline li rileva e segnala, ma non li cancella.
- La pubblicazione Git richiede `GitRepositoryPath` configurato e separato dall'output sorgente; il fallback implicito su `OutputDirectory` non e' piu' usato per pubblicare.
- `Pubblica repository AI` puo' eseguire push reale dall'Editor quando l'utente lo avvia e Git e' configurato; Codex non deve eseguire questo push durante lo sviluppo.
- Obsidian resta output opzionale e disabilitato di default nella pipeline canonica.


| Problema | Area | Dettaglio |
|---|---|---|
| Flow non e traversal exec completo | `AIReadableBlueprintPackExporter` | `FlowText` e `FlowJson` includono tutti i nodi del graph per ogni entry, non solo raggiungibili via exec |
| Data dependency non completa | flow | non ricostruisce dipendenze pure/constant/branch condition in modo semantico profondo |
| Widget tree parziale | UMG | non usa designer tree UMG dedicato, inferisce da nomi/nodi |
| Componenti parziali | Actor Blueprint | non esporta SCS, attach socket, transform, collision, mesh in modo affidabile |
| Campi member/function/variable vuoti | Blueprint node export | i campi sono presenti ma non popolati da classi K2 specializzate |
| Search basata su euristiche | AI-readable pack | `GuessSearchKind`, `GuessSymbolKind`, `GuessUsage` usano string matching su class name |
| File obsoleti fuori `BlueprintExports` | output root | root JSON/Obsidian non viene pulita |
| Git da plugin opzionale ma delicato | Git workflow | dipende da repo, executable, permessi, credenziali esterne |
| Tooltips/testi in italiano e inglese misti | UI/docs | naming misto nel codice e nei messaggi |
| Automation test modifica settings temporanei | test | salva config durante test e poi ripristina |
| Output Obsidian non pulito | Obsidian | note vecchie possono restare se asset non esportato |
| Pack AI-readable cancella cartella | BlueprintExports | comportamento corretto per stale files, ma distruttivo solo verso quella sottocartella |

## Warning esterni noti

Nel codice sono presenti stringhe di warning/report, ma non warning TODO. Warning di build osservati in precedenza derivano da toolchain/Engine/plugin esterni, non dal codice documentato qui.

## Architettura migliorabile

- `BlueprintJSONExporter.cpp` contiene molte funzioni statiche e molte responsabilita.
- `AIReadableBlueprintPackExporter.cpp` e autonomo ma lungo.
- Manca una gerarchia di exporter per asset type.
- Manca astrazione condivisa per writer/paths.
- Alcuni output AI-readable sono derivati da JSON generico invece che da API Unreal specifiche.
