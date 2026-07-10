# Implementation History

## Come usare questo documento

Questo documento e il registro tecnico permanente delle modifiche realmente applicate al plugin BlueprintJSONExporter.

- Ogni modifica futura al plugin deve aggiungere una nuova voce.
- Le voci piu recenti devono stare in alto, subito sotto la sezione "Stato iniziale documentato" o sopra le voci operative precedenti.
- Ogni voce deve descrivere solo cambiamenti effettivamente applicati al codice, alla configurazione, agli output o alla documentazione.
- Non devono essere registrate richieste non implementate.
- Bug, limiti o verifiche mancanti devono essere indicati esplicitamente come aperti, parziali o non verificati.
- In caso di rollback, aggiungere una nuova voce di rollback invece di cancellare la voce originale.

## Stato iniziale documentato

### 2026-07-10 - Baseline documentale dello stato attuale

**Stato**
- baseline documentale

**Fonti usate**
- codice attuale in `BJE21Clean/`
- documenti presenti in `Documentation/`
- `BJE21Clean/BlueprintJSONExporter.uplugin`

**Cronologia Git**
- Cronologia Git non usata come fonte storica affidabile.
- Nel workspace era presente una cartella `.git` nel root, ma dalle ricognizioni precedenti non risultava un repository Git valido utilizzabile per ricostruire la storia del plugin.
- Le informazioni sotto sono quindi una baseline ricostruita e documentata dallo stato corrente, non una cronologia commit-by-commit.

**Versione rilevata**
- `BJE21Clean/BlueprintJSONExporter.uplugin` dichiara:
  - `Version`: `6`
  - `VersionName`: `2.4.0`
  - modulo `BlueprintJSONExporter`, tipo `Editor`, loading phase `Default`

**Funzionalita principali presenti**
- Export Editor-only, sola lettura.
- Menu contestuali nel Content Browser per asset e cartelle.
- Export JSON pretty-print per asset supportati.
- Export Obsidian in `Unreal Blueprint Export/`.
- Export `.canvas` per Blueprint.
- Manifest dell'export.
- Cartella `AI_Context/` con file Markdown e JSON semantici.
- Cartella `BlueprintExports/` con pack AI-readable.
- Indici globali `GLOBAL_INDEX.json`, `GLOBAL_SEARCH.jsonl`, `GLOBAL_SYMBOL_INDEX.jsonl`, `GLOBAL_ASSET_INDEX.md`.
- Output per asset, graph e flow.
- Workflow Git opzionale con add, commit, push, summary, change report e semantic diff.
- Automation test presente nel codice per formati asset read-only e verifiche di output.

**Tipi di asset supportati**
- `UBlueprint`
- Widget Blueprint come caso generico di `UBlueprint`, con supporto UMG specifico parziale
- Actor Blueprint come caso generico di `UBlueprint`
- Component Blueprint come caso generico di `UBlueprint`
- Animation Blueprint come caso generico di `UBlueprint`
- `UDataTable`
- `UUserDefinedStruct`
- `UUserDefinedEnum`

**Output principali**
- JSON asset completo pretty-print.
- `manifest.json`.
- `AI_Context/AI_Context.md`.
- `AI_Context/AI_Instructions.md`.
- `AI_Context/AssetIndex.md`.
- `AI_Context/BlueprintSummaries.md`.
- `AI_Context/ChangeReport.md`.
- `AI_Context/CompileStatus.md`.
- `AI_Context/DataModel.md`.
- `AI_Context/DependencyMap.md`.
- `AI_Context/ExportSummary.md`.
- `AI_Context/LargeGraphs.md`.
- `AI_Context/ProjectOverview.md`.
- `AI_Context/SemanticDiff.json`.
- `AI_Context/SemanticSummary.json`.
- `AI_Context/SystemMap.md`.
- `BlueprintExports/GLOBAL_INDEX.json`.
- `BlueprintExports/GLOBAL_SEARCH.jsonl`.
- `BlueprintExports/GLOBAL_SYMBOL_INDEX.jsonl`.
- `BlueprintExports/GLOBAL_ASSET_INDEX.md`.
- `BlueprintExports/assets/<AssetKey>/...`.
- Obsidian notes per categoria.
- Canvas JSON `.canvas`.
- `.AIExportCache/PreviousManifest.json`.
- `.AIExportCache/PreviousSemanticSummary.json`.

