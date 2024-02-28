# workflows

Stores reusable workflows that can be used from other actions.

- [General](#general)
  - [Release please](#release-please)
  - [Docker build and push](#docker-build-and-push)
  - [Lint PR](#lint-pr)
  - [Deploy to portainer](#deploy-to-portainer)
- [Rust](#rust)
  - [Testing](#testing)
  - [Publish to crates.io](#publish-to-cratesio)

## General

### Release please

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
    secrets:
      RELEASE_PLEASE_TOKEN: ${{ secrets.RELEASE_PLEASE_TOKEN }}
    with:
      release-type: "simple"
```

### Docker build and push

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
```

### Lint PR

Example usage:

```yml
name: "Lint PR"

on:
  pull_request_target:
    types:
      - opened
      - edited
      - synchronize

permissions:
  pull-requests: read

jobs:
  lint-pr:
    uses: majksa-actions/workflows/.github/workflows/lint-pr.yml@v1
```

### Deploy to portainer

Example usage:

```yml
name: "Deploy"

on:
  push:
    branches:
      - "env/**"

permissions:
  contents: read

jobs:
  deploy:
    uses: majksa-actions/workflows/.github/workflows/portainer-deploy.yml@v1
```

## Rust

### Testing

Example usage:

```yml
name: Test

on:
  push:
    branches:
      - "**"
  pull_request:
    branches:
      - "**"

jobs:
  rust:
    uses: majksa-actions/workflows/.github/workflows/rust-test.yml@v1
    secrets:
      CODECOV_TOKEN: ${{ secrets.CODECOV_TOKEN }}
```

### Publish to crates.io

Example usage:

```yml
name: Publish

on:
  push:
    tags:
      - "**"

permissions:
  contents: read

jobs:
  cargo:
    uses: majksa-actions/workflows/.github/workflows/rust-publish.yml@v1
    secrets:
      CARGO_REGISTRY_TOKEN: ${{ secrets.CARGO_REGISTRY_TOKEN }}
```
