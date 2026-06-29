# Noriyuki Higashide CV TeX

This folder contains a LaTeX rebuild of the full CV.

## Build

Use XeLaTeX via latexmk:

```bash
cd cv_tex
latexmk -xelatex -interaction=nonstopmode cv.tex
```

The output is:

```text
cv.pdf
```

Clean temporary files:

```bash
latexmk -C cv.tex
```

## Notes

- The source keeps the information density of the original seven-page CV.
- Current affiliation and recent roles are updated from the supplied LinkedIn screenshots.
- Items marked `TODO` need confirmation before a final public CV:
  - exact Ph.D. completion dates, because the original CV and LinkedIn display differ;
  - official English name, date, and awarding body for `専攻科長賞`;
  - current institutional email and whether to remove the former UTokyo address.

