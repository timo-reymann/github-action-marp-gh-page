# marp-gh-page-action
GitHub Action to build a marp repository and publish to github pages

## Required for usage

- You have one or no asset folder
- Export as HTML must be running
- GitHub Pages enabled for the repo
- One presentation per repo

## Usage

### with asset path, CNAME

```yaml
name: Build and Deploy
on: [push]
permissions:
  contents: write
jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: marp-gh-page
        uses: timo-reymann/marp-gh-page-action@v1
        with:
          domain: your-cname.example.com
          assets_path: images
```

### with no assets or CNAME

```yaml
name: Build and Deploy
on: [push]
permissions:
  contents: write
jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: marp-gh-page
        uses: timo-reymann/marp-gh-page-action@v1
```
