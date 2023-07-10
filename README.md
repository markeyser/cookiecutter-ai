# Cookiecutter AI

_A logical, reasonably standardized, but flexible project structure for doing
and sharing artificial intelligence work._

This is a
[Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/readme.html)
template designed for establishing the groundwork of artificial intelligence
projects. It incorporates industry-standard methodologies and integrates tools
for tasks such as testing, linting, creating documentation, and implementing
continuous integration.

## Features

- Comprehensive Python environment setup with `requirements.txt` and
  `pyproject.toml` for package management.
- Pre-configured linting and formatting tools: Black, flake8, pylint, and a
  pre-commit configuration.
- Testing setup with pytest, including a dedicated directory for test files.
- Documentation generator using MkDocs, including a pre-configured `mkdocs.yml`
  and a directory for project documentation.
- GitHub-specific configurations such as Code Owners, Issue Templates, and Pull
  Request Templates for better project management.
- A structured data directory, organized into `external`, `interim`,
  `processed`, and `raw` subfolders for different stages of data processing.
- Jupyter notebooks for data exploration and experimentation.
- Source code directory for all the project code.
- `Makefile` with predefined commands to simplify complex workflows.
- `setup.py` to make the project pip installable.
- Environment variable file `.env` for managing sensitive information.
- Configuration directory for project-specific settings.
- VS Code specific configurations for consistent development environments.
- CI/CD configuration (if any, e.g., GitHub Actions, GitLab CI/CD).

## Requirements to use the cookiecutter template

- Python 3.5+
- [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/readme.html)
  Python package

## Usage

First, make sure you have installed cookiecutter:

```shell
pip install cookiecutter
```

To generate a new project, run:

```shell
cookiecutter gh:markeyser/cookiecutter-ai
```

Follow the prompts to enter your project details.

## The resulting directory structure

The directory structure of your new project looks like this:

```text
├── .env                        <- Environment variables for the project.
├── .github                     <- GitHub-specific settings and configurations.
│   ├── CODEOWNERS              <- Specifies individuals or teams that are responsible for code in a repository.
│   ├── ISSUE_TEMPLATE          <- Templates for issues to be used by contributors.
│   │   ├── ask_issues_template.md         <- Issue template for asking questions.
│   │   ├── bug_report_template.md         <- Issue template for reporting bugs.
│   │   ├── data_aquisition_template.md    <- Issue template for data acquisition tasks.
│   │   ├── data_creation_template.md      <- Issue template for data creation tasks.
│   │   ├── experiment_issues_template.md  <- Issue template for experiment tasks.
│   │   ├── explore_issues_template.md     <- Issue template for exploration tasks.
│   │   ├── feature_request.md             <- Issue template for feature requests.
│   │   └── model_issues_templates.md      <- Issue template for model-related tasks.
│   └── PULL_REQUEST_TEMPLATE   <- Templates for pull requests to be used by contributors.
│       └── pull_request_template.md
├── .gitignore                  <- Specifies intentionally untracked files to ignore.
├── .pre-commit-config.yaml     <- Configuration for pre-commit hooks to enforce coding style and checks.
├── .vscode                     <- Configuration for Visual Studio Code editor.
│   ├── extensions.json         <- Specifies extensions recommended for the project in VS Code.
│   └── settings.json           <- Project-specific settings for VS Code.
├── Makefile                    <- Makefile with commands like `make data` or `make train`.
├── READMEmd                    <- The top-level README for developers using this project.
├── configuration               <- Directory for project configuration files.
├── data                        <- Data for the project, divided into different stages of data processing.
│   ├── external                <- Data from third party sources.
│   ├── interim                 <- Intermediate data that has been transformed.
│   ├── processed               <- The final, canonical data sets for modeling.
│   └── raw                     <- The original, immutable data dump.
├── docs                        <- Directory for project documentation.
├── mkdocs.yml                  <- Configuration file for the MkDocs documentation tool.
├── notebooks                   <- Jupyter notebooks for data exploration and experimentation.
├── pyproject.toml              <- Specifies dependencies for the project in a format that pip can understand.
├── requirements.txt            <- The requirements file for reproducing the analysis environment.
├── setup.py                    <- Makes this project pip installable with `pip install -e`.
├── src                         <- Source code for the project.
│   └── __init__.py             <- Makes src a Python module.
└── test                        <- Directory for test files.
```
