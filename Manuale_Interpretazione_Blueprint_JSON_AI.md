# Manuale di interpretazione dei JSON Blueprint per AI

Questo manuale spiega come leggere correttamente i file JSON generati dal plugin BlueprintJSONExporter per Unreal Engine. Va fornito a una AI insieme a manifest.json e ai JSON dei singoli Blueprint.

## Scopo

I JSON descrivono Blueprint Unreal in forma testuale e compatta. Servono per analisi, documentazione, refactoring guidato, ricerca di dipendenze, comprensione dei flussi logici e confronto tra Blueprint.

La AI deve considerarli come una rappresentazione statica in sola lettura dello stato del Blueprint al momento dell'esportazione. Non deve presumere che il JSON contenga runtime state, valori dinamici di gioco, asset binari, contenuti .uasset completi o logica C++ non esposta nei grafi.

## File disponibili

La cartella esportata contiene:

- manifest.json: riepilogo generale dell'esportazione.
- Un file .json per ogni Blueprint esportato.

Usare sempre prima manifest.json per capire quali Blueprint sono disponibili, quali hanno errori e dove si trovano i relativi JSON.

## Regole per la AI

1. Non inventare nodi, pin, variabili o dipendenze non presenti nei JSON.
2. Se un campo e assente, vuoto o ambiguo, dichiararlo esplicitamente.
3. Non assumere che un Blueprint sia compilabile solo perche e presente nel JSON.
4. Usare compileStatus per valutare lo stato di compilazione.
5. Usare nodeGuid e pinId come identificatori stabili per ricostruire collegamenti.
6. Non duplicare mentalmente i collegamenti: l'export li ha gia deduplicati.
7. Distinguere tra struttura del grafo, valori predefiniti, dipendenze verso asset e intenzione funzionale dedotta dai titoli dei nodi.
8. Quando si descrive il comportamento, separare fatti osservati da inferenze.

## Struttura del manifest

Il file manifest.json contiene informazioni globali:

- schemaVersion: versione dello schema dell'export.
- unrealEngineVersion: versione di Unreal usata.
- outputDirectory: cartella di output.
- blueprintsExported: numero di Blueprint esportati correttamente.
- blueprintsWithErrors: numero di Blueprint con errori.
- blueprints: elenco dei Blueprint.

Ogni voce in blueprints contiene:

- name: nome del Blueprint.
- path: percorso asset Unreal.
- jsonPath: percorso del JSON specifico.
- mainClass: classe generata principale.
- compileStatus: stato di compilazione.
- graphCount: numero di grafi.
- nodeCount: numero di nodi.
- pinCount: numero di pin.
- linkCount: numero di collegamenti.
- functions: funzioni rilevate.
- events: eventi rilevati.
- mainDependencies: dipendenze principali.
- errors: errori avvenuti durante l'esportazione.

Usare il manifest per priorita e navigazione. Per analisi dettagliata, aprire il JSON specifico indicato da jsonPath.

## Struttura del JSON di un Blueprint

Ogni JSON Blueprint contiene:

- schemaVersion
- unrealEngineVersion
- name
- path
- type
- mainClass
- parentClass
- compileStatus
- implementedInterfaces
- variables
- graphs
- dependencies

### Identita del Blueprint

name, path, type, mainClass e parentClass identificano il Blueprint e la sua classe generata.

Interpretazione consigliata:

- path identifica l'asset nel progetto Unreal.
- mainClass e la classe Blueprint generata, se disponibile.
- parentClass indica la classe base.
- type indica il tipo oggetto Unreal del Blueprint, non necessariamente la categoria di gameplay.

### Stato di compilazione

compileStatus puo indicare, per esempio:

- UpToDate: Blueprint aggiornato.
- UpToDateWithWarnings: compilato con warning.
- Dirty: modificato o da ricompilare.
- Error: stato di errore.
- Unknown: stato non determinato.

La AI deve trattare Dirty, Error e Unknown come segnali di cautela.

### Interfacce

implementedInterfaces e un array di classi interfaccia implementate dal Blueprint.

Usare questo campo per capire contratti esterni, eventi o funzioni che il Blueprint potrebbe dover implementare.

### Variabili

variables contiene oggetti con:

- name: nome variabile.
- type: tipo Unreal/Blueprint in forma compatta.
- defaultValue: valore predefinito testuale, se disponibile.

Il campo type puo contenere parti separate da |, per esempio categoria, sottotipo, oggetto, container o qualificatori come ref, const, weak.

Non interpretare defaultValue come valore runtime: e solo il default salvato/esposto dal Blueprint.

## Grafi

graphs e l'array principale per leggere la logica.

Ogni grafo contiene:

- name: nome del grafo.
- type: tipo di grafo.
- nodes: nodi contenuti.
- links: collegamenti tra pin.

Tipi comuni di grafo:

- EventGraph: grafo eventi.
- Function: funzione Blueprint.
- Macro: macro Blueprint.
- DelegateSignature: firma delegate.
- altri valori indicano classi o tipi di grafo Unreal.

Analizzare ogni grafo separatamente. Non assumere che nodi in grafi diversi siano collegati direttamente, salvo riferimenti espliciti.

## Nodi

