# Ploomber sample projects

![CI](https://github.com/ploomber/projects/workflows/ci/badge.svg)
[![Twitter](https://img.shields.io/twitter/follow/edublancas?label=Follow&style=social)](https://twitter.com/intent/user?screen_name=edublancas)

This repository contains sample pipelines developed using [Ploomber](https://github.com/ploomber/ploomber)

**Note:** Make sure you read the [first two tutorials](https://ploomber.readthedocs.io/en/stable/get-started/spec-api-python.html) in the documentation to familiarize yourself with Ploomber's basic concepts.

## Running examples

Use Binder (no need to install anything but it takes a few minutes to load):

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ploomber/binder-env/main?urlpath=git-pull%3Frepo%3Dhttps%253A%252F%252Fgithub.com%252Fploomber%252Fprojects%26urlpath%3Dlab%252Ftree%252Fprojects%252FREADME.ipynb%26branch%3Dmaster)

Or run locally:

~~~sh
pip install ploomber

# list examples
ploomber examples

# download one example
ploomber examples --name {name}
~~~

## How to read the examples

Each example contains a `README.md` file with more information, and a
`README.ipynb` file, which has the same contents as the `.md` file but in a
Jupyter notebook format and with the output from each cell.

## Index

### Basic

{% for idx, name, entry, description in basic %}
{{idx}}. [`{{name}}/`]({{name}}/README.{{entry}}) {{description}}
{% endfor %}

### Intermediate

{% for idx, name, entry, description in intermediate %}
{{idx}}. [`{{name}}/`]({{name}}/README.{{entry}}) {{description}}
{% endfor %}

### Advanced

{% for idx, name, entry, description in advanced %}
{{idx}}. [`{{name}}/`]({{name}}/README.{{entry}}) {{description}}
{% endfor %}

## Guides

These are part of the [documentation](https://ploomber.readthedocs.io/en/stable/user-guide/index.html).


1. [`spec-api-python/`](spec-api-python/README.ipynb) Introductory tutorial
2. [`parametrized/`](parametrized/README.ipynb) Pipeline with input parameters
3. [`debugging/`](debugging/README.ipynb) Pipeline to demonstrate debugging capabilities
4. [`testing/`](testing/README.ipynb) Pipeline with SQL and Python tasks showing how to test pipelines
5. [`sql-templating/`](sql-templating/README.ipynb) SQL pipeline showing how to use macros to write concise SQL scripts
6. [`logging`](guides/logging/README.ipynb) Logging configuration
7. [`serialization`](guides/serialization/README.ipynb) Configuring serialization for function tasks

## Python API

The simplest way to get started with Ploomber is via the Spec API, which allows you to describe pipelines using a `pipeline.yaml` file, most examples on this repository use the Spec API. However, if you want more flexibility, you may write pipelines with Python.

The [`python-api/`](python-api) directory contains a project written using the Python API. And the [`python-api-examples/`](python-api-examples) includes some tutorials and more examples.

