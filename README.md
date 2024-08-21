# ParaPy Application Test GitHub Action

This GitHub Action is provided by ParaPy to easily test ParaPy applications.

Example workflow, utilizing the Action:

```yaml
name: Test your application
on: 
  [push]

jobs:
  application-testing:
    runs-on: ubuntu-20.04
    steps:
    - uses: parapydev/app-test-action
        with:
            license-key: ${{ secrets.PARAPY_LICENSE_KEY_1 }}
            license-certificate: ${{ secrets.PARAPY_LICENSE_KEY_2 }}
            parapy-pypi-user-name: ${{ vars.PARAPY_PYPI_USERNAME }}
            parapy-pypi-password: ${{ secrets.PARAPY_PYPI_PASSWORD }}
```
