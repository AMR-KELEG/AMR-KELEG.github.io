---
layout: post
title: A dump of useful Latex commands
date: 2023-05-18
description: A digital backup for latex packages/ commands that I found useful someday!
---

- `printlen`: To print the length of text width (6.3 for LREC template) - [documentation](https://ftp.cc.uoc.gr/mirrors/CTAN/macros/latex/contrib/printlen/printlen-doc.pdf)
- Use `\protect` before `\cite` to add citations into captions
- Use `\onslide` within `\begin{overprint}` for values replacing each others
- Square brackets are for optional values, curly braces are for obligatory ones
- Use `\phantom` to hide text or graphics while reserving the space
- For changing the header/footer
```
\usepackage{fancyhdr}
\begin{document}
\pagestyle{fancy}
\fancyhead{}
\fancyhead[LO,LE]{HEADER TEXT} \\ LO = Left Odd "page", LE = Left Even "page"
\end{document}
```
- For typing IPA characters, use a package called `tipa`
- This [webpage](https://jblevins.org/log/greek) has a list of greek symbols that is quite handy!
