# Settings

Classe:

```text
UBlueprintJSONExporterSettings
```

Config:

```text
config=EditorPerProjectUserSettings
Category=Plugins
Section="Blueprint JSON Exporter"
```

Persistenza tipica:

```text
Saved/Config/<Platform>Editor/EditorPerProjectUserSettings.ini
```

## Elenco settings

| Nome | Tipo | Default | Chi la legge | Quando cambia |
|---|---|---|---|---|
| `OutputDirectory` | `FDirectoryPath` | vuoto | `GetOutputDirectory`, `ChooseOutputDirectory` | UI "Imposta cartella" |
| `bEnableGitIntegration` | `bool` | `false` | `FGitExportWorkflow` | settings editor/test |
| `bAutoGitAdd` | `bool` | `false` | `FGitExportWorkflow` | settings editor/test |
| `bAutoGitCommit` | `bool` | `false` | `FGitExportWorkflow` | settings editor/test |
| `bAutoGitPush` | `bool` | `false` | `FGitExportWorkflow` | settings editor/test |
| `GitExecutablePath` | `FFilePath` | vuoto | `GetGitExecutable` | settings editor/test |
| `GitRepositoryPath` | `FDirectoryPath` | vuoto | `GetRepositoryPath` | settings editor/test |
| `GitCommitMessageTemplate` | `FString` | `Blueprint Export {DateTime}` | `ReplacePlaceholders` | settings editor/test |
| `bGenerateChangeReport` | `bool` | `true` | `FGitExportWorkflow` | settings editor/test |
| `bGenerateSemanticDiff` | `bool` | `true` | `FGitExportWorkflow` | settings editor/test |

## Default impostati nel costruttore

```text
GitCommitMessageTemplate = "Blueprint Export {DateTime}"
bGenerateChangeReport = true
bGenerateSemanticDiff = true
```

## Directory output

## Settings aggiunti 2026-07-10

- `DocumentationSourceDirectory` (`FDirectoryPath`): cartella sorgente della documentazione tecnica da copiare nel repository AI come `Plugin_Documentation/`.
- `bGenerateObsidianOutput` (`bool`, default `false`): mantiene Obsidian come output opzionale e non canonico.
- `bValidateBeforePublish` (`bool`, default `true`): valida `Exported_Files_forAI` prima di sync/Git.
- `bRequireCompleteExportBeforePublish` (`bool`, default `true`): blocca la pubblicazione se `EXPORT_MANIFEST.json` indica `complete=false`.
- `bIncludeLegacyRootJson` (`bool`, default `false`): impedisce la rigenerazione dei JSON legacy nella root di `OutputDirectory`.
- `bKeepBatFallback` (`bool`, default `true`): documenta la conservazione del BAT come fallback operativo.

`GitRepositoryPath` resta separato da `OutputDirectory` e identifica il working tree Git in cui pubblicare solo le cartelle gestite.


Se `OutputDirectory` e vuoto:

```text
FPaths::ProjectSavedDir() / "BlueprintAIExports"
```

Se relativo:

- path che inizia con `..`: convertito a full path.
- altrimenti relativo a `ProjectDir`.

Se assoluto:

- normalizzato con `FPaths::ConvertRelativePathToFull`.
