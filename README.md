# Laravel Cloud Deploy

This GitHub Action will trigger a deployment on Laravel Cloud.

## Usage

```yaml
name: Deploy

on:
  push:

jobs:
  deploy:
    name: Deploy
    runs-on: ubuntu-latest
    steps:
        - name: Deploy
          uses: nhedger/laravel-cloud-deploy@v1
          with:
            webhook: ${{ secrets.LARAVEL_CLOUD_WEBHOOK }}
