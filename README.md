[![PyPI version](https://img.shields.io/pypi/v/offlinedatasci.svg)](https://pypi.python.org/pypi/offlinedatasci/)
[![Python versions supported](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/github/license/carpentriesoffline/offlinedatasci.svg)](https://github.com/carpentriesoffline/offlinedatasci/blob/main/LICENSE)
[![Build Check](https://github.com/carpentriesoffline/offlinedatasci/actions/workflows/package-check.yml/badge.svg)](https://github.com/carpentriesoffline/offlinedatasci/actions/workflows/package-check.yml)
[![Documentation Status](https://readthedocs.org/projects/offlinedatasci/badge/?version=latest)](https://offlinedatasci.readthedocs.io/en/latest/?badge=latest)
![PyPI - Downloads](https://img.shields.io/pypi/dm/offlinedatasci)

# OfflineDataSci

This package helps you download and configure common tools for teaching and doing data science without an internet connection.
This includes:

* Installers for data science languages: Currently R and Python
* Installers for common data science IDEs: Currently RStudio
* Partial local mirrors of package repositories: Currently CRAN (for R) and PyPI (for Python)
* Locally browseable clones of data science teaching websites: Currently Data Carpentry and Software Carpentry

## Status

Early stage experiment

## Installation

### Install the CLI (using pipx):

We recomend that most users install the command line interface (CLI) using [pipx](https://pipx.pypa.io/).
This will produce an isolated installation than can be run using the CLI.
First, [install pipx](https://pipx.pypa.io/stable/installation/) and then run:

```sh
pipx install offlinedatasci
```

### Using pip:

To install the package into the current Python environment using pip:

```sh
pip install offlinedatasci
```

### Installing development versions

If you need functionality that has been implemented but not released yet you can install the development version.

#### Directly From GitHub

To install directly from GitHub without have a local copy of the code to edit:

```sh
pip install git+https://git@github.com/carpentriesoffline/offlinedatasci.git
```

#### Locally

To download and then install the code (which provides a local copy of the code to edit), first clone the repository and then from the root directory run:

```sh
git clone https://github.com/carpentriesoffline/offlinedatasci.git
cd offlinedatasci
pip install .
```

On macOS make sure wheel package is installed first.

## Usage

### Download and setup everything

Download and install everything (~2 GB):

```sh
offlinedatasci install all <path>
```

### Create a local CRAN mirror

Create just the local CRAN mirror with basic data science packages (~0.5 GB):

```sh
offlinedatasci install r-packages <path>
```

### Add packages to repository mirrors:

To add packages beyond those included in the basic data science teaching focused mirrors use `add-packages`
The command structure is `offlinedatasci add-packages` followed by the language you want to add packages to, followed by the names of the packages, followed by the path of the mirror.
The path should be the same as where the mirror was originally setup, so the same install path you used for setup offlinedatasci.

For example, to add the `sf`, `terra`, and `stars` geospatial packages to the CRAN mirror: 

```sh
offlinedatasci add r-packages package1 package2 ... <path>
```

## Developer docs

### Creating a release

1. Increment the version numbers in `pyproject.toml`, `__init__.py`, and `docs/conf.py`
2. Commit and push the changes to GitHub
3. Create a tag for the new version
4. Push the tag to GitHub (`git push upstream <tag_name>`)
5. Make sure the `build` package is installed
6. Make sure your PyPI credentials are stored in `~/.pypirc`
7. Build the source distribution: `python -m build --sdist`
8. Build the universal wheel: `python -m build --wheel`
9. Upload the new release to PyPI: `twine upload dist/*`
