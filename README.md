# ParaPy Application Test GitHub Action

![ParaPy Logo](https://s3-eu-west-1.amazonaws.com/parapy-cache/wp-content/uploads/2016/12/22134017/Logo_margin.png)

This GitHub Action is provided by [ParaPy](https://parapy.nl) to easily test ParaPy applications.

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
            parapy-pypi-username: ${{ vars.PARAPY_PYPI_USERNAME }}
            parapy-pypi-password: ${{ secrets.PARAPY_PYPI_PASSWORD }}
```
