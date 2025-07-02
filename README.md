# Template Skripsi Gunadarma LaTeX


- file hypenation koreksi made-hypen.tex harus diletakkan pada direktori yang setingkat. File ini bisa saja diubah ditambahi bila menemukan pemenggalan yang tidak tepat.

- Pada bagian Abstraksi hati-hati terutama yang ada code "LaTeX" (ERT berwarna merah).  Beberapa paragraf pada bagian abstraksi memiliki spasi single.
  Pada bagian yang ada \noindent setelahnya ada spasi 

- Spasi dokumen ini adalah one-and-half (saya memutuskan tidak pakai double, terlalu membuang kertas)


## VSCODE Settings
Put this setting in your settings.json vscode file
```json
"latex-workshop.kpsewhich.enabled": true,
  "latex-workshop.intellisense.package.enabled": true,
  "latex-workshop.latex.recipes": [
    {
      "name": "latexmk (with bibtex)",
      "tools": [
        "latexmk"
      ]
    },
    {
      "name": "pdflatex -> bibtex -> pdflatex*2",
      "tools": [
        "pdflatex",
        "bibtex",
        "pdflatex",
        "pdflatex"
      ]
    },
  ],
  "latex-workshop.latex.tools": [
    {
      "name": "latexmk",
      "command": "latexmk",
      "args": [
        "-pdf",
        "-interaction=nonstopmode",
        "-synctex=1",
        "-file-line-error",
        "-bibtex",
        "-output-directory=out",
        "%DOC%"
      ]
    },
    {
      "name": "pdflatex",
      "command": "pdflatex",
      "args": [
        "-interaction=nonstopmode",
        "-synctex=1",
        "-file-line-error",
        "%DOC%"
      ]
    }
  ]
```