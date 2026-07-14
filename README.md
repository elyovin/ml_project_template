# PyTorch Template for DL projects

<p align="center">
  <a href="#installation">Installation</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#credits">Credits</a> •
  <a href="#license">License</a>
</p>

## Installation

This project uses [`uv`](https://docs.astral.sh/uv/) for dependency and Python
version management. The Python version is pinned in `.python-version` (3.11).

0. Install `uv` (see the [installation guide](https://docs.astral.sh/uv/getting-started/installation/)):

   ```bash
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```

1. Create the environment and install all dependencies (including dev tools). `uv`
   automatically downloads Python 3.11 if it is not already available and creates a
   `.venv` in the project root:

   ```bash
   uv sync
   ```

2. Install `pre-commit`:

   ```bash
   uv run pre-commit install
   ```

## How To Use

To train a model, run the following command:

```bash
uv run python train.py -cn=CONFIG_NAME HYDRA_CONFIG_ARGUMENTS
```

Where `CONFIG_NAME` is a config from `src/configs` and `HYDRA_CONFIG_ARGUMENTS` are optional arguments.

To run inference (evaluate the model or save predictions):

```bash
uv run python inference.py HYDRA_CONFIG_ARGUMENTS
```

> You can also activate the environment (`source .venv/bin/activate`) and run
> `python train.py ...` directly, without the `uv run` prefix.

## Credits

This repository is based on a heavily modified fork of [pytorch-template](https://github.com/victoresque/pytorch-template) and [asr_project_template](https://github.com/WrathOfGrapes/asr_project_template) repositories.

## License

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)
