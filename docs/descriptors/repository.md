---
title: REPOSITORY linters in MegaLinter
description: checkov, devskim, dustilock, git_diff, gitleaks, grype, kics, ls-lint, secretlint, semgrep, syft, trivy, trivy-sbom, trufflehog are available to analyze REPOSITORY files in MegaLinter
---
<!-- markdownlint-disable MD003 MD020 MD033 MD041 -->
<!-- @generated by .automation/build.py, please don't update manually -->
<!-- Instead, update descriptor file at https://github.com/oxsecurity/megalinter/tree/main/megalinter/descriptors/repository.yml -->
# REPOSITORY

## Linters

| Linter                                                                                             | Additional                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**checkov**](repository_checkov.md)<br/>[_REPOSITORY_CHECKOV_](repository_checkov.md)             | [![GitHub stars](https://img.shields.io/github/stars/bridgecrewio/checkov?cacheSeconds=3600)](https://github.com/bridgecrewio/checkov) ![sarif](https://shields.io/badge/-SARIF-orange)   |
| [**devskim**](repository_devskim.md)<br/>[_REPOSITORY_DEVSKIM_](repository_devskim.md)             | [![GitHub stars](https://img.shields.io/github/stars/microsoft/DevSkim?cacheSeconds=3600)](https://github.com/microsoft/DevSkim) ![sarif](https://shields.io/badge/-SARIF-orange)         |
| [**dustilock**](repository_dustilock.md)<br/>[_REPOSITORY_DUSTILOCK_](repository_dustilock.md)     | [![GitHub stars](https://img.shields.io/github/stars/Checkmarx/dustilock?cacheSeconds=3600)](https://github.com/Checkmarx/dustilock) ![sarif](https://shields.io/badge/-SARIF-orange)     |
| [**git_diff**](repository_git_diff.md)<br/>[_REPOSITORY_GIT_DIFF_](repository_git_diff.md)         | [![GitHub stars](https://img.shields.io/github/stars/git/git?cacheSeconds=3600)](https://github.com/git/git)                                                                              |
| [**gitleaks**](repository_gitleaks.md)<br/>[_REPOSITORY_GITLEAKS_](repository_gitleaks.md)         | [![GitHub stars](https://img.shields.io/github/stars/gitleaks/gitleaks?cacheSeconds=3600)](https://github.com/gitleaks/gitleaks) ![sarif](https://shields.io/badge/-SARIF-orange)         |
| [**grype**](repository_grype.md)<br/>[_REPOSITORY_GRYPE_](repository_grype.md)                     | [![GitHub stars](https://img.shields.io/github/stars/anchore/grype?cacheSeconds=3600)](https://github.com/anchore/grype) ![sarif](https://shields.io/badge/-SARIF-orange)                 |
| [**kics**](repository_kics.md)<br/>[_REPOSITORY_KICS_](repository_kics.md)                         | [![GitHub stars](https://img.shields.io/github/stars/checkmarx/kics?cacheSeconds=3600)](https://github.com/checkmarx/kics) ![sarif](https://shields.io/badge/-SARIF-orange)               |
| [**ls-lint**](repository_ls_lint.md)<br/>[_REPOSITORY_LS_LINT_](repository_ls_lint.md)             | [![GitHub stars](https://img.shields.io/github/stars/loeffel-io/ls-lint?cacheSeconds=3600)](https://github.com/loeffel-io/ls-lint)                                                        |
| [**secretlint**](repository_secretlint.md)<br/>[_REPOSITORY_SECRETLINT_](repository_secretlint.md) | [![GitHub stars](https://img.shields.io/github/stars/secretlint/secretlint?cacheSeconds=3600)](https://github.com/secretlint/secretlint) ![sarif](https://shields.io/badge/-SARIF-orange) |
| [**semgrep**](repository_semgrep.md)<br/>[_REPOSITORY_SEMGREP_](repository_semgrep.md)             | [![GitHub stars](https://img.shields.io/github/stars/returntocorp/semgrep?cacheSeconds=3600)](https://github.com/returntocorp/semgrep) ![sarif](https://shields.io/badge/-SARIF-orange)   |
| [**syft**](repository_syft.md)<br/>[_REPOSITORY_SYFT_](repository_syft.md)                         | [![GitHub stars](https://img.shields.io/github/stars/anchore/syft?cacheSeconds=3600)](https://github.com/anchore/syft) ![sarif](https://shields.io/badge/-SARIF-orange)                   |
| [**trivy**](repository_trivy.md)<br/>[_REPOSITORY_TRIVY_](repository_trivy.md)                     | [![GitHub stars](https://img.shields.io/github/stars/aquasecurity/trivy?cacheSeconds=3600)](https://github.com/aquasecurity/trivy) ![sarif](https://shields.io/badge/-SARIF-orange)       |
| [**trivy-sbom**](repository_trivy_sbom.md)<br/>[_REPOSITORY_TRIVY_SBOM_](repository_trivy_sbom.md) | [![GitHub stars](https://img.shields.io/github/stars/aquasecurity/trivy?cacheSeconds=3600)](https://github.com/aquasecurity/trivy) ![sarif](https://shields.io/badge/-SARIF-orange)       |
| [**trufflehog**](repository_trufflehog.md)<br/>[_REPOSITORY_TRUFFLEHOG_](repository_trufflehog.md) | [![GitHub stars](https://img.shields.io/github/stars/trufflesecurity/trufflehog?cacheSeconds=3600)](https://github.com/trufflesecurity/trufflehog)                                        |

## Linted files

## Configuration in MegaLinter

| Variable                        | Description                                     | Default value |
|---------------------------------|-------------------------------------------------|---------------|
| REPOSITORY_PRE_COMMANDS         | List of bash commands to run before the linters | None          |
| REPOSITORY_POST_COMMANDS        | List of bash commands to run after the linters  | None          |
| REPOSITORY_FILTER_REGEX_INCLUDE | Custom regex including filter                   |               |
| REPOSITORY_FILTER_REGEX_EXCLUDE | Custom regex excluding filter                   |               |

