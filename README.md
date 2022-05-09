# Thank You Action

Say thanks any time someone makes a new Pull Request on your repository!

## Getting Started
* Create a [Tenor API](https://tenor.com/gifapi/documentation) key and set it as a [Secret](https://docs.github.com/en/actions/reference/encrypted-secrets) on your GitHub repo
* Add a new GitHub Action workflow:
```
name: PR message

on:
  pull_request:
    types: [opened, edited, reopened]

jobs:
  pr-message:
    runs-on: ubuntu-latest
    steps:
      - uses: opeomotayo/pr-message-action@master
        with:
          GITHUB_TOKEN: ${{secrets.GITHUB_TOKEN}}
          TENOR_TOKEN: ${{secrets.TENOR_TOKEN}}
```

