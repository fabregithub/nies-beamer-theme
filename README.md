# NIES beamer theme

<a href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.en">
  <img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-nd.png" style="width: 120px; height: auto;"/>
</a>

This is an unofficial LaTeX beamer theme for the National Institute for Environmental Studies. Only the 16:9 aspect ratio version is currently available.

### Features

- Custom NIES-branded title page, background, and frame title, driven by the
  artwork in `theme/images/` (`nies-bg.png` for normal frames, `nies-title.png`
  for the title frame).
- `\titleframe` — drop-in title frame with its own background, distinct from
  regular frames.
- `\ftnote{...}` — places a small gray citation/DOI note at a fixed position
  near the bottom of a slide (e.g. `\ftnote{\url{https://doi.org/...}}`).
- Numbered, navyblue `itemize`/`enumerate` lists (circle/sub-bullet markers for
  `itemize`; `1.`/`a.`/`i.` for `enumerate`), and a matching numbered
  `\tableofcontents` style.
- Frame number shown in the footer (`page X / Y`).
- Colour palette: `navyblue`, `turquoise`, `brightsky`, `lightred`, `violet`,
  `charcoal`, `gray`, `americanrose` (see `theme/beamercolorthemeNIES.sty`).

### Requirements

Compile with **XeLaTeX** — the theme relies on `fontspec`. The bundled
examples additionally use `Lato` (Latin text), `Lete Sans Math` (math), and
`Noto Sans JP`/`zxjatype` (Japanese text in `main-JP.tex`); install these fonts
or swap in your own via `\setmainfont`/`\setmathfont`/`\setjamainfont`.

### Installation
Retrieve nies-beamer via [GitHub](https://github.com/fabregithub/nies-beamer-theme) and place
it in a directory where LaTeX can find it.

You can check the integrity of your installation with

```
$ kpsewhich beamerthemeNIES.sty
```

### Usage

Using the theme is as simple as invoking beamer's `\usetheme`. Pass the `t`
documentclass option so frames (including `\tableofcontents`) are top-aligned
by default:

```latex
\documentclass[aspectratio=169,t]{beamer}

\usetheme{NIES}

\usepackage{lipsum}

\title{Some slides with the NIES beamer theme}
\subtitle{This is a dummy subtitle}
\author{NIES Researcher}

\begin{document}

\titleframe % Title frame different from the others

\begin{frame}
\frametitle{A first test frame}
\lipsum
\end{frame}

\end{document}
```
See
[here](/example/main-EN.tex)
(or the Japanese variant, [main-JP.tex](/example/main-JP.tex)) for a more
verbose example, including lists, blocks, a two-column layout, and an
outline frame built with `\tableofcontents`.

### File structure

```
nies-beamer-theme/
├── theme/
│   ├── beamerthemeNIES.sty        % entry point, loaded via \usetheme{NIES}
│   ├── beamercolorthemeNIES.sty   % colour palette
│   ├── beamerfontthemeNIES.sty    % fonts/sizes for titles, frame titles, etc.
│   ├── beamerinnerthemeNIES.sty   % itemize/enumerate/TOC styling
│   ├── beamerouterthemeNIES.sty   % backgrounds, footline, frametitle, \titleframe, \ftnote
│   └── images/                    % nies-bg.png, nies-title.png
└── example/
    ├── main-EN.tex
    └── main-JP.tex
```

### License

This software is published under the [CC BY-NC-ND 4.0  license](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.en).