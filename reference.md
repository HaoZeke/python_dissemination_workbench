---
title: "Reference"
---

# Glossary

Abstract Dependency
:   A dependency declaration with loose version constraints (e.g.,
    `numpy>=1.20`{.verbatim}) as found in `pyproject.toml`{.verbatim},
    maximizing compatibility with other packages.

Artifact
:   A file produced by the build process, typically a source
    distribution (`.tar.gz`{.verbatim}) or a wheel (`.whl`{.verbatim}).

Build Backend
:   The tool that converts source code into installable artifacts (e.g.,
    `hatchling`{.verbatim}, `meson-python`{.verbatim},
    `setuptools`{.verbatim}, `uv_build`{.verbatim}).

Build Frontend
:   The tool that invokes the build backend (e.g.,
    `uv build`{.verbatim}, `pip wheel`{.verbatim},
    `python -m build`{.verbatim}).

cibuildwheel
:   A tool that builds binary wheels for multiple platforms using CI
    services such as GitHub Actions.

Concrete Dependency
:   An exact, pinned version of a package (e.g.,
    `numpy==2.1.0`{.verbatim}) as recorded in a lockfile, ensuring
    reproducibility.

`conda-forge`{.verbatim}
:   A community-maintained channel of `conda`{.verbatim} packages
    providing both Python libraries and system-level binaries.

Constraint Satisfaction
:   The process a package manager uses to find a set of dependency
    versions that simultaneously satisfy all requirements without
    conflicts.

Continuous Integration (CI)
:   The practice of automatically running tests and checks on every code
    push, typically using a service like GitHub Actions.

Dependency Group
:   A named set of dependencies in `pyproject.toml`{.verbatim} (e.g.,
    `dev`{.verbatim}, `docs`{.verbatim}) that can be installed
    selectively. Defined by PEP 735.

Editable Install
:   An installation mode (`uv pip install -e .`{.verbatim}) where
    changes to source code are immediately reflected without
    reinstalling.

F2PY
:   A tool (part of NumPy) that generates Python bindings for Fortran
    subroutines, producing C wrapper code and shared objects.

GitHub Actions
:   A CI/CD platform integrated into GitHub that runs workflows defined
    in YAML files on push, pull request, or other events.

Inline Script Metadata
:   A PEP 723 feature that embeds dependency declarations directly in a
    Python script using a special comment block
    (`# /// script`{.verbatim}).

Lockfile
:   A file (e.g., `uv.lock`{.verbatim}) that pins the exact versions of
    all direct and transitive dependencies for reproducibility.

Manylinux
:   A standard that defines a minimal set of Linux system libraries a
    binary wheel may depend on, ensuring broad compatibility across
    distributions.

Matrix Strategy
:   A CI configuration that runs the same job across multiple
    combinations of parameters (e.g., Python versions and operating
    systems).

Meson
:   A build system used for compiling C, C++, and Fortran code into
    shared libraries. Used by NumPy and SciPy.

`meson-python`{.verbatim}
:   A PEP 517 build backend that integrates the Meson build system with
    Python packaging, enabling compiled extensions in wheels.

Module
:   A single `.py`{.verbatim} file that can be imported.

News Fragment
:   A small text file (e.g., `news/42.feature`{.verbatim}) used by
    `towncrier`{.verbatim} to record a single changelog entry, avoiding
    merge conflicts.

OIDC (Trusted Publishing)
:   An authentication method allowing GitHub Actions to publish to PyPI
    without storing API tokens, using OpenID Connect identity
    verification.

Package
:   A directory containing an `__init__.py`{.verbatim} file (and usually
    other modules), making it importable as a unit.

PEP
:   Python Enhancement Proposal. A design document that describes a new
    feature or standard for Python. Key PEPs in this lesson: 518, 517,
    621, 668, 723, 735, 751.

`pixi`{.verbatim}
:   A cross-platform package manager for managing system dependencies
    and task automation via `conda-forge`{.verbatim}.

Pixibang
:   A shebang line
    (`#!/usr/bin/env -S pixi exec ... -- uv run`{.verbatim}) that chains
    `pixi`{.verbatim} and `uv`{.verbatim} to provide both system
    binaries and Python packages for a single script.

