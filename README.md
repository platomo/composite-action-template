# [Action Name]

This GitHub Action [describes what the Action does].

## Description

This Action is useful for [describe specific use case of the Action]. It enables [brief explanation of key functions and steps of the Action].

## Inputs

| Name         | Description                    | Required | Default                        |
| ------------ | ------------------------------ | -------- | ------------------------------ |
| `input-name` | Description of the input value | Yes/No   | [Default value, if applicable] |
| `input-name` | Description of the input value | Yes/No   | [Default value, if applicable] |
| ...          | ...                            | ...      | ...                            |

## Usage

Create a workflow file (e.g., `.github/workflows/[workflow-name].yml`) and use this Action as follows:

```yaml
name: [Workflow Name]

on:
  push:
    branches:
      - main

jobs:
  [job-name]:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: [Action Name]
        uses: ./
        with:
          input-name: "[Example value]"
          input-name: "[Example value]"
```

## Workflow Steps

Install pypa/build: Installs the build package, required for building the Python package.
Build Wheel and Source Tarball: Builds the package and creates both .whl and .tar.gz files in the dist/ folder.
Publish Package to TestPyPI: Uses gh-action-pypi-publish to upload the package files to the specified TestPyPI repository.

## Required Permissions

To successfully run the Action, an authentication token must be stored in the repository secrets (secrets) to publish the package to TestPyPI.
