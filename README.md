# composer-test-pr

An action that shows the code necessary to be added to composer in order to test a PR

## Example

You can use it as a Github Action like this:

_.github/workflows/how_to_test_pr.yml_
```yaml
name: How to test this PR

on:
    pull_request:
        types: [opened]

jobs:
    composer-test-pr:
        runs-on: ubuntu-latest
        steps:
          - name: Checkout
            uses: actions/checkout@v2

          - name: Composer Test PR
            uses: franmomu/composer-how-to-test-pr@master
            env:
              GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