`prek`{.verbatim}
:   A Rust rewrite of the `pre-commit`{.verbatim} tool for running git
    hooks that enforce code quality checks before commits.

Pre-commit Hook
:   A git hook that runs automated checks (linting, formatting) before a
    commit is finalized, preventing bad code from entering the
    repository.

`pyproject.toml`{.verbatim}
:   The standard configuration file for Python projects (PEP 621),
    replacing `setup.py`{.verbatim} and `setup.cfg`{.verbatim}.

PyPI
:   The Python Package Index, the default repository for Python
    packages.

`pytest`{.verbatim}
:   A testing framework for Python that discovers and runs test
    functions, providing detailed failure reports.

`ruff`{.verbatim}
:   An extremely fast Python linter and formatter written in Rust,
    replacing `flake8`{.verbatim}, `black`{.verbatim}, and
    `isort`{.verbatim}.

Shadowing
:   When a local file has the same name as a standard library module
    (e.g., `math.py`{.verbatim}), causing Python to import the local
    file instead.

Shared Object
:   A compiled binary (`.so`{.verbatim} on Linux, `.dylib`{.verbatim} on
    macOS, `.dll`{.verbatim} on Windows) that Python can load as an
    extension module.

Shebang
:   The first line of a script (starting with `#!`{.verbatim}) that
    tells the operating system which interpreter to use to execute the
    file.

Source Distribution (sdist)
:   A compressed archive of the source code (`.tar.gz`{.verbatim}) that
    requires a build step before installation.

Sphinx
:   The standard documentation generator for Python projects, converting
    reStructuredText or Markdown into HTML, PDF, or other formats.

`src`{.verbatim} Layout
:   A project structure where the package source lives under a
    `src/`{.verbatim} directory, preventing accidental imports from the
    project root.

`sys.path`{.verbatim}
:   The list of directories Python searches when resolving
    `import`{.verbatim} statements.

Test PyPI
:   A separate instance of PyPI (`test.pypi.org`{.verbatim}) used for
    testing package uploads without affecting the production index.

`towncrier`{.verbatim}
:   A tool for managing changelogs using per-change fragment files to
    avoid merge conflicts.

Transitive Dependency
:   A package that is not directly required by your project but is
    pulled in as a dependency of one of your direct dependencies.

`uv`{.verbatim}
:   A fast Python package installer and project manager from Astral,
    written in Rust.

`uvx`{.verbatim}
:   A tool runner from `uv`{.verbatim} that fetches and executes a
    command-line tool in an ephemeral environment without permanent
    installation.

Virtual Environment
:   An isolated Python environment with its own
    `site-packages`{.verbatim} directory, preventing dependency
    conflicts between projects.

Wheel
:   A binary distribution format (`.whl`{.verbatim}) that can be
    installed without a build step. It is essentially a ZIP archive with
    a standardized layout.

# Key Commands

## `uv`{.verbatim} Commands

  Command                                  Description
  ---------------------------------------- -----------------------------------------------------------
  `uv init --lib`{.verbatim}               Create a new library project with `src`{.verbatim} layout
  `uv add <package>`{.verbatim}            Add a runtime dependency
  `uv add --dev <package>`{.verbatim}      Add a development dependency
  `uv add --group docs <pkg>`{.verbatim}   Add a dependency to a named group
  `uv sync --dev`{.verbatim}               Install all dependencies including dev
  `uv run <command>`{.verbatim}            Run a command in the project environment
  `uv build`{.verbatim}                    Build sdist and wheel into `dist/`{.verbatim}
  `uv pip install -e .`{.verbatim}         Install the project in editable mode
  `uv python install 3.12`{.verbatim}      Install a specific Python version
  `uvx twine upload dist/*`{.verbatim}     Upload artifacts to PyPI
  `uvx <tool>`{.verbatim}                  Run a tool in an ephemeral environment

## `pixi`{.verbatim} Commands

  Command                                        Description
  ---------------------------------------------- ----------------------------------------
  `pixi init`{.verbatim}                         Initialize a new pixi project
  `pixi add <package>`{.verbatim}                Add a conda dependency
  `pixi run <task>`{.verbatim}                   Run a defined task
  `pixi exec --spec <pkg> -- <cmd>`{.verbatim}   Run a command with a package available

