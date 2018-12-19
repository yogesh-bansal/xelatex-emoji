# xelatex-emoji
Emoji support for XeLaTeX documents

## Installation
Clone this repo into your [`texmf` folder](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages) or to the project folder.

```bash
# For Mac OS X:
$ mkdir -p ~/Library/texmf/tex/latex/local
$ cd ~/Library/texmf/tex/latex/local
$ git clone https://github.com/yogesh-bansal/xelatex-emoji.git
```

## Usage
Use the `xelatexemoji` package. Enjoy :)

## Example layout
```tex
\documentclass{article}

\usepackage{xltxtra}
\usepackage{xelatexemoji}

\setmainfont{Ubuntu}

\begin{document}

  Hello, 🌎. Lorem 😃 😄 😅 😆 ipsum dolor.

\end{document}
```

By default, xelatex-emoji expects the images to be in `images/utf8code.extension`. The package supports the same image formats (extensions) as XeLaTeX.

For example: If you insert the emoji 👌 (code `1F44C`) in your document, then the translation will work if the file `images/1F44C.pdf` or `images/1F44C.png` exist. If both exist, then XeLaTeX will use the “better” version `images/1F44C.pdf`.


## Development

To generate the flag codes:

```
ruby bin/generate_flags.rb > xelatexemoji-flags.sty
```
