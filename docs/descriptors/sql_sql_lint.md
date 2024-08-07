---
title: sql-lint configuration in MegaLinter
description: How to use sql-lint (configure, ignore files, ignore errors, help & version documentations) to analyze SQL files
---
<!-- markdownlint-disable MD033 MD041 -->
<!-- @generated by .automation/build.py, please don't update manually -->
# sql-lint
[![GitHub stars](https://img.shields.io/github/stars/joereynolds/sql-lint?cacheSeconds=3600)](https://github.com/joereynolds/sql-lint) [![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/joereynolds/sql-lint?sort=semver)](https://github.com/joereynolds/sql-lint/releases) [![GitHub last commit](https://img.shields.io/github/last-commit/joereynolds/sql-lint)](https://github.com/joereynolds/sql-lint/commits) [![GitHub commit activity](https://img.shields.io/github/commit-activity/y/joereynolds/sql-lint)](https://github.com/joereynolds/sql-lint/graphs/commit-activity/) [![GitHub contributors](https://img.shields.io/github/contributors/joereynolds/sql-lint)](https://github.com/joereynolds/sql-lint/graphs/contributors/)

_This linter has been disabled in this version_

## sql-lint documentation

- Version in MegaLinter: **1.0.0**
- Visit [Official Web Site](https://github.com/joereynolds/sql-lint#readme){target=_blank}
- See [How to configure sql-lint rules](https://sql-lint.readthedocs.io/en/latest/files/configuration.html){target=_blank}
  - If custom `.sql-config.json` config file isn't found, [.sql-config.json](https://github.com/oxsecurity/megalinter/tree/main/TEMPLATES/.sql-config.json){target=_blank} will be used
- See [Index of problems detected by sql-lint](https://github.com/joereynolds/sql-lint#checks){target=_blank}

[![sql-lint - GitHub](https://gh-card.dev/repos/joereynolds/sql-lint.svg?fullname=)](https://github.com/joereynolds/sql-lint){target=_blank}

## Configuration in MegaLinter

- Enable sql-lint by adding `SQL_SQL_LINT` in [ENABLE_LINTERS variable](https://megalinter.io/beta/configuration/#activation-and-deactivation)
- Disable sql-lint by adding `SQL_SQL_LINT` in [DISABLE_LINTERS variable](https://megalinter.io/beta/configuration/#activation-and-deactivation)

| Variable                                 | Description                                                                                                                                                                                  | Default value                                   |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| SQL_SQL_LINT_ARGUMENTS                   | User custom arguments to add in linter CLI call<br/>Ex: `-s --foo "bar"`                                                                                                                     |                                                 |
| SQL_SQL_LINT_COMMAND_REMOVE_ARGUMENTS    | User custom arguments to remove from command line before calling the linter<br/>Ex: `-s --foo "bar"`                                                                                         |                                                 |
| SQL_SQL_LINT_FILTER_REGEX_INCLUDE        | Custom regex including filter<br/>Ex: `(src\|lib)`                                                                                                                                           | Include every file                              |
| SQL_SQL_LINT_FILTER_REGEX_EXCLUDE        | Custom regex excluding filter<br/>Ex: `(test\|examples)`                                                                                                                                     | Exclude no file                                 |
| SQL_SQL_LINT_CLI_LINT_MODE               | Override default CLI lint mode<br/>- `file`: Calls the linter for each file<br/>- `project`: Call the linter from the root of the project                                                    | `file`                                          |
| SQL_SQL_LINT_FILE_EXTENSIONS             | Allowed file extensions. `"*"` matches any extension, `""` matches empty extension. Empty list excludes all files<br/>Ex: `[".py", ""]`                                                      | `[".sql"]`                                      |
| SQL_SQL_LINT_FILE_NAMES_REGEX            | File name regex filters. Regular expression list for filtering files by their base names using regex full match. Empty list includes all files<br/>Ex: `["Dockerfile(-.+)?", "Jenkinsfile"]` | Include every file                              |
| SQL_SQL_LINT_PRE_COMMANDS                | List of bash commands to run before the linter                                                                                                                                               | None                                            |
| SQL_SQL_LINT_POST_COMMANDS               | List of bash commands to run after the linter                                                                                                                                                | None                                            |
| SQL_SQL_LINT_UNSECURED_ENV_VARIABLES     | List of env variables explicitly not filtered before calling SQL_SQL_LINT and its pre/post commands                                                                                          | None                                            |
| SQL_SQL_LINT_CONFIG_FILE                 | sql-lint configuration file name</br>Use `LINTER_DEFAULT` to let the linter find it                                                                                                          | `.sql-config.json`                              |
| SQL_SQL_LINT_RULES_PATH                  | Path where to find linter configuration file                                                                                                                                                 | Workspace folder, then MegaLinter default rules |
| SQL_SQL_LINT_DISABLE_ERRORS              | Run linter but consider errors as warnings                                                                                                                                                   | `false`                                         |
| SQL_SQL_LINT_DISABLE_ERRORS_IF_LESS_THAN | Maximum number of errors allowed                                                                                                                                                             | `0`                                             |
| SQL_SQL_LINT_CLI_EXECUTABLE              | Override CLI executable                                                                                                                                                                      | `['sql-lint']`                                  |

## IDE Integration

Use sql-lint in your favorite IDE to catch errors before MegaLinter !

|                                                                 <!-- -->                                                                 | IDE                         | Extension Name                                |                                 Install                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------:|-----------------------------|-----------------------------------------------|:-----------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/icons/vim.ico" alt="" height="32px" class="megalinter-icon"></a> | [vim](https://www.vim.org/) | [ale](https://github.com/dense-analysis/ale/) | [Visit Web Site](https://github.com/dense-analysis/ale/){target=_blank} |

## MegaLinter Flavors

This linter is available in the following flavors

|                                                                         <!-- -->                                                                         | Flavor                                               | Description               | Embedded linters |                                                                                                                                                                       Info |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------|:--------------------------|:----------------:|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img src="https://github.com/oxsecurity/megalinter/raw/main/docs/assets/images/mega-linter-square.png" alt="" height="32px" class="megalinter-icon"></a> | [all](https://megalinter.io/beta/supported-linters/) | Default MegaLinter Flavor |       125        | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/oxsecurity/megalinter/beta) ![Docker Pulls](https://img.shields.io/docker/pulls/oxsecurity/megalinter) |

## Behind the scenes

### How are identified applicable files

- File extensions: `.sql`

<!-- markdownlint-disable -->
<!-- /* cSpell:disable */ -->
### How the linting is performed

- sql-lint is called one time by identified file (`file` CLI lint mode)

### Example calls

```shell
sql-lint myfile.sql
```

```shell
sql-lint --config .sql-config.json myfile.sql
```


### Help content

```shell
Usage: sql-lint [options]

Lint sql files and stdin for errors, oddities, and bad practices.

Options:
  -V, --version                output the version number
  --fix [string]               The .sql string to fix (experimental and alpha)
  -d, --driver <string>        The driver to use, must be one of ['mysql',
                               'postgres']
  -v, --verbose                Brings back information on the what it's linting
                               and the tokens generated
  --format <string>            The format of the output, can be one of
                               ['simple', 'json'] (default: "simple")
  --host <string>              The host for the database connection
  --user <string>              The user for the database connection
  --password <string>          The password for the database connection
  --port <string>              The port for the database connection
  --config <string>            The path to the configuration file
  --ignore-errors <string...>  The errors to ignore (comma separated)
  -h, --help                   display help for command
```

### Installation on mega-linter Docker image

- NPM packages (node.js):
  - [sql-lint](https://www.npmjs.com/package/sql-lint)