## `ruff`{.verbatim} Commands

  Command                              Description
  ------------------------------------ ------------------------------------------
  `ruff check .`{.verbatim}            Lint the current directory
  `ruff check --fix .`{.verbatim}      Lint and auto-fix issues
  `ruff format .`{.verbatim}           Format code according to style rules
  `ruff format --check .`{.verbatim}   Check formatting without modifying files

## `pytest`{.verbatim} Commands

  Command                                  Description
  ---------------------------------------- ----------------------------------------------------
  `pytest`{.verbatim}                      Run all tests in the `tests/`{.verbatim} directory
  `pytest --cov=src`{.verbatim}            Run tests with code coverage reporting
  `pytest -v`{.verbatim}                   Run tests with verbose output
  `pytest tests/test_file.py`{.verbatim}   Run tests from a specific file

## `towncrier`{.verbatim} Commands

  Command                                        Description
  ---------------------------------------------- -----------------------------------------------------------------------------------
  `towncrier create <num>.<type>`{.verbatim}     Create a changelog fragment (e.g., `1.feature`{.verbatim}, `2.bugfix`{.verbatim})
  `towncrier build --version X.Y.Z`{.verbatim}   Compile fragments into the changelog
  `towncrier build --yes`{.verbatim}             Compile fragments without confirmation

## `prek`{.verbatim} Commands

  Command                     Description
  --------------------------- ---------------------------------------------
  `prek`{.verbatim}           Run all configured pre-commit hooks
  `prek install`{.verbatim}   Install hooks into `.git/hooks/`{.verbatim}

## `f2py`{.verbatim} / Meson Commands

  Command                                                    Description
  ---------------------------------------------------------- -----------------------------------------
  `f2py -c file.f90 -m modname`{.verbatim}                   Compile Fortran into a Python extension
  `f2py -c file.f90 -m modname --build-dir out`{.verbatim}   Compile with intermediate files visible

## Sphinx Commands

  Command                                                         Description
  --------------------------------------------------------------- -----------------------------
  `sphinx-quickstart`{.verbatim}                                  Initialize a docs directory
  `sphinx-build -b html docs/source docs/build/html`{.verbatim}   Build HTML documentation

# Useful Links

## Core Standards

-   [Python Packaging User Guide](https://packaging.python.org/)
-   [Writing
    pyproject.toml](https://packaging.python.org/en/latest/guides/writing-pyproject-toml/)
-   [PEP 517: Build System Interface](https://peps.python.org/pep-0517/)
-   [PEP 518: Build System
    Requirements](https://peps.python.org/pep-0518/)
-   [PEP 621: Project Metadata](https://peps.python.org/pep-0621/)
-   [PEP 723: Inline Script Metadata](https://peps.python.org/pep-0723/)
-   [PEP 735: Dependency Groups](https://peps.python.org/pep-0735/)
-   [PEP 751: Lock Files
    (pylock.toml)](https://peps.python.org/pep-0751/)

## Tools

-   [uv Documentation](https://docs.astral.sh/uv/)
-   [pixi Documentation](https://pixi.prefix.dev/)
-   [ruff Documentation](https://docs.astral.sh/ruff/)
-   [pytest Documentation](https://docs.pytest.org/)
-   [prek Documentation](https://prek.j178.dev/cli/)
-   [towncrier Documentation](https://towncrier.readthedocs.io/)
-   [Sphinx Documentation](https://www.sphinx-doc.org/)
-   [sphinx-autoapi
    Documentation](https://sphinx-autoapi.readthedocs.io/)

## Build Systems

-   [Meson Build System](https://mesonbuild.com/)
-   [meson-python Documentation](https://meson-python.readthedocs.io/)
-   [F2PY User Guide (NumPy)](https://numpy.org/doc/stable/f2py/)
-   [cibuildwheel Documentation](https://cibuildwheel.pypa.io/)

## Platforms

-   [Test PyPI](https://test.pypi.org/)
-   [PyPI (Production)](https://pypi.org/)
-   [GitHub Actions Documentation](https://docs.github.com/en/actions)
-   [astral-sh/setup-uv Action](https://github.com/astral-sh/setup-uv)
