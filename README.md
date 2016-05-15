# xelatex-emoji
Emoji support for XeLaTeX documents

## Installation
Clone this repo into your [`texmf` folder](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages) or to the project folder. Clone emoji images named after the utf8 code - I recommend [EmojiOne](https://github.com/Ranks/emojione).

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

yields (using the great [EmojiOne](https://github.com/Ranks/emojione) images)

![example result](example/example.png)

### Image path

By default, xelatex-emoji expects the images to be in `images/utf8code.png`. You can change the path and extension by creating your own `\xelatexemojipath` command.

```tex
\newcommand{\xelatexemojipath}[1]{mycustompath/{#1}.pdf}
```

## Development

To generate the flag codes:

```
ruby bin/generate_flags.rb > xelatexemoji-flags.sty
```
