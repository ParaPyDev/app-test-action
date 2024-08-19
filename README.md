# ParaPy Application Test GitHub Action

This GitHub Action is provided by ParaPy to easily release and deploy ParaPy applications, to your ParaPy Cloud.

Example workflow, utilizing the Action:

```yaml
name: Test your application
on: 
  [push]

jobs:
  application-testing:
    runs-on: ubuntu-latest
    steps:
    - uses: parapydev/app-test-action
        with:
            license-key: ${{ secrets.PARAPY_LICENSE_KEY_1 }}
            license-certificate: ${{ secrets.PARAPY_LICENSE_KEY_2 }}
            parapy-pypi-user-name: ${{ vars.PARAPY_PYPI_USERNAME }}
            parapy-pypi-password: ${{ secrets.PARAPY_PYPI_PASSWORD }}
```
