# NIES beamer theme

<a href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.en">
  <img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-nd.png" style="width: 120px; height: auto;"/>
</a>

This is an unofficial LaTeX beamer theme for the National Institute for Environmental Studies. Only the 16:9 aspect ratio version is currently available.

### Installation
Retrieve nies-beamer via [GitHub](https://github.com/nschloe/ua-beamer) and place
it in a directory where LaTeX can find it.

You can check the integrity of your installation with

```
$ kpsewhich beamerthemeNIES.sty
```

### Usage

Using the theme is as simple as invoking beamer's `\usetheme`:

```latex
\documentclass[aspectratio=169]{beamer}

\usetheme{NIES}

\usepackage{lipsum}

\title{Some slides with a JECS beamer theme}
\subtitle{This is a dummy subtitle}
\author{Jecs Researcher}

\begin{document}

\titleframe % Title frame different from the others

\begin{frame}
\frametitle{A first test frame}
\lipsum
\end{frame}

\end{document}
```
See
[here](/example/main.tex)
for a more verbose example.

### License

This software is published under the [CC BY-NC-ND 4.0  license](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.en).