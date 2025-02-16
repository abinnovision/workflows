# abinnovision/workflows

This repository contains a collection of GitHub Actions Workflows. Most of them
are designed to be used within the
[abinnovision](https://github.com/abinnovision) organization.

## Workflows

These are the currently available workflows:

- [release-v2](./.github/workflows/release-v2.yaml): Release workflow for all
  repositories using release-please.
- ~~[release-please](./.github/workflows/release-please.yaml): Wrapper around
  release-please, which takes care about acquiring the GitHub App token.~~ (
  Deprecated)

## Usage

All workflows within this repository can be used in other repositories like
this:

```yaml
# ...
jobs:
  <job>:
    uses: abinnovision/workflows/.github/workflows/<workflow>.yaml@main
    with:
      input-key: input-value
    secrets:
      secret-key: secret-value
# ...
```

Currently, there is no versioning of these workflows. The `main` branch is used
as ref.
Breaking changes to workflows will result in new workflow files.
