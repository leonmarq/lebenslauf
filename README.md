# Lebenslauf

German, one-page CV. Build with LuaLaTeX (recommended) or pdfLaTeX.
The source uses UTF-8, engine-appropriate Latin Modern fonts, German
hyphenation, PDF language/author/title metadata, and microtypography.

## Build

```sh
latexmk main.tex
```

The PDF and intermediate files are written to `build/`. To use pdfLaTeX:

```sh
latexmk -pdf main.tex
```

Required TeX packages: `iftex`, `fontspec` (LuaLaTeX/XeLaTeX), `fontenc`
and `lmodern` (pdfLaTeX), `babel` with German patterns, `geometry`,
`graphicx`, `xcolor`, `array`, `tabularx`, `titlesec`, `enumitem`,
`microtype`, and `hyperref`. Package versions are listed in `build/main.log`.
The included PDF artwork and QR image must remain alongside `main.tex`.

## Current TeX distribution and package updates

As of 20 October 2026, the current distribution is TeX Live 2026 and the
current stable LaTeX kernel release is 2026-06-01. Install TeX Live 2026
using the official installer, then use that installation's `tlmgr`:

```sh
tlmgr update --self --all
```

Do not run this against the existing Debian-managed TeX Live 2023 to attempt
a cross-release upgrade. Debian-managed installations are updated through
APT; their package versions follow the distribution repositories. A separate
upstream TeX Live installation is needed for current CTAN packages when the
OS repositories lag behind. Make sure its binary directory is first in PATH.

References:
- https://tug.org/texlive/quickinstall.html
- https://tug.org/texlive/upgrade.html
- https://tug.org/texlive/tlmgr.html
- https://latex-project.org/news/2026/06/01/issue43-of-latex2e-released/

## Verification

The modernized source was compiled with LuaLaTeX and pdfLaTeX on the available
TeX Live 2023 installation. Both produce a one-page CV. This verifies backward
compatibility; a TeX Live 2026 build has not yet been run. This project does not
claim PDF/UA conformance or enable experimental automatic PDF tagging.
