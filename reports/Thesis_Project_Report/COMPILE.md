# Compilation Instructions for Byakaron Thesis

## IMPORTANT: Use XeLaTeX Compiler

This thesis contains **Bangla (Bengali) script** which requires **XeLaTeX** compiler.

### On Overleaf:

1. Click the **Menu** button (top-left hamburger icon)
2. Scroll to **Settings**
3. Change **Compiler** from `pdfLaTeX` to **`XeLaTeX`**
4. Click **Recompile**

### Font Used

The template uses **Noto Sans Bengali** font which is pre-installed on Overleaf.

## Local Compilation

```bash
cd Thesis_Project_Report

# Use xelatex instead of pdflatex
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

### Required Font (Local)

Install Noto Sans Bengali from Google Fonts:
https://fonts.google.com/noto/specimen/Noto+Sans+Bengali

## Bangla Text Commands

The template defines `\bn{}` command for inline Bangla text:
```latex
\bn{বাংলা টেক্সট}
```

## Troubleshooting

| Error | Solution |
|-------|----------|
| Font not found | Ensure XeLaTeX compiler is selected |
| Unicode errors | Switch from pdfLaTeX to XeLaTeX |
| Missing packages | Run `tlmgr install polyglossia fontspec` |
