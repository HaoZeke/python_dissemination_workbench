---
title: "Setup"
---

## Software setup

::: discussion
### Details

We basically require `pixi` and `uv`. For conciseness, we reproduce the
most direct instructions below.

Technically any Python interpreter suffices, here we use `pixi` to
handle system dependencies and run tasks, with `uv` for managing Python
dependencies and environments.
:::

::: spoiler
### Windows

Following along with the `pixi` [instructions upstream
here](https://pixi.prefix.dev/latest/installation/#__tabbed_1_2).

``` bash
powershell -ExecutionPolicy Bypass -c "irm -useb https://pixi.sh/install.ps1 | iex"
```

Along with `uv` from [the official installation
documentation](https://docs.astral.sh/uv/getting-started/installation/#__tabbed_1_2).

``` bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```
:::

::: spoiler
### MacOS and Linux

Following along with the `pixi` [instructions upstream
here](https://pixi.prefix.dev/latest/installation/#__tabbed_1_1).

``` bash
curl -fsSL https://pixi.sh/install.sh | sh
```

Along with `uv` [from the official
documentation](https://docs.astral.sh/uv/getting-started/installation/#__tabbed_1_1).

``` bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
:::

## Accounts required

To finalize publishing to an index [^1] we need:

A Git instance in the cloud
:   Any of Github, Gitlab, Sourcehut etc. would work, [Github is
    recommended](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github).

An index account
:   For the tutorial [Test
    PyPI](https://test.pypi.org/account/register/) will suffice, for
    production, an account [on PyPI](https://pypi.org/account/register/)
    would be required as well.

::: checklist
-   [ ] I have an account on a Git server
-   [ ] I have an account on Test PyPI
:::

[^1]: Making the code widely available over the net
