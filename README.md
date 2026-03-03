# Awnon CV

This repository contains my professionally crafted Curriculum Vitae (CV), written in LaTeX. The CV showcases my academic background, research experience, and professional achievements in a structured and visually appealing format.

## Features

- Clean, elegant layout designed for readability and impact.
- Organized sections for education, research experience, work experience, publications, presentations, technical skills, and more.
- Incorporates **FontAwesome 5** and **Academicons** for iconography.
- Bibliography section managed via **BibLaTeX** for easy referencing.

## Getting Started

To compile the LaTeX source into a PDF, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/awnonbhowmik/Awnon-CV.git
   ```
2. Ensure you have an up-to-date LaTeX distribution installed (e.g., TeXLive or MikTeX).
3. Compile the LaTeX file:
   ```bash
   pdflatex main.tex
   biber main
   pdflatex main.tex
   pdflatex main.tex
   ```
## CI/CD

This repository includes a GitHub Actions workflow that automatically compiles the LaTeX source into a PDF on every push to `main`. The built PDF is uploaded as an artifact and published as a [GitHub Release](https://github.com/awnonbhowmik/Awnon-CV/releases/tag/latest).

## Reference Sites

Such beauty could not have been achieved, even with my masterful abilities in LaTeX. Therefore, I must give credit where it’s due. This CV's professional look and feel were inspired by the following resources:

- [Hansen Lab CV Bibliography](http://www.hansenlab.org/cv_bibliography_tex)
- [StackExchange: Author Name Formatting with BibTeX](https://tex.stackexchange.com/questions/29381/is-it-normal-for-bibtex-to-replace-similar-author-names-with)
- [Overleaf: Biblatex Bibliography Styles](https://www.overleaf.com/learn/latex/Biblatex_bibliography_styles)
- [FontAwesome 5 Documentation](http://mirrors.ibiblio.org/CTAN/fonts/fontawesome5/doc/fontawesome5.pdf)

## License

© 2025 Awnon Bhowmik. All rights reserved.

No part of this project may be reproduced, distributed, or transmitted in any form or by any means without the prior written permission of the author.
