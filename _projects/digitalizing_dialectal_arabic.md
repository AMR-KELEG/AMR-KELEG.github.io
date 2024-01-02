---
layout: page
title: Digitalization of Dialectal Arabic documents
description: an effort to increase the representation of Digitalized Arabic Corpora 
importance: 2
layout: post
date: 2024-01-01
---

### Case Study: Parallel Tunisian Constitution Corpus (PTCC)
Official and legal documents in Arab countries, such as the constitution, are primarily issued in Arabic, and can sometimes be available in other languages such as: English and French. It is extremely rare to find these documents written in a variant of Dialectal Arabic.

On reading the [TunBERT: Pretrained Contextualized Text Representation for Tunisian Dialect](https://arxiv.org/abs/2111.13138) paper, I found that the 2014 Tunisian Constitution was translated in Tunisian Arabic, as an attempt to make it more accessible to the Tunisians.

I managed to find two versions of the constitution as pdf files written in [MSA](https://upload.wikimedia.org/wikipedia/commons/7/78/Constitution_Tunisienne_2014.pdf) and [Tunisian Arabic](https://www.babnet.net/rttdetail-84167.asp). While text embedded in **epub** files can be automatically parsed (e.g.: using [EbookLib](https://pypi.org/project/EbookLib/)), text embedded in **pdf** files pose a challenge. Even a daunting manual copying of text from **pdf** files is not possible, as Arabic text tend to get mingled, as shown below if the following text, representing the first article, is copied from the pdf: "الفصل 1. تونس دولة حرّة مسْتقلّة ذات سيادة يعني حتّى دولة وإلآ سلطة أخرى ما تتدخل فيها, وتونس مسلمة ولوغتها العربية معنتها أغلبية شعبها مسلم ولوغتو العربية ونظامها جمهوري يعني الشعب هو إلي ينتخب رئيس الجمهورية موش كيما المُلوكية يكون فيها الحكم بالوراثة. الفصل هاذا ما إنجّموش نبدلوه."

```
الفصل
. 1
تونس دولة حرّ ة م
ة ذات سيادة يعني حتّ قلّ تْ سْ
ى دولة
إلاّ و
سلطة
تْ أخرى ما ت
دخّل
، فيها
وتونس مسلمة
لوغتها العربية و
معنتها
أغلبية شعبها
مسلم ولوغتو العربية ونظامها
ج
مهوري يعني الشّعب
إ لّ هو
ي ينتخب رئيس الجمهورية
موش كيما الم لوكية يكون فيها الحكم
. 
```

Another option is using Optical Character Recognition (OCR) to transform images of text into machine-readable text. [Tesseract](https://github.com/tesseract-ocr/tesseract) is an open-source OCR library. The library has a [python interface](https://pypi.org/project/pytesseract/) and supports [Arabic](https://github.com/tesseract-ocr/tessdata/blob/main/ara.traineddata). I used **PyTesseract** as per the [following instructions](https://github.com/AMR-KELEG/Digitalizing-Arabic-Documents), followed by some ad-hoc script for aligning the articles extracted from the two pdf files. The aligned sentences form **Parallel Tunisian Constitution Corpus (PTCC)** which can be accessed through: [https://huggingface.co/datasets/AMR-KELEG/PTCC](https://huggingface.co/datasets/AMR-KELEG/PTCC)
