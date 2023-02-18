# abinnovision/workflows

This repository contains a collection of GitHub Actions Workflows. This repository has been designed to provide a
comprehensive set of workflows that can be used to automate common development tasks and workflows.

## Workflows

These are the currently available workflows:

- [release-please](./.github/workflows/release-please.yaml): Wrapper around release-please, which takes care about
	acquiring the GitHub App token.

## Usage

All workflows within this repository can be used in other repositories like this:

```yaml
# ...
jobs:
  <job>:
    uses: abinnovision/workflows/.github/workflows/<workflow>.yaml@master
    with:
      input-key: input-value
    secrets:
      secret-key: secret-value
# ...
```

Currently, there is no proper versioning of these workflows, therefore we use `master` as ref. 
