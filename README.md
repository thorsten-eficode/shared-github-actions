# shared-github-actions

Repo for all Github Actions created for testing.

## Usage in workflows

```
name: demo-workflow
on:
  workflow_dispatch:
jobs:
  demo:
    runs-on: ubuntu-20.04
    steps:
      - name: checkout shared repo
        uses: actions/checkout@v2
        with:
          repository: thorsten-eficode/shared-github-actions
          path: sharedGHA

      - name: Call a shared action
        id: actions-in-action
        uses: ./sharedGHA/actions-in-action
        with:
          argument-one: "one"
          argument-two: "two"
```

