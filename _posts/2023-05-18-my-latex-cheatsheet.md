---
layout: post
title: A dump of useful Latex commands
date: 2023-05-18
description: A (non-exhaustive) digital backup for latex packages/ commands that I found useful someday! (Last updated - October 2025)
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
- To insert a full citation in a paper (thesis!) while using natbib:
```
\usepackage{bibentry}
\nobibliography*
```
Then, use `\bibentry{ENTRY_KEY}`.
- More information about the different bib entries: [here](https://bibtex.eu/types/)
- Use `\autoref{}` instead of `\ref{}` to anchor the whole reference and not just the number!
- The `changes` package is useful for tracking changes
```
\usepackage{changes}

% The following lines are only needed for changing the colors!
\definecolor{addedcolor}{RGB}{0,128,0} % Green for added
\definecolor{deletedcolor}{RGB}{255,69,0} % Orange for deleted
\setaddedmarkup{\color{addedcolor}\uline{#1}}
\setdeletedmarkup{\color{deletedcolor}\sout{#1}}


...

\begin{document}
    \added{TEXT ADDED} \replaced{NEW}{OLD} \deleted{DELETE}
\end{document}

```
