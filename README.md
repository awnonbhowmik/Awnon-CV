# Awnon CV

This repository contains three professionally tailored LaTeX documents for different application contexts:

| File | Description | Engine |
|------|-------------|--------|
| [`general CV/main.tex`](general%20CV/main.tex) | General-purpose CV | XeLaTeX |
| [`Academic CV/main.tex`](Academic%20CV/main.tex) | Teaching-focused CV for academic roles | pdfLaTeX |
| [`SWE Resume/main.tex`](SWE%20Resume/main.tex) | Software engineering résumé | XeLaTeX |

## Features

- Clean, professional layout designed for readability and impact.
- Three targeted documents: a comprehensive **General CV**, an academic **Teaching CV**, and a concise **SWE Résumé**.
- Employer- and institution-first sections with related roles, assignments, and research projects nested under the same organization.
- Organized sections covering education, research experience, work experience, publications, presentations, technical skills, honors, and more.
- **FontAwesome 5** icons throughout the documents.
- General CV bibliography managed with **BibLaTeX** and **Biber**, using IEEE style, author-name highlighting, and reverse-chronological sorting.
- Per-project `.latexmkrc` files select the correct engine automatically.

## Repository Structure

```
Awnon-CV/
├── general CV/
│   ├── main.tex          # General CV source
│   ├── pub.bib           # Journal articles
│   ├── present.bib       # Conference presentations
│   └── .latexmkrc        # XeLaTeX config
├── Academic CV/
│   ├── main.tex          # Teaching CV source
│   └── .latexmkrc        # pdfLaTeX config
├── SWE Resume/
│   ├── main.tex          # Software engineering résumé source
│   └── .latexmkrc        # XeLaTeX config
└── .github/workflows/
    └── build-pdf.yml     # CI/CD workflow
```

## Building Locally

All three documents use `latexmk` with per-project `.latexmkrc` files, so no manual engine flags are needed.

**General CV** (XeLaTeX + Biber):

```bash
cd "general CV"
latexmk -outdir=out main.tex
```

**Teaching CV** (pdfLaTeX):

```bash
cd "Academic CV"
latexmk -outdir=out main.tex
```

**SWE Résumé** (XeLaTeX):

```bash
cd "SWE Resume"
latexmk -outdir=out main.tex
```

Output PDFs are written to the `out/` subdirectory in each folder.

> **VS Code users:** The LaTeX Workshop extension will build automatically on save using the `.latexmkrc` in each project folder.

## CI/CD

A GitHub Actions workflow ([`build-pdf.yml`](.github/workflows/build-pdf.yml)) detects which document sources changed and builds only the affected PDFs. Pull requests are validated without publishing; pushes to `main` publish successful builds to the [latest GitHub Release](https://github.com/awnonbhowmik/Awnon-CV/releases/tag/latest). A manual workflow run builds and publishes all three documents.

| Release File | Source |
|---|---|
| `Awnon-Bhowmik-General-CV.pdf` | `general CV/main.tex` |
| `Awnon-Bhowmik-Teaching-CV.pdf` | `Academic CV/main.tex` |
| `Awnon-Bhowmik-SWE-Resume.pdf` | `SWE Resume/main.tex` |

## Reference Sites

- [Hansen Lab CV Bibliography](http://www.hansenlab.org/cv_bibliography_tex)
- [StackExchange: Author Name Formatting with BibTeX](https://tex.stackexchange.com/questions/29381/is-it-normal-for-bibtex-to-replace-similar-author-names-with)
- [Overleaf: Biblatex Bibliography Styles](https://www.overleaf.com/learn/latex/Biblatex_bibliography_styles)
- [FontAwesome 5 Documentation](http://mirrors.ibiblio.org/CTAN/fonts/fontawesome5/doc/fontawesome5.pdf)

## License

© 2026 Awnon Bhowmik. All rights reserved.

No part of this project may be reproduced, distributed, or transmitted in any form or by any means without the prior written permission of the author.
