# Awnon CV

This repository contains my professionally crafted Curriculum Vitae (CV), written in LaTeX. Two variants are maintained:

| File | Description | Engine |
|------|-------------|--------|
| [`general CV/main.tex`](general%20CV/main.tex) | General-purpose CV | XeLaTeX |
| [`Academic CV/teaching_cv.tex`](Academic%20CV/teaching_cv.tex) | Teaching-focused CV for academic roles | pdflatex |

## Features

- Clean, professional layout designed for readability and impact.
- Two CV variants: a **General CV** and a **Teaching CV** for online adjunct/college roles.
- Organized sections covering education, research experience, work experience, publications, presentations, technical skills, honors, and more.
- **FontAwesome 5** and **Academicons** icons in the General CV (requires XeLaTeX).
- Bibliography managed via **BibLaTeX** with IEEE style, author name highlighting, and automatic sorting by year.
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
│   ├── teaching_cv.tex   # Teaching CV source
│   └── .latexmkrc        # pdflatex config
└── .github/workflows/
    └── build-pdf.yml     # CI/CD workflow
```

## Building Locally

Both CVs use `latexmk` with per-project `.latexmkrc` files — no manual engine flags needed.

**General CV** (XeLaTeX + Biber):
```bash
cd "general CV"
latexmk -outdir=out main.tex
```

**Teaching CV** (pdflatex + Biber):
```bash
cd "Academic CV"
latexmk -outdir=out teaching_cv.tex
```

Output PDFs are written to the `out/` subdirectory in each folder.

> **VS Code users:** The LaTeX Workshop extension will build automatically on save using the `.latexmkrc` in each project folder.

## CI/CD

A GitHub Actions workflow ([`build-pdf.yml`](.github/workflows/build-pdf.yml)) builds both CVs on every push to `main` and publishes the PDFs to the [latest GitHub Release](https://github.com/awnonbhowmik/Awnon-CV/releases/tag/latest):

| Release File | Source |
|---|---|
| `Awnon-Bhowmik-General-CV.pdf` | `general CV/main.tex` |
| `Awnon-Bhowmik-Teaching-CV.pdf` | `Academic CV/teaching_cv.tex` |

## Reference Sites

- [Hansen Lab CV Bibliography](http://www.hansenlab.org/cv_bibliography_tex)
- [StackExchange: Author Name Formatting with BibTeX](https://tex.stackexchange.com/questions/29381/is-it-normal-for-bibtex-to-replace-similar-author-names-with)
- [Overleaf: Biblatex Bibliography Styles](https://www.overleaf.com/learn/latex/Biblatex_bibliography_styles)
- [FontAwesome 5 Documentation](http://mirrors.ibiblio.org/CTAN/fonts/fontawesome5/doc/fontawesome5.pdf)

## License

© 2026 Awnon Bhowmik. All rights reserved.

No part of this project may be reproduced, distributed, or transmitted in any form or by any means without the prior written permission of the author.
