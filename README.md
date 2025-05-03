# Python test, build and publish

## Overview

This repository contains a convenient set of actions useful for developing
and publishing Python packages using:

- pytest
- pytest-cov
- ruff
- uv

## Motivation

These actions were created when I found myself repeating the same patterns.

## Actions available

The following actions are available and can be used individually in your GitHub workflows:

- `deeprave/actions/test@main`: Run tests using pytest
- `deeprave/actions/test-build@main`: Run tests and build the package
- `deeprave/actions/test-build-publish@main`: Run tests, build and publish the package
- `deeprave/actions/test-build-publish-with-cov@main`: Run tests with coverage, build and publish the package
- `deeprave/actions/test-build-with-cov@main`: Run tests with coverage and build the package
- `deeprave/actions/test-with-cov@main`: Run tests with coverage reporting

## Usage

To use these actions in your GitHub workflow, add them to your workflow YAML file:

```yaml
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: deeprave/actions/test@main
        with:
          python-version: '3.13'
```

See each action's YAML file for available input parameters.