**Classi principali**
- `FBlueprintJSONExporterModule`
- `UBlueprintJSONExporterSettings`
- `FAIContextExporter`
- `FAIReadableBlueprintPackExporter`
- `FAssetSystemClassifier`
- `FSemanticSummaryBuilder`
- `FGitCommandRunner`
- `FExportChangeTracker`
- `FSemanticDiffBuilder`
- `FChangeReportWriter`
- `FExportSummaryWriter`
- `FGitExportWorkflow`

**Modelli principali**
- `FExportStats`
- `FAssetRelation`
- `FSemanticGraph`
- `FSemanticAssetRecord`
- `FAIContextResult`
- `FReadableBlueprintInput`
- `FReadableBlueprintPackResult`
- `FGitCommandResult`
- `FGitWorkflowResult`
- `FExportPostProcessInput`
- `FExportPostProcessResult`

**Funzionalita parziali**
- Flow AI-readable: presente, ma non ricostruisce un traversal exec completo; include dati del graph in modo ampio.
- Data dependency dei flow: parziale.
- Widget tree UMG: parziale, inferito da graph/nodi e nomi; non risulta un export completo del designer tree tramite API UMG dedicate.
- Component export: parziale, inferito; non risulta un export completo di SCS, transform, collision, mesh e attachment.
- Function/event index: presente ma in parte inferito.
- Campi `memberName`, `functionName`, `variableName`, `targetClass`: presenti nello schema nodi, ma non risultano popolati in modo specialistico per ogni nodo K2.

**Problemi noti**
- La root export classica non viene pulita, quindi possono restare file obsoleti fuori da `BlueprintExports/`.
- `BlueprintExports/` viene cancellata e rigenerata a ogni pack.
- Il workflow Git dipende da configurazione locale, repository, eseguibile Git e credenziali esterne.
- Non e presente un commandlet dedicato.
- Non e presente un custom details panel.
- Non e presente una toolbar dedicata; il codice registra menu Content Browser.
- Non sono presenti TODO/FIXME/HACK/TEMP reali nei sorgenti analizzati, secondo la documentazione generata.

**Impostazioni Git gia presenti**
- `bEnableGitIntegration`, default `false`.
- `bAutoGitAdd`, default `false`.
- `bAutoGitCommit`, default `false`.
- `bAutoGitPush`, default `false`.
- `GitExecutablePath`, default vuoto, usa `git` da PATH.
- `GitRepositoryPath`, default vuoto, usa output directory.
- `GitCommitMessageTemplate`, default `Blueprint Export {DateTime}`.

**Altre impostazioni presenti**
- `OutputDirectory`, default vuoto; fallback a `ProjectSavedDir()/BlueprintAIExports`.
- `bGenerateChangeReport`, default `true`.
- `bGenerateSemanticDiff`, default `true`.

**File Documentation presenti al momento della baseline**
- `Documentation/AI_CONTEXT.md`
- `Documentation/Architecture.md`
- `Documentation/AssetSupport.md`
- `Documentation/Classes.md`
- `Documentation/ExportFormats.md`
- `Documentation/ExtensionGuide.md`
- `Documentation/Features.md`
- `Documentation/GeneratedChangelog.md`
- `Documentation/KnownIssues.md`
- `Documentation/Outputs.md`
- `Documentation/Settings.md`
- `Documentation/Todo.md`
- `Documentation/Workflow.md`
- `Documentation/ImplementationHistory.md`

**Verifiche della baseline**
- Questa voce non registra una nuova build.
- Questa voce non registra nuovi test.
- Questa voce documenta lo stato corrente senza modificare il plugin.

### 2026-07-10 - Sanitizzazione filename flow AI-readable

**Stato**
- completata

**Obiettivo**
- Correggere la generazione dei filename AI-readable quando nomi evento, graph o asset contengono newline, tab, caratteri di controllo o caratteri non validi su Windows.

**Modifiche applicate**
- Aggiunto `FFilenameSanitizer` come funzione centralizzata riutilizzabile per componenti di filename.
- La sanitizzazione sostituisce whitespace, newline, tab, caratteri di controllo e `< > : " / \ | ? *` con `_`.
- Comprime underscore multipli, rimuove punti/spazi finali, gestisce nomi vuoti e nomi riservati Windows.
- Applicata la regola ad asset key, graph key, entry/flow name e filename legacy generati dal plugin.
- Migliorata la diagnostica di scrittura AI-readable con path finale, directory padre, esistenza directory, lunghezza path e risultato writer.
- Il testo interno dei Flow mantiene il nome originale dell'evento.

