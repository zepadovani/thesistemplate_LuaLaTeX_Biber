### Compilation Instructions

Compile using: `lualatex` + `biber` + `lualatex` + `lualatex`.

### If using VSCode...
1. Install the LaTeX Workshop extension and configure the compilation file (Recipe).
2. Edit User Config JSON (Ctrl+Shift+P), and configure the recipes and set the one that compiles automatically on every save.

```[json]
   "latex-workshop.latex.clean.fileTypes": [
    "%DOCFILE%.aux",
    "%DOCFILE%.bbl",
    "%DOCFILE%.blg",
    "%DOCFILE%.idx",
    "%DOCFILE%.ind",
    "%DOCFILE%.lof",
    "%DOCFILE%.lot",
    "%DOCFILE%.out",
    "%DOCFILE%.toc",
    "%DOCFILE%.acn",
    "%DOCFILE%.acr",
    "%DOCFILE%.alg",
    "%DOCFILE%.glg",
    "%DOCFILE%.glo",
    "%DOCFILE%.gls",
    "%DOCFILE%.fls",
    "%DOCFILE%.log",
    "%DOCFILE%.fdb_latexmk",
    "%DOCFILE%.snm",
    "%DOCFILE%.synctex(busy)",
    "%DOCFILE%.synctex.gz(busy)",
    "%DOCFILE%.nav",
    "%DOCFILE%.vrb",
    "%DOCFILE%.synctex.gz"
  ],
  "[latex]": {
    "editor.formatOnPaste": false,
    "editor.suggestSelection": "recentlyUsedByPrefix"
  },
  "latex-workshop.latex.tools": [
    {
      "name": "lualatex",
      "command": "lualatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOC%"
      ]
    },
    {
      "name": "bibtex",
      "command": "bibtex",
      "args": [
        "%DOCFILE%"
      ]
    },
    {
      "name": "biber",
      "command": "biber",
      "args": [
        "%DOCFILE%"
      ]
    },
    {
      "name": "pdflatex",
      "command": "pdflatex",
      "args": [
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOC%"
      ]
    }
  ],
  "latex-workshop.latex.recipes": [
    {
      "name": "LuaLaTeX",
      "tools": [
        "lualatex"
      ]
    },
    {
      "name": "LuaLaTeX + Biber + LuaLaTeX x2",
      "tools": [
        "lualatex",
        "biber",
        "lualatex",
        "lualatex"
      ]
    },
    {
      "name": "LuaLaTeX + BibTeX + LuaLaTeX x2",
      "tools": [
        "lualatex",
        "bibtex",
        "lualatex",
        "lualatex"
      ]
    },
    {
      "name": "LuaLaTeX",
      "tools": [
        "lualatex"
      ]
    },
    {
      "name": "BibTeX",
      "tools": [
        "bibtex"
      ]
    },
    {
      "name": "Biber",
      "tools": [
        "biber"
      ]
    },
    {
      "name": "pdfLaTeX + BibTeX + pdfLaTeX x2",
      "tools": [
        "pdflatex",
        "bibtex",
        "pdflatex",
        "pdflatex"
      ]
    },
    {
      "name": "pdfLaTeX + Biber + pdfLaTeX x2",
      "tools": [
        "pdflatex",
        "biber",
        "pdflatex",
        "pdflatex"
      ]
    },

  ],
    "latex-workshop.latex.recipe.default":"LuaLaTeX + Biber + LuaLaTeX x2",
    "latex-workshop.latex.build.clearLog.everyRecipeStep.enabled": false,
    "latex-workshop.formatting.latex": "tex-fmt",
```

Also... consider installing LTeX as a spell/write check tool.

### Bibliography

Export your bibliography to a .bib using the Better BibTeX (Zotero) extension.

*Important: also check this...*: Check the gist and Zotero configuration to export the `.bib` file correctly using Better BibTeX. Refer to the gist here: [https://gist.github.com/zepadovani/cfa10ec91ac1192f3c6ea286e227d3d1](https://gist.github.com/zepadovani/cfa10ec91ac1192f3c6ea286e227d3d1). This is necessary to correctly export access dates for URLs.