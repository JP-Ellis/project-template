# Project Template

This is a template I have created containing the basic structure of most utilities that I use in my projects.

## Features

## Git Ignore

The `.gitignore` file is set up to ignore files which are typically specific to the developer's environment, don't version control well (such as binaries), or are generated during the build process. The `.gitignore` file in this leverages the [GitHub gitignore templates](https://github.com/github/gitignore) extensively.

## Pre-commit

[Pre-commit](https://pre-commit.com/) is a framework for managing and maintaining multi-language Git hooks. This template includes a configuration file (`.pre-commit-config.yaml`) that sets up a number of hooks. Not every hook needs to remain (especially if you're not using the language or tool it's designed for), but they are included as a starting point.

-   [standard pre-commit hooks](https://github.com/pre-commit/pre-commit-hooks)
    -   `check-added-large-files`: Prevents large files from being added to the repository.
    -   `check-case-conflict`: Prevents files with names that would conflict on a case-insensitive filesystem from being added to the repository.
    -   `check-executables-have-shebangs`: Ensures that executable script files have a shebang (`#!/path/to/interpreter`) on the first line.
    -   `check-illegal-windows-names`: Prevents the addition of files with illegal names on Windows (e.g., `NUL`, `CON`, `COM1`, `LPT1`, etc.).
    -   `check-merge-conflict`: Prevents Git merge conflicts from being added to the repository.
    -   `check-shebang-scripts-are-executable`: Ensures that scripts with the executable flag have a shebang.
    -   `check-symlinks`: Prevents symlinks from pointing to nothing.
    -   `check-vcs-permalinks`: Ensures that links to VCS repositories are permanent (e.g., not pointing to `master`).
    -   `destroyed-symlinks`: Prevents a symlink from being replaced with the file it points to (which can be an issue on Windows).
    -   `end-of-file-fixer`: Ensures that files end with a newline.
    -   `fix-byte-order-marker`: Removes the byte order marker (BOM) from files.
    -   `mixed-line-ending`: Prevents mixed line endings in files.
    -   `trailing-whitespace`: Prevents trailing whitespace at the end of lines.

## YAML

Two tools are used to check and format YAML files:

-   [yamllint](https://yamllint.readthedocs.io/en/stable/) is a linter for YAML files. This template includes a configuration file (`.yamllint.yaml`) that sets up a number of rules.
-   [yamlfix](https://github.com/lyz-code/yamlfix/) formats and fixes a number of small issues in YAML files. This template includes a configuration file (`.yamlfix.yaml`) that sets up a number of rules.

It is recommended that `yamlfix` be run before `yamllint` to ensure that the files are formatted correctly before being linted. There are also VS Code recommended extensions and settings specifically targetting YAML files.

## Markdown

Markdown files are checked using [markdownlint](https://github.com/igorshubovych/markdownlint-cli). In addition, a number of extensions are recommended for VS Code to improve the editing experience. Further formatting is done using [mdformat](https://github.com/hukkin/mdformat).