**File modificati**
- `BJE21Clean/Source/BlueprintJSONExporter/Private/AIReadableBlueprintPackExporter.cpp`: uso sanitizer e logging writer.
- `BJE21Clean/Source/BlueprintJSONExporter/Private/BlueprintJSONExporter.cpp`: uso sanitizer per componenti filename generati.
- `Documentation/ImplementationHistory.md`: voce operativa.
- `Documentation/AI_CONTEXT.md`: nota naming sicuro.
- `Documentation/KnownIssues.md`: aggiornamento bug flow risolto.
- `Documentation/Features.md`: test e sanitizzazione filename.
- `Documentation/Outputs.md`: regola filesystem per output canonico.

**Nuovi file**
- `BJE21Clean/Source/BlueprintJSONExporter/Private/FilenameSanitizer.h`: API sanitizer.
- `BJE21Clean/Source/BlueprintJSONExporter/Private/FilenameSanitizer.cpp`: implementazione e automation test.

**Output modificati**
- Per `UpdatePrompt\nCustom_Event` con GUID breve `F8E3B2BE`:
  - `UpdatePrompt_Custom_Event__F8E3B2BE__FLOW.txt`
  - `UpdatePrompt_Custom_Event__F8E3B2BE__FLOW.json`

**Test e verifiche**
- Build UE 5.4 eseguita con `RunUAT BuildPlugin`.
- Risultato build: successo, package `BJE_Pkg_v24_FilenameFix`.
- Automation test eseguiti su host temporaneo `BJE_FilenameTestHost`.
- Test passati:
  - `BlueprintJSONExporter.FilenameSanitizer.ParentDirectoryWrite`
  - `BlueprintJSONExporter.FilenameSanitizer.SafeComponents`
- Nessun push Git eseguito.
- Nessun asset Unreal modificato.

**Problemi noti introdotti o rimasti**
- Verifica manuale finale su `WBP_GenericPrompt` ancora consigliata dentro il progetto reale per confermare l'assenza di warning specifici dell'asset.

**Compatibilita**
- Verificato con Unreal Engine 5.4.
- Nessuna migrazione richiesta per i contenuti Unreal.

**Documentazione aggiornata**
- `ImplementationHistory.md`
- `AI_CONTEXT.md`
- `KnownIssues.md`
- `Features.md`
- `Outputs.md`

**Rollback**
- Ripristinare la generazione precedente dei componenti filename e rimuovere `FilenameSanitizer.*`; sconsigliato perche' reintrodurrebbe il bug su newline/caratteri Windows non validi.

### 2026-07-10 - Pipeline AI canonica e pubblicazione Git gestita

**Stato**
- parziale: codice e documentazione aggiornati; build UE 5.4 riuscita; test editor/automation non eseguiti

**Obiettivo**
- Rendere `Exported_Files_forAI` il pacchetto canonico per AI, sincronizzare documentazione/export nel repository Git configurato e rimuovere la dipendenza operativa dal BAT mantenendolo come fallback.

**Modifiche applicate**
- Aggiunto validatore `FAIExportPackageValidator`.
- Spostato il pacchetto AI-readable da `BlueprintExports` a `Exported_Files_forAI`.
- Aggiunto supporto al pacchetto canonico per Blueprint, DataTable, Struct ed Enum.
- Aggiunti `README.md`, `EXPORT_MANIFEST.json`, `EXPORT_STATUS.md` nel pacchetto canonico.
- Aggiunta sincronizzazione gestita verso `Plugin_Documentation` e `Exported_Files_forAI` nel repository Git.
- Sostituito `git add -A` generico con pathspec limitato alle cartelle gestite.
- Aggiunti controlli su Git, branch, remote e upstream prima del push.
- Aggiunta conferma esplicita in Editor prima delle azioni che possono eseguire push reale.
- Disabilitata di default la scrittura dei JSON legacy nella root tramite `bIncludeLegacyRootJson=false`.

**File modificati**
- `BJE21Clean/Source/BlueprintJSONExporter/Public/BlueprintJSONExporterSettings.h`: nuovi setting.
- `BJE21Clean/Source/BlueprintJSONExporter/Private/AIReadableBlueprintPackExporter.cpp`: nuovo pacchetto canonico e manifest/status.
- `BJE21Clean/Source/BlueprintJSONExporter/Private/BlueprintJSONExporter.cpp`: menu, selectors, export canonico, test aggiornati.
- `BJE21Clean/Source/BlueprintJSONExporter/Private/GitExportWorkflow.cpp`: validazione, sync e Git pathspec limitati.
- `Documentation/*.md`: documentazione tecnica aggiornata.

