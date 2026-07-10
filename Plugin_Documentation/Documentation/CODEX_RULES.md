# Codex Rules — BlueprintJSONExporter

## 1. Priorita delle regole

- Queste regole sono permanenti e non negoziabili.
- Devono essere lette prima di ogni modifica al plugin.
- In caso di conflitto tra un prompt futuro e queste regole, Codex deve fermarsi, descrivere il conflitto e chiedere conferma.
- Il codice reale nel workspace e la fonte di verita tecnica.
- La documentazione deve essere mantenuta coerente con il codice.
- Non dichiarare mai esistente o completata una funzione senza verificarla nel codice e, quando richiesto, con build/test.

## 2. Sicurezza e natura del plugin

- Il plugin deve restare Editor-only.
- Il plugin deve restare read-only rispetto agli asset Unreal.
- Non modificare, salvare, ricompilare o alterare asset di gioco.
- Non modificare gameplay Blueprint, mappe, DataTable, Struct, Enum o altri `.uasset`.
- Non cancellare file o cartelle fuori dalle directory esplicitamente gestite.
- Validare ogni percorso prima di operazioni distruttive.
- Non inserire credenziali, token GitHub o segreti nel codice, nei config, nei BAT o nella documentazione.

## 3. Compatibilita

- Mantenere compatibilita con Unreal Engine 5.4 salvo richiesta esplicita.
- Usare API Unreal appropriate per plugin Editor.
- Non introdurre dipendenze esterne non necessarie.
- Non cambiare modulo, `.uplugin` o dipendenze senza motivazione tecnica documentata.
- Preservare impostazioni e formati esistenti quando possibile.

## 4. Preservazione delle funzionalita

- Non rimuovere output, menu, settings o workflow esistenti salvo richiesta esplicita.
- Non riscrivere interi sottosistemi se basta una modifica locale.
- Prima di modificare, identificare file e classi realmente coinvolti.
- Preservare export Blueprint, DataTable, User Defined Struct e User Defined Enum.
- Preservare AI Context, AI-readable pack, Git workflow e Obsidian finche non viene chiesta esplicitamente la rimozione.
- Obsidian deve restare opzionale e non necessario per il workflow AI principale.
- Evitare duplicazioni di exporter, writer, validatori e logica path.

## 5. Regole sugli output

- Tutti i file testuali devono essere UTF-8.
- Usare newline LF quando tecnicamente possibile.
- Tutti i normali file `.json` devono essere validi, multilinea e pretty-printed con indentazione di 2 spazi.
- Non minificare i normali `.json` su una sola riga.
- I file `.jsonl` devono contenere esattamente un oggetto JSON valido per riga.
- Non pretty-printare un record JSONL su piu righe.
- Evitare righe eccessivamente lunghe.
- Splittare i file grandi quando il formato lo consente.
- Mantenere `nodeGuid`, `pinId` e riferimenti stabili quando disponibili.
- Non serializzare un intero JSON dentro una stringa `content` salvo necessita documentata.
- Ogni export deve indicare almeno:
  - `schemaVersion`;
  - `pluginVersion`;
  - `unrealEngineVersion`;
  - `generatedAt`;
  - `complete` o stato equivalente.
- Manifest e indici devono rappresentare l'export corrente e non file obsoleti.

## 6. Struttura canonica del repository AI

Struttura permanente:

```text
UnrealGitRepository/
  Plugin_Documentation/
  Exported_Files_forAI/
```

- `Plugin_Documentation/` contiene la copia sincronizzata di `Documentation/`.
- `Exported_Files_forAI/` contiene l'export corrente del progetto Unreal destinato all'AI.
- I percorsi sorgente devono restare distinti:
  - `DocumentationSourceDirectory`;
  - `OutputDirectory`.
- Il repository deve essere configurato separatamente tramite `GitRepositoryPath`.
- Il plugin puo rigenerare o sincronizzare soltanto:
  - `Plugin_Documentation/`;
  - `Exported_Files_forAI/`.
- Il plugin non deve mai cancellare o modificare:
  - `.git/`;
  - il `README.md` root non gestito;
  - `.gitignore` utente;
  - `LICENSE`;
  - altri file esterni alle cartelle gestite.

## 7. Struttura degli asset esportati

- Ogni asset deve usare un `AssetKey` stabile derivato dall'asset path Unreal.
- Ogni Blueprint deve avere una cartella dedicata.
- Graphs e Flows devono stare dentro la cartella del Blueprint relativo.
- DataTable, Struct ed Enum devono avere cartelle dedicate.
- Evitare file asset sparsi nella root.
- Gli indici globali devono consentire di trovare asset, simboli, graph e flow senza aprire subito il JSON completo.

Ordine di lettura AI:

```text
README
→ EXPORT_STATUS
→ GLOBAL_INDEX / GLOBAL_SEARCH / GLOBAL_SYMBOL_INDEX
→ asset SUMMARY / INDEX
→ Graphs / Flows
→ FULL.pretty.json
```

## 8. Export e repository Git

