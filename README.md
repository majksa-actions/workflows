# workflows

Stores reusable workflows that can be used from other actions.

- [General](#general)
  - [Release please](#release-please)
  - [Docker build and push](#docker-build-and-push)
  - [Lint PR](#lint-pr)
  - [Create deployment manifest from config](#create-deployment-manifest-from-config)
  - [Deploy to portainer](#deploy-to-portainer)
- [Rust](#rust)
  - [Testing](#testing)
  - [Publish to crates.io](#publish-to-cratesio)
  - [Publish documentation to GitHub Pages](#publish-documentation-to-github-pages)
- [TypeScript](#typescript)
  - [Publish GitHub Action](#publish-github-action)
  - [Vitest](#vitest)
  - [Biome](#biome)
    - [Check](#check)
    - [Format](#format)

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

### Create deployment manifest from config

Example usage:

```yml
name: Deploy

on:
  push:
    branches:
      - main

permissions:
  contents: write
  pull-requests: write

jobs:
  create-manifest:
    uses: majksa-actions/workflows/.github/workflows/create-deployment-manifest.yml@v1
    strategy:
      matrix:
        environment: ["prod", "dev"]
    with:
      environment: ${{ matrix.environment }}
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

### Publish documentation to GitHub Pages

Example usage:

```yml
name: Publish documentation

on:
  push:
    tags:
      - "**"

concurrency:
  group: "pages"
  cancel-in-progress: false

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  cargo:
    uses: majksa-actions/workflows/.github/workflows/rust-docs.yml@v1
```

## TypeScript

### Publish GitHub Action

```yml
name: Publish

on:
  release:
    types: [published, edited]

permissions:
  contents: write

jobs:
  build:
    uses: majksa-actions/workflows/.github/workflows/action-publish.yml@v1
```

### Vitest

```yml
name: Test

on:
  push:
  pull_request:

permissions:
  contents: write
  pull-requests: write

jobs:
  vitest:
    uses: majksa-actions/workflows/.github/workflows/vitest.yml@v1
```

### Biome

#### Check

```yml
name: Code Review

on:
  push:
  pull_request:

permissions:
  contents: read

jobs:
  biome:
    uses: majksa-actions/workflows/.github/workflows/biome-lint.yml@v1
```

#### Format

```yml
name: Code Review

on:
  pull_request:

permissions:
  contents: write
  pull-requests: write

jobs:
  biome:
    uses: majksa-actions/workflows/.github/workflows/biome-format.yml@v1
```