**Nuovi file**
- `BJE21Clean/Source/BlueprintJSONExporter/Private/AIExportPackageValidator.h`: API validatore pacchetto AI.
- `BJE21Clean/Source/BlueprintJSONExporter/Private/AIExportPackageValidator.cpp`: implementazione validazione JSON/JSONL.

**Impostazioni aggiunte o modificate**
- `DocumentationSourceDirectory`, default vuoto, persistenza `EditorPerProjectUserSettings`.
- `bGenerateObsidianOutput=false`, persistenza `EditorPerProjectUserSettings`.
- `bValidateBeforePublish=true`, persistenza `EditorPerProjectUserSettings`.
- `bRequireCompleteExportBeforePublish=true`, persistenza `EditorPerProjectUserSettings`.
- `bIncludeLegacyRootJson=false`, persistenza `EditorPerProjectUserSettings`.
- `bKeepBatFallback=true`, persistenza `EditorPerProjectUserSettings`.

**Output modificati**
- Nuovo canonico: `<OutputDirectory>/Exported_Files_forAI/`.
- Repository AI: `<GitRepositoryPath>/Plugin_Documentation/` e `<GitRepositoryPath>/Exported_Files_forAI/`.
- `BlueprintExports` resta storico, non canonico.
- JSON legacy in root non vengono cancellati automaticamente.

**Test e verifiche**
- Build plugin UE 5.4 eseguita con `RunUAT BuildPlugin`.
- Risultato build: successo, package `BJE_Pkg_v24_AIRepo`.
- Test editor/automation non eseguiti in questa voce.
- Verifica manuale Unreal ancora richiesta.
- Nessun push reale eseguito da Codex.

**Problemi noti introdotti o rimasti**
- Azione di pulizia legacy con dry-run e doppia conferma ancora da implementare in una modifica separata.
- Obsidian resta opzionale e disabilitato di default.

**Compatibilita**
- Target dichiarato: Unreal Engine 5.4.
- Richiede configurazione esplicita di `GitRepositoryPath` separato da `OutputDirectory`.
- Le configurazioni che dipendevano dal fallback implicito del repository sull'output devono impostare il repository Git.

**Documentazione aggiornata**
- `AI_CONTEXT.md`
- `Architecture.md`
- `Classes.md`
- `ExportFormats.md`
- `Features.md`
- `KnownIssues.md`
- `Outputs.md`
- `Settings.md`
- `Todo.md`
- `Workflow.md`
- `ImplementationHistory.md`

**Rollback**
- Ripristinare `BlueprintExports` come root del pack in `FAIReadableBlueprintPackExporter`.
- Rimuovere validatore/sync gestito da `FGitExportWorkflow`.
- Ripristinare `git add -A` solo se accettabile per il repository operativo.

## Template per le modifiche future

### YYYY-MM-DD - Titolo modifica

**Stato**
- completata | parziale | annullata | rollback

**Obiettivo**
- descrizione sintetica della richiesta

**Modifiche applicate**
- elenco concreto delle funzionalita implementate

**File modificati**
- percorso file
- motivo della modifica

**Nuovi file**
- percorso
- scopo

**Impostazioni aggiunte o modificate**
- nome setting
- default
- posizione di persistenza

**Output modificati**
- file/cartelle interessati
- compatibilita con output precedenti

**Test e verifiche**
- build eseguita
- test eseguiti
- risultato
- eventuali verifiche manuali ancora richieste

**Problemi noti introdotti o rimasti**
- elenco

**Compatibilita**
- versione Unreal
- migrazioni richieste
- impatto su configurazioni precedenti

**Documentazione aggiornata**
- elenco dei file Documentation aggiornati

**Rollback**
- indicazioni sintetiche per annullare la modifica, se applicabile

## Regole permanenti

1. Dopo ogni implementazione futura, aggiornare `ImplementationHistory.md`.
2. Aggiornare anche i documenti tecnici interessati:
   - `AI_CONTEXT.md`
   - `Features.md`
   - `KnownIssues.md`
   - `Todo.md`
   - `Settings.md`
   - `Outputs.md`
   - `Workflow.md`
   - altri file pertinenti.
3. Non dichiarare "completata" una funzione se la build o la verifica richiesta non e stata eseguita.
4. Segnalare esplicitamente:
   - codice compilato ma non testato in Unreal;
   - test parziali;
   - limitazioni note;
   - cambiamenti incompatibili.
5. Non rimuovere le voci precedenti.
6. In caso di rollback, aggiungere una nuova voce invece di cancellare la vecchia.
7. Usare percorsi e nomi reali delle classi.
8. Evitare descrizioni generiche come "miglioramenti vari".
