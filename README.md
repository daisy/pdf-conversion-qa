# pdf-conversion-qa

Repository for the **DAISY Consortium PDF Conversion Quality Framework**: a methodology for evaluating services that convert PDF documents to structured documents.

The framework is written as a [ReSpec](https://respec.org/docs/) document.

## Read the framework

- [Editors' Working Draft](https://ways2read.github.io/pdf-conversion-qa/framework/draft/) (latest)
- [Working Draft, 6 April 2026](https://ways2read.github.io/pdf-conversion-qa/framework/published/WD-20260406/) (published version)

## Layout

- `framework/draft/index.html`: the Editors' Working Draft (the live source).
- `framework/published/<STATUS>-<YYYYMMDD>/index.html`: frozen published versions, e.g. `WD-20260406`.
- `common/`: shared styles and the DAISY logo.

Pushes to `main` deploy the whole repository to GitHub Pages (`.github/workflows/static.yml`).

## Publishing a new version

1. Edit `framework/draft/index.html`.
2. Copy it to `framework/published/<STATUS>-<YYYYMMDD>/index.html`.
3. In the copy, set `subtitle`, `publishDate`, `thisVersion` and `previousVersion` in `respecConfig`, and change the relative `../../common` paths to `../../../common`.
4. Commit and push to `main`.

## Licence

CC0 1.0 Universal. See `LICENSE`.
