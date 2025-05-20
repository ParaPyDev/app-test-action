# ParaPy Application Test GitHub Action

<a href="https://parapy.nl" rel="ParaPy">![ParaPy](https://s3-eu-west-1.amazonaws.com/parapy-cache/wp-content/uploads/2016/12/22134017/Logo_margin.png)</a>

This GitHub Action is provided by [ParaPy](https://parapy.nl) to easily test ParaPy applications.

Example workflow (*with recommended usage of [secrets](https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions)/[vars](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/store-information-in-variables) usage for the different parameters*):

```yaml
name: Test your application
on: 
  [push]

jobs:
  application-testing:
    runs-on: ubuntu-22.04
    steps:
    - uses: parapydev/app-test-action
        with:
            license-key-1: ${{ secrets.PARAPY_LICENSE_KEY_1 }}
            license-key-2: ${{ secrets.PARAPY_LICENSE_KEY_2 }}
            parapy-pypi-username: ${{ vars.PARAPY_PYPI_USERNAME }}
            parapy-pypi-password: ${{ secrets.PARAPY_PYPI_PASSWORD }}
```

Please find descriptions for each parameter in the [pipeline specification](action.yml). And find extensive information to obtain each input parameter in the [ParaPy pipeline documentation](https://parapy.nl/docs/cloud/latest/application_developer/cicd_pipelines.html#pipeline-parameters).

