# FastAPI + Poetry Boilerplate

## Requirements

- [Poetry](https://python-poetry.org/) for Python package and environment management.
- [FastAPI](https://fastapi.tiangolo.com/) for Python RESTful API.
- [Docker](https://www.docker.com/) for containerization and deployment.

## Quickstart

### Prerequisites

- Install [Poetry](https://python-poetry.org/) following the official documentation.
- Install [Docker](https://www.docker.com/) following the official documentation.
- Clone the boilerplate from GitHub.

```sh
git clone git@github.com:Salfiii/fastapi-template.git [project-name]
```

### Prepare Environment

Install the project dependencies specified in `pyproject.toml` and `poetry.lock` and create Poetry virtual environment. 

```sh
poetry install
```

## Build from Scatch

### Prepare Environment

#### Initialize pyproject.toml

Initialize a pre-populated directory as a Poetry project by creating a basic `pyproject.toml` file in the current directory.

```sh
cd [directory]
poetry init
```

The command will guide the process of creating the `pyproject.toml` config. Provide required package information. Particularly, supply python version as `^3.11` and `fastapi` as a main dependecy. 

Manually add the following config to `pyproject.toml` to use Poetry only for dependency management but not for packaging.

```toml
[tool].poetry
package-mode = false
```

**Optional:** Add dependencies that are only needed for test and development, for example `pytest` and `ipykernel`.

```sh
poetry add pytest ipykernel --group dev
```

#### Install Project Dependencies

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


