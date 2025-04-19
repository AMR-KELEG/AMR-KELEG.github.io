---
layout: post
title: The difficulties of typing Arabic text in latex
date: 2023-09-24
description: TL;DR - Use babel with pdflatex!<br> (Last Updated - April 2025)
---

Arabic across different other languages has its own script, which requires the usage of fonts that are not included by default in latex. A font is the way a specific character is rendered into the output pdf document.

An [overleaf page](https://web.archive.org/web/20230718130842/https://www.overleaf.com/learn/latex/Arabic)[^1] recommends the usage of `polyglossia`, which requires changing the compiler to either `XeLaTeX` or `LuaLaTeX`. Additionally, it mentions the following: "Many authors are mandated to use pdfLaTeX due to requirements of their workflow, but if you are able to choose the LaTeX compiler, the modern approach to typesetting Arabic is to use XeLaTeX (XeTeX engine) or LuaLaTeX (LuaHBTeX engine).". As a LaTeX beginner, I did not think I have any mandates that would enforce me to refrain from using another compiler, so I happily used the `polyglossia` solution.

## The arXiv issue
I was quite happy with following the recommendation of using `polyglossia`. However, I realized that arXiv does not support neither `XeLaTeX` nor `LuaLaTeX`. Consequently, one needs to use the `pdfLaTeX` compiler which does not support the `polyglossia` pacakge. Moreover, the site does allow directly uploading pdfs if they were compiled from latex. Impressively, arXiv can detect that an pdf is compiled from latex sources, and disallows the submission.

## The babel solution
The solution I found to type Arabic text in English documents is to use the `babel` package. The package is supported by `pdfLaTeX`, which means that arXiv will be able to compile it. As far as I remember, the `arabtex` package has some limitations that I forgot about 😌. The `babel` solution entails two simple steps: 

* First, the package need to be included <br> `\usepackage[arabic,USenglish]{babel}`

* Then, to type Arabic text, you need to use a `\AR` scope as follows <br> `This is an example of Arabic text \AR{مثال بالعربية} within English text!`

* And voilà!<br>
<img src="https://raw.githubusercontent.com/AMR-KELEG/AMR-KELEG.github.io/master/assets/img/arabic_latex.png" alt="compiled text!">

## Transliterating Arabic words
Given that Arabic has its own script, it is sometimes useful to transliterate Arabic words to the Latin script. The [Habash-Soudi-Buckwalter (HSB)](https://link.springer.com/chapter/10.1007/978-1-4020-6046-5_2) scheme provides a one-to-one mapping between Arabic and Latin characters. Additionally, [camel_tools](https://camel-tools.readthedocs.io/en/v1.5.5/cli/camel_transliterate.html) provides a handy interface for transliteration as a CLI tool or a Python module.

**Example:** `$ echo "راجل" | camel_transliterate -s "ar2hsb"`

* **Comment (1)** The scheme is designed for MSA, so the latin transliteration would look odd for characters that are pronunced differently in a dialect. For example above, the transliteration is `rAjl`, where `ج` is transliterated as an MSA `j` and not as a dialectal `g` for Egyptian Arabic.<br>
 
* **Comment (2)** The HSB scheme uses some non-ASCII characters, which can not be rendered by default in a latex document. I either had to type them as greek letters (i.e., adding `greek` to babel, and encapsulating the letters in `\foreignlanguage{greek}{GREEK_LETTER}`). Other letters are written using the [tipa](https://ctan.org/pkg/tipa?lang=en) latex package.

## Further notes
* The rendered Arabic text looks bold and with a bit larger font size compared to the latin counterpart. Hence, I defined a new command `\ARA` to slightly improve on these issues: <br> `\newcommand{\ARA}[1]{\begin{footnotesize}\AR{#1}\end{footnotesize}}`

* The `\AR` command causes rendering errors when added to captions. You should add `\protect` before it to fix the errors.

* Given that Arabic is a right-to-left language, it is preferrable to have Arabic text oriented to the right in latex tables. Assuming the column is `p`, then adding `>{RaggedLeft}` before the `p` will render Arabic in an appealing way.

* Typing Arabic using babel causes some issues with referencing `\chapter{}` constructs. The following snippet copied from a [stackexchange answer](https://tex.stackexchange.com/questions/238225/arabic-support-in-babel-mess-up-chapter-referencing/238442#238442) fixed this:
{% raw %}
    ```

    \usepackage[arabic,main=english]{babel}
    \makeatletter
    \def\@part[#1]#2{%
    \addtocontents{toc}{\xstring\select@language{\main@Arabi@language}}%
    \if@rl\SAV@@part[\textRL{#1}]{\textRL{#2}}%
    \else\SAV@@part[\textLR{#1}]{\textLR{#2}}%
    \fi} 

    \def\@spart#1{%
    \addtocontents{toc}{\xstring\select@language{\main@Arabi@language}}%
    \if@rl\SAV@spart{\textRL{#1}}%
    \else\SAV@spart{\textLR{#1}}%
    \fi}  

    \def\@chapter[#1]#2{%
    \addtocontents{toc}{\xstring\select@language{\main@Arabi@language}}%
    \if@rl\SAV@@chapter[\textRL{#1}]{\textRL{#2}}%
    \else\SAV@@chapter[\textLR{#1}]{\textLR{#2}}%
    \fi} 

    \def\@schapter#1{%
    \addtocontents{toc}{\xstring\select@language{\main@Arabi@language}}%
    \if@rl\SAV@schapter{\textRL{#1}}%
    \else\SAV@schapter{\textLR{#1}}%
    \fi}  
    \makeatother
    ```
{% endraw %}

<hr/>

[^1]: The version of 18th of July 2023.