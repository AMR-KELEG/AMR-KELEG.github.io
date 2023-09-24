---
layout: post
title: The difficulties of typing Arabic text in latex
date: 2023-09-24
description: TL;DR - Use babel with pdflatex!
---

Arabic across different other languages has its own script, which requires the usage of fonts that are not included by default in latex. A font is the way a specific character is rendered into the output pdf document.

An [overleaf page](https://web.archive.org/web/20230718130842/https://www.overleaf.com/learn/latex/Arabic)[^1] recommends the usage of `polyglossia`, which requires changing the compiler to either `XeLaTeX` or `LuaLaTeX`. Additionally, it mentions the following: "Many authors are mandated to use pdfLaTeX due to requirements of their workflow, but if you are able to choose the LaTeX compiler, the modern approach to typesetting Arabic is to use XeLaTeX (XeTeX engine) or LuaLaTeX (LuaHBTeX engine).". As a LaTeX beginner, I did not think I have any mandates that would enforce me to refrain from using another compiler, so I happily used the `polyglossia` solution.

## The arXiv issue
I was quite happy with following the recommendation of using `polyglossia`. However, I realized that arXiv does not support neither `XeLaTeX` nor `LuaLaTeX`. Consequently, one needs to use the `pdfLaTeX` compiler which does not support the `polyglossia` pacakge. Moreover, the site does allow directly uploading pdfs if they were compiled from latex. Impressively, arXiv can detect that an pdf is compiled from latex sources, and disallows the submission.

## The babel solution
The solution I found to type Arabic text in English documents is to use the `babel` package. The package is supported by `pdfLaTeX`, which means that arXiv will be able to compile it. As far as I remember, the `arabtex` package has some limitations that I forgot about 😌. The `babel` solution entails two simple steps: 

* First, the package need to be included <br> `\usepackage[arabic,USenglish]{babel}`

* Then, to type Arabic text, you need to use a `\AR` scope as follows <br> `This is an example of Arabic text \AR{مثال بالعربية} within English text!`

<img src="assets/img/arabic_latex.png" alt="compiled text!">

<hr/>

[^1]: The version of 18th of July 2023.