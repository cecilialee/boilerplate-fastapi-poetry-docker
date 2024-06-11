# FastAPI + Poetry Boilerplate

# Install Poetry

The official [Poetry documentation](https://python-poetry.org/docs/) suggests to install Poetry with `pipx`. `pipx` is used to install Python CLI applications globally while still isolating them in virtual environments. pipx will manage upgrades and uninstalls when used to install Poetry.

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
