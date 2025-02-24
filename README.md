# Laravel Cloud Deploy

This GitHub Action will trigger a deployment on [Laravel Cloud](https://laravel.cloud).

Check out the [documentation](https://cloud.laravel.com/docs/deployments#deploy-hooks) to retrieve your webhook URL.
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
