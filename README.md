# Github Actions Workflow - Open Policy Agent with Terraform

## Inputs
* `opa_version`: open policy agent version (default: 0.33.1, optional)
* `tf_version`: terraform version (default: 1.0.0, optional)
* `policy_filename`: opa policy filename (default: empty, if not exists the workflow will skip the evaluate step)

## How to use

In your caller workflow, with default inputs:
...

jobs:
  my-caller-workflow:
    uses: edsoncelio/workflow-opa-terraform/.github/workflows/opa-terraform.yml@main
```

In your caller workflow, with custom inputs:
...

jobs:
  my-caller-workflow:
    uses: edsoncelio/workflow-opa-terraform/.github/workflows/opa-terraform.yml@main
    with:
        opa_version: v0.33.0
```