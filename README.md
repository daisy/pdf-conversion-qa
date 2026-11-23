# pdf-conversion-qa

Repository for the **DAISY Consortium PDF Conversion Quality Framework**: a methodology for evaluating services that convert PDF documents to structured documents.

The framework is written as a [ReSpec](https://respec.org/docs/) document.

## Read the framework

- [Editors' Working Draft](https://ways2read.github.io/pdf-conversion-qa/framework/draft/) (latest)
- [Working Draft, 6 April 2026](https://ways2read.github.io/pdf-conversion-qa/framework/published/WD-20260406/) (published version)

## Test protocol

Conversion services are currently tested against a subset of the criteria in the framework. For each criterion, one reference PDF is designated so that results are comparable between services. The PDFs are in [`reference-materials/pdf`](reference-materials/pdf).

| Criterion | Success criteria | Reference PDF |
|---|---|---|
| Latin text (digital) | Text fidelity matches the ground truth Word document. | [Dog Information](reference-materials/pdf/Dog%20Information.pdf) |
| Latin text (scanned) | Text fidelity matches the ground truth Word document. | [Biodiversity register](reference-materials/pdf/Biodiversity%20register.pdf) |
| Reading order | Title, subtitle, authors, text columns, table, captions and footnotes flow logically. | [Uncovering the New Accessibility Crisis in Scholarly PDFs](reference-materials/pdf/Uncovering%20the%20New%20Accessibility%20Crisis%20in%20Scholarly%20PDFs.pdf) |
| Artifact removal | Running header, footer and watermarks are excluded. | [Biodiversity register](reference-materials/pdf/Biodiversity%20register.pdf) |
| Heading hierarchy | All headings are present, identified as such, and assigned H1, H2 etc. as per the ground truth Word document. | [Dog Information](reference-materials/pdf/Dog%20Information.pdf) |
| List structures | All lists are present, identified as such, and hierarchy matches the ground truth Word document. | [Dog Information](reference-materials/pdf/Dog%20Information.pdf) |
| Character styles | Bold and italic characters match the ground truth Word document. | [Biodiversity register](reference-materials/pdf/Biodiversity%20register.pdf) |
| Note formatting | Superscript numbers are retained as such, and the footnote and reference is included as a separate paragraph. | [Uncovering the New Accessibility Crisis in Scholarly PDFs](reference-materials/pdf/Uncovering%20the%20New%20Accessibility%20Crisis%20in%20Scholarly%20PDFs.pdf) |
| Equation conversion | All equations are present and accurately converted to digital math. | [Calculus excerpt](reference-materials/pdf/Calculus%20excerpt.pdf) |
| Image integrity | All main images are present, cropped appropriately and inserted in a logical place in the reading order. | [Biodiversity register](reference-materials/pdf/Biodiversity%20register.pdf) |
| Alt-text retention | Image alt text from the source PDF is present in the converted document. | [Dog Information](reference-materials/pdf/Dog%20Information.pdf) |
| Table conversion | All tables are present, well-structured and inserted in a logical place in the converted document. | [Uncovering the New Accessibility Crisis in Scholarly PDFs](reference-materials/pdf/Uncovering%20the%20New%20Accessibility%20Crisis%20in%20Scholarly%20PDFs.pdf) |

## Layout

- `framework/draft/index.html`: the Editors' Working Draft (the live source).
- `framework/published/<STATUS>-<YYYYMMDD>/index.html`: frozen published versions, e.g. `WD-20260406`.
- `reference-materials/pdf/`: the reference PDFs used for testing.
- `common/`: shared styles and the DAISY logo.

Pushes to `main` deploy the whole repository to GitHub Pages (`.github/workflows/static.yml`).

## Publishing a new version

1. Edit `framework/draft/index.html`.
2. Copy it to `framework/published/<STATUS>-<YYYYMMDD>/index.html`.
3. In the copy, set `subtitle`, `publishDate`, `thisVersion` and `previousVersion` in `respecConfig`, and change the relative `../../common` paths to `../../../common`.
4. Commit and push to `main`.

## Licence

CC0 1.0 Universal. See `LICENSE`.
