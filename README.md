# marp-gh-page-action
[![LICENSE](https://img.shields.io/github/license/timo-reymann/marp-gh-page-action)](https://github.com/timo-reymann/marp-gh-page-action/blob/main/LICENSE)

<p align="center">
  <img width="300" src="https://avatars.githubusercontent.com/u/54465427?v=4">
  <br />
  GitHub Action to build a marp repository and publish to github pages
</p>

## Required for usage

- You have one or no asset folder
- Export as HTML must be running
- GitHub Pages enabled for the repo
- One presentation per repo: `index.md`

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
