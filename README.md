# Pull resources from Translation Hosting

This Github Action uses [official SimpleLocalize CLI](https://github.com/simplelocalize/simplelocalize-cli).

Learn more: https://simplelocalize.io/docs/integrations/github-actions/

## Usage

```yml
name: 'My project'
on:
  push:
    branches: [ main, master ]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Pull translations
        uses: simplelocalize/pull@v2.1
        with:
          apiKey: <YOUR_API_KEY>
          pullPath: ./my-hosting/
          environment: latest # or 'production'
```