- `OutputDirectory` e `GitRepositoryPath` devono essere distinti.
- L'export deve essere completato e validato prima della sincronizzazione Git.
- Verificare che il repository esista e contenga `.git`.
- Non mostrare successo se sincronizzazione, add, commit o push falliscono.
- Non creare commit se non ci sono modifiche.
- Controllare tutti gli exit code.
- Usare `git add` soltanto sui path gestiti.
- Non usare automaticamente `git add .`.
- Il plugin non deve dipendere da un BAT per il workflow principale.
- Eventuali BAT esistenti sono fallback temporanei.
- Codex non deve eseguire push reali come parte delle normali modifiche al codice.
- La pubblicazione viene gestita dal plugin, salvo richiesta esplicita dell'utente.
- Non salvare credenziali o token.

## 9. Documentazione obbligatoria

Dopo ogni modifica reale Codex deve:

- aggiornare `Documentation/ImplementationHistory.md`;
- aggiornare `Documentation/AI_CONTEXT.md`;
- aggiornare tutti i documenti tecnici pertinenti;
- non aggiornare documenti non coinvolti senza motivo;
- distinguere sempre:
  - implementato;
  - compilato;
  - testato automaticamente;
  - verificato manualmente in Unreal;
  - non verificato;
- non dichiarare "completata" una funzione se build o verifica richiesta non sono state eseguite;
- non cancellare voci precedenti da `ImplementationHistory.md`;
- in caso di rollback, aggiungere una nuova voce;
- sincronizzare `CODEX_RULES.md` nel repository tramite il workflow del plugin.

## 10. Processo obbligatorio prima di modificare

Sequenza obbligatoria:

1. leggere `Documentation/CODEX_RULES.md`;
2. leggere `Documentation/AI_CONTEXT.md`;
3. leggere `Documentation/ImplementationHistory.md`;
4. leggere i documenti pertinenti;
5. ispezionare il codice reale;
6. identificare file, classi, settings e output coinvolti;
7. verificare modifiche non committate;
8. descrivere brevemente il piano;
9. applicare modifiche minimali e coerenti;
10. aggiornare la documentazione;
11. compilare;
12. correggere tutti gli errori;
13. eseguire i test disponibili;
14. riportare con precisione cosa e stato e non e stato verificato.

## 11. Build e test

- Compilare il plugin dopo modifiche C++.
- Correggere tutti gli errori introdotti.
- Non ignorare warning importanti.
- Usare test automatici esistenti quando pertinenti.
- Aggiungere test mirati per nuove funzionalita critiche.
- Per output JSON verificare almeno:
  - file esistente;
  - JSON valido;
  - multilinea per `.json`;
  - un record per riga per `.jsonl`;
  - manifest coerente.
- Per Git verificare errori di repository, add, commit e push.
- Non simulare test non eseguiti.
- Indicare chiaramente le verifiche manuali ancora necessarie in Unreal Editor.

## 12. Gestione percorsi

- Non hardcodare percorsi utente o di progetto.
- Usare settings e API Unreal.
- Normalizzare e validare tutti i path.
- Supportare spazi e caratteri non ASCII.
- Impedire che sorgente e destinazione coincidano quando e pericoloso.
- Impedire cancellazioni sulla root del repository.
- Non inventare il percorso della documentazione.
- Usare `DocumentationSourceDirectory` come fonte della documentazione da sincronizzare.

## 13. Qualita del codice

- Usare nomi coerenti con il codice esistente.
- Mantenere separate le responsabilita di:
  - export asset;
  - writer;
  - validazione;
  - sincronizzazione;
  - Git workflow.
- Riutilizzare helper esistenti.
- Aggiungere nuovi file solo quando migliorano davvero la separazione delle responsabilita.
- Non fare refactoring estesi non richiesti.
- Commentare solo la logica non ovvia.
- Non lasciare TODO, FIXME, HACK o codice temporaneo senza documentazione.

## 14. Accuratezza semantica

- Preferire API Unreal specifiche alle euristiche basate sui titoli localizzati.
- Non basarsi solo su stringhe visibili dei nodi.
- Usare classi K2, member reference, property reference, function reference e class reference quando disponibili.
- Preservare GUID, riferimenti e relazioni reali.
- Dichiarare quando un output e inferito, parziale o euristico.
- Non rappresentare dati inferiti come certi.

## 15. Divieti permanenti

- Non modificare asset di gioco.
- Non inserire segreti.
- Non fare push reali da Codex.
- Non cancellare la cronologia documentale.
- Non minificare i normali JSON.
- Non usare JSONL multilinea.
- Non cancellare la root del repository.
- Non dichiarare test non eseguiti.
- Non inventare API, percorsi o funzionalita.
- Non usare la copia del plugin dentro il progetto Unreal come fonte primaria se il workspace di sviluppo contiene la versione corrente.
- Non ignorare conflitti con queste regole.

## 16. Checklist finale obbligatoria

Ogni futura sessione dovra riportare questa checklist nel riepilogo finale:

- [ ] CODEX_RULES letto
- [ ] AI_CONTEXT letto
- [ ] ImplementationHistory letto
- [ ] codice reale analizzato
- [ ] asset Unreal non modificati
- [ ] output esistenti preservati
- [ ] documentazione aggiornata
- [ ] build eseguita
- [ ] errori di compilazione corretti
- [ ] test eseguiti
- [ ] verifiche manuali mancanti dichiarate
- [ ] nessun push Git reale eseguito da Codex
- [ ] nessun segreto inserito
- [ ] modifiche e limiti riepilogati con precisione

