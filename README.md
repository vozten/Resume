# LaTeX Resume

This repository contains the LaTeX source for Volkan Ozten's resume. The
document is formatted as a compact, single-page US Letter resume.

## Contents

- `Resume.tex` - Resume content and formatting
- `Resume.pdf` - Compiled resume, when included
- `.gitignore` - Excludes local tools, private source material, and temporary
  LaTeX build files

The original reference PDF is intentionally excluded from version control.

## Requirements

Install a LaTeX distribution that provides `pdflatex`, such as:

- [MiKTeX](https://miktex.org/download) on Windows
- [TeX Live](https://www.tug.org/texlive/) on Linux
- [MacTeX](https://www.tug.org/mactex/) on macOS

The document uses the `geometry`, `enumitem`, `hyperref`, and `microtype`
packages. MiKTeX can install missing packages automatically during compilation.

## Build

From the repository root, run:

```powershell
pdflatex -interaction=nonstopmode -halt-on-error Resume.tex
pdflatex -interaction=nonstopmode -halt-on-error Resume.tex
```

The second pass resolves PDF metadata and hyperlinks. The generated document is
written to `Resume.pdf`.

With `latexmk`, the equivalent command is:

```powershell
latexmk -pdf Resume.tex
```

## Editing

Contact information and resume entries are in `Resume.tex`. Reusable commands
near the top of the file control section headings, roles, bullet indentation,
font sizing, and spacing.

Keep the resume to one page after making changes and review the compiled PDF
for line wrapping before publishing it.
