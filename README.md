# FastAPI + Poetry Boilerplate

## Requirements

- [Poetry](https://python-poetry.org/) for Python package and environment management.
- [FastAPI](https://fastapi.tiangolo.com/) for Python RESTful API.
- [Docker](https://www.docker.com/) for containerization and deployment.

## Prerequisites

- Install [Poetry](https://python-poetry.org/) following the official documentation.
- Install [Docker](https://www.docker.com/) following the official documentation.

## Quickstart

Clone the boilerplate from GitHub.

```sh
git clone git@github.com:Salfiii/fastapi-template.git
```

### Prepare Environment

Install the project dependencies specified in `pyproject.toml` and `poetry.lock` and create Poetry virtual environment. 

```sh
poetry install
```

### Serve on Local Development Mode

The FastAPI local development mode has auto-reload enabled by default, so it will automatically reload the server when code changes are made. This is resource intensive and should only be used for development.

Run FastAPI development mode under Poetry virtual environment.

```sh
poetry run fastapi dev app/main.py
```

Alternatively, activate the Poetry nested shell and run FastAPI development mode. Exit the shell with `exit`.

```sh
poetry shell
fastapi dev app/main.py
```

By default it servces at http://127.0.0.1, which is the localhost. The Swagger API documentation is available at http://127.0.0.1:8000/docs.

## Build from Scatch

### Create Poetry Environment

#### Initialize pyproject.toml

Create a basic `pyproject.toml` file in the current directory.

```sh
cd [directory]
poetry init
```

The command will guide the process of creating the `pyproject.toml` config. Set python version as `^3.11`. Provide the following packages as main dependencies.

- `fastapi`
- `pydantic-settings`

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


