# FastAPI + Poetry Boilerplate

## Requirements

- [Poetry](https://python-poetry.org/) for Python package and environment management.
- [FastAPI](https://fastapi.tiangolo.com/) for Python RESTful API.
- [Docker](https://www.docker.com/) for containerization and deployment.

## Quickstart

```sh
git clone git@github.com:Salfiii/fastapi-template.git
```

### Prepare Environment

> [!NOTE]
>
> The project uses [Poetry](https://python-poetry.org/) for package and environment management. If Poetry is not already installed, following the installation steps at the later sections.

Install the project dependencies specified in `pyproject.toml` and `poetry.lock` and create Poetry virtual environment. 

```sh
poetry install
```

## Build from Scatch

### Install Poetry

If Poetry is not already installed, install Poetry following the steps below.


The official [Poetry documentation](https://python-poetry.org/docs/) suggested to install Poetry with `pipx`. `pipx` is used to install Python CLI applications globally while still isolating them in virtual environments. pipx will manage upgrades and uninstalls when used to install Poetry.

If `pipx` is not already installed, install following the official [pipx documentation](https://pipx.pypa.io/stable/installation/) according to the OS system.

```sh
# macOS
brew install pipx
pipx ensurepath # add pipx to PATH environment variable
sudo pipx ensurepath --global # optional to allow pipx actions in global scope
```

Install Poetry with `pipx`.

```sh
pipx install poetry
```

### Initialize a Poetry Project

Initialize a pre-populated directory as a Poetry project by creating a basic `pyproject.toml` file in the current directory.

```sh
cd [directory]
poetry init
```

The command will guide the process of creating the `pyproject.toml` config. Provide required package information. Particularly, supply python version as `^3.11` and `fastapi` as a main dependecy. 

Manually add the following config to `pyproject.toml` under `[tool].poetry` section to use Poetry only for dependency management but not for packaging.

```toml
package-mode = false
```

The resulting file should be as follows.

```toml
[tool.poetry]
name = "your-project-name"
version = "0.1.0"
description = "Your project description."
authors = ["Your Name <your@email.com>"]
readme = "README.md"
package-mode = false

[tool.poetry.dependencies]
python = "^3.11"
fastapi = "^0.111.0"


[build-system]
requires = ["poetry-core"]
build-backend = "poetry.core.masonry.api"
```

**Optional:** Add dependencies that are only needed for test and development, for example `pytest` and `ipykernel`.

```sh
poetry add pytest ipykernel --group dev
```

### Prepare Poetry Environment

Install the project dependencies specified in `pyproject.toml` and create Poetry virtual environment.

```sh
poetry install
```

> [!TIP]
> List all the environments with the current project. The newly created environment should be shown and marked as `Activated`.
> 
> ```sh
> poetry env list
> ```
>
> List all the available packages installed in the environment.
> 
> ```sh
> poetry show
> ```


