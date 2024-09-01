# gha-setup-python
This GitHub Action sets up a Python environment for use in workflows.

_*NOTE: This workflow is opinionated and meets the needs of its author. It is provided publicly as a reference for others to use and modify as needed.*_

This action will perform the following actions:
* Install Python
* Install Pipenv
* Generate Pipfile.lock if does not exist (only to be used in that run)
* Install dependencies

## Usage
To use this action, add the following step to your workflow:

```yaml
steps:
  - name: Checkout code
    uses: serverlessopsio/gha-setup-workspace@v1

  - name: Setup Python enviornment
    uses: serverlessopsio/gha-setup-python@v1
```

## Inputs
* python-version (_optional_): The version of Python to use. This action uses the version resolution employed by [actions/setup-python](https://github.com/actions/setup-python)

## Outputs
* python-version: he installed Python or PyPy version. Useful when given a version range as input.
* cache-hit: A boolean value to indicate a cache entry was found
* python-path: The absolute path to the Python or PyPy executable.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes.

## Contact
For any questions or support, please open an issue in this repository.