Ogni nodo in nodes contiene:

- nodeGuid: identificatore del nodo.
- class: classe Unreal del nodo.
- title: titolo leggibile del nodo.
- comment: commento del nodo, se presente.
- x: posizione X nel grafo.
- y: posizione Y nel grafo.
- pins: pin del nodo.

Interpretazione:

- title e utile per spiegazioni umane.
- class e piu affidabile per classificare il tipo tecnico del nodo.
- comment puo contenere intenzione dell'autore.
- x e y aiutano a ricostruire la disposizione visiva, ma non determinano da soli l'ordine di esecuzione.

## Pin

Ogni pin contiene:

- pinId: identificatore del pin.
- name: nome del pin.
- direction: Input o Output.
- type: tipo del dato o exec pin.
- defaultValue: valore predefinito del pin, se presente.

Interpretazione:

- I pin Input ricevono dati o flusso.
- I pin Output producono dati o flusso.
- I pin di esecuzione sono spesso riconoscibili dal tipo/categoria exec o dal nome.
- Un pin senza collegamenti puo comunque avere un defaultValue.

## Collegamenti

Ogni grafo contiene links, con oggetti:

- fromNodeGuid
- fromPinId
- toNodeGuid
- toPinId

Per ricostruire un collegamento:

1. Trovare il nodo con nodeGuid uguale a fromNodeGuid.
2. Dentro quel nodo, trovare il pin con pinId uguale a fromPinId.
3. Trovare il nodo con nodeGuid uguale a toNodeGuid.
4. Dentro quel nodo, trovare il pin con pinId uguale a toPinId.
5. Interpretare il collegamento come flusso o dato in base al tipo dei pin.

I link sono deduplicati. Non crearne una seconda copia invertendo from e to.

## Dipendenze

dependencies nel JSON Blueprint e mainDependencies nel manifest indicano asset o Blueprint collegati.

Usare questi campi per:

- individuare asset esterni necessari;
- capire riferimenti ad altri Blueprint;
- valutare impatto di modifiche;
- costruire mappe di dipendenza.

Non assumere che ogni dipendenza sia usata direttamente in un nodo visibile: alcune possono derivare da variabili, classi, default, componenti o metadati.

## Metodo consigliato di analisi

Quando una AI riceve questi file, dovrebbe procedere cosi:

1. Leggere manifest.json.
2. Elencare Blueprint esportati, errori e stati di compilazione.
3. Aprire i JSON specifici richiesti.
4. Riassumere identita, classe base, interfacce e variabili.
5. Analizzare i grafi uno alla volta.
6. Per ogni grafo, identificare eventi/funzioni di ingresso.
7. Ricostruire i flussi usando links, non solo la posizione dei nodi.
8. Distinguere flusso di esecuzione da flusso dati.
9. Segnalare dipendenze importanti.
10. Evidenziare incertezze, campi vuoti o stato di compilazione problematico.

## Template di istruzioni da dare alla AI

Usa questo testo quando alleghi i JSON a una AI:

```text
Stai analizzando JSON esportati da Unreal Engine tramite BlueprintJSONExporter.

Interpreta i file come rappresentazione statica e in sola lettura dei Blueprint.
Leggi prima manifest.json, poi i JSON dei Blueprint necessari.

Non inventare informazioni mancanti. Se un campo e vuoto o ambiguo, dichiaralo.
Usa nodeGuid e pinId per ricostruire i collegamenti. I link sono gia deduplicati.
Non dedurre l'ordine di esecuzione dalla posizione x/y: usa i link tra pin.
Se descrivi un comportamento, separa fatti osservati da inferenze.
Considera compileStatus come indicatore di affidabilita del Blueprint esportato.

Quando rispondi:
1. riassumi lo scopo probabile del Blueprint;
2. elenca classe base, interfacce e variabili importanti;
3. descrivi eventi, funzioni e macro;
4. ricostruisci i flussi principali dai links;
5. segnala dipendenze e possibili rischi;
6. indica chiaramente cosa non e determinabile dal JSON.
```

## Limiti della rappresentazione

Il JSON non contiene:

- contenuto binario degli asset;
- file .uasset o .umap;
- stato runtime;
- risultato di una compilazione automatica;
- informazioni non esposte dalle API editor usate;
- comportamento C++ interno non rappresentato nei nodi.

Una AI deve quindi evitare conclusioni assolute quando il comportamento dipende da asset esterni, classi native, componenti non esportati o dati runtime.

## Output consigliato per analisi AI

Quando si chiede una analisi, e utile richiedere una risposta strutturata cosi:

```text
1. Sintesi del Blueprint
2. Stato di compilazione e affidabilita
3. Classe base e interfacce
4. Variabili principali
5. Grafi disponibili
6. Flusso logico principale
7. Eventi e funzioni
8. Dipendenze
9. Problemi o ambiguita
10. Suggerimenti, se richiesti
```

## Nota finale

Il JSON e pensato per essere compatto. Alcuni campi sono stringhe sintetiche invece di oggetti molto dettagliati. In caso di dubbio, preferire una lettura prudente e chiedere ulteriori JSON, screenshot o contesto Unreal prima di proporre modifiche operative.
