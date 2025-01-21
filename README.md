# Deploy Tor Hidden Service with Apache2

A GitHub Action to deploy a website as a Tor hidden service using Apache2.

## Usage

To use this action, include the following in your workflow YAML file:

```yaml
name: Deploy Tor Hidden Service with Apache2

on:
  push:
    branches:
      - main # or your main branch name
  schedule:
    - cron: '0 */5 * * *'

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
    - name: Deploy Tor Hidden Service
      uses: anuragmuxui/deploy-tor-action@v1
      with:
        repository: ${{ github.repository }}
```

# Inputs

`repository`

Required The repository to clone. Default is `${{ github.repository }}`.

#Example

```name: Deploy Tor Hidden Service with Apache2

on:
  push:
    branches:
      - main # or your main branch name
  schedule:
    - cron: '0 */5 * * *'

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
    - name: Deploy Tor Hidden Service
      uses: anuragmuxui/deploy-tor-action@v1
      with:
        repository: ${{ github.repository }}
```

# Contributing

Contributions are welcome! Please open an issue or submit a pull request.
