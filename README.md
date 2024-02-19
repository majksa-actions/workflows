# workflows

Stores reusable workflows that can be used from other actions.

## Release please

Example usage:

```yml
name: Release Please

on:
  push:
    branches:
      - main

permissions:
  contents: write
  pull-requests: write

jobs:
  release-please:
    uses: majksa-actions/workflows/.github/workflows/release-please.yml@v1
    secrets: inherit
    with:
      release-type: "simple"
```

## Docker build and push

Example usage:

```yml
name: Build and Publish

on:
  push:
    branches:
      - main

permissions:
  contents: read
  packages: write

jobs:
  build-and-push-image:
    uses: majksa-actions/workflows/.github/workflows/docker-build-and-push.yml@v1
    secrets: inherit
```
