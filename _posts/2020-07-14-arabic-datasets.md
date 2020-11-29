---
layout: post
title: Arabic NLP resources
date: 2020-07-14
description: A non-exhaustive list of linguistic Arabic resources online
---

## Datasets

| Dataset | Description | Languages | Published|
|-----|-----|-----|
| [LinCE](https://ritual.uh.edu/lince/home) | A NER dataset (stats?) and Language Identification corpus (each token in the sentence is annotated with the language MSA or EGA)| MSA & EGA | 2020 |
| [MADAR](https://camel.abudhabi.nyu.edu/madar-shared-task-2019/)| A set of setences manually translated by professional translators from different cities into different dialects from Travel (Subtask 1) and Twitter (Substask 2) data | 26 different dialects from different Arabian cities including MSA| 2019 |
| [Arabic sentiment analysis](https://archive.ics.uci.edu/ml/datasets/Twitter+Data+set+for+Arabic+Sentiment+Analysis)| A two label dataset of Arabic tweets (2000 positive and 2000 negative) | NA | 2013 |
| [ANERCorp](https://github.com/EmnamoR/Arabic-named-entity-recognition) | A relatively old Arabic NER (Person, Location, Organisation, Miscellaneous) corpus of 150K tokens (11% are entities) | NA | 2007 |
| [HARD](https://github.com/elnagara/HARD-Arabic-Dataset), [paper](https://link.springer.com/chapter/10.1007/978-3-319-67056-0_3)|93700 hotel reviews in Arabic language collected from Booking.com|MSA & Dialects|2018|
| [ASTD](https://github.com/mahmoudnabil/ASTD)| Arabic Sentiment Tweets Dataset contains over 10k Arabic sentiment tweets classified into four classes subjective positive, subjective negative, subjective mixed, and objective | NA | 2015 |
| [LABR](https://github.com/mohamedadaly/LABR)| Large Scale Arabic Book Reviews Dataset contains over 63,000 book reviews in Arabic collected from goodreads.| NA | 2013 |
| [CALM](http://linguistics.byu.edu/thesisdata/CALMcorpusDownload.html) ||||

## Tools

| Tool name | Description | Programming language | Languages | Published|
|-----|-----|-----|
| [stanza](https://stanfordnlp.github.io/stanza/) | TBC (A tool for NER and POS? for multiple languages including Arabic), uses AQMAR and PADT | python (pytorch) | MSA & EGA | 2020 (Christopher D. Manning.) |

- [PADT](http://ufal.mff.cuni.cz/padt/PADT_1.0/docs/index.html) An Arabic Treebank released in 2004!
and [PADT](https://github.com/UniversalDependencies/UD_Arabic-PADT)

- [AQMAR](https://github.com/nschneid/arabic-tagger) An arabic sequence tagger!
and dataset http://www.cs.cmu.edu/~ark/ArabicNER/

- [Multidialect BERT](https://huggingface.co/bashar-talafha/multi-dialect-bert-base-arabic)

- Stanza's dependencies:

| Processor | Package |
------------|----------
| tokenize  | padt    |
| mwt       | padt    |
| pos       | padt    |
| lemma     | padt    |
| depparse  | padt    |
| ner       | aqmar   |

- Farasa supports MSA only
- Madamira supports MSA and ARZ
- CODA has a set of guidelines for annotation: https://sites.google.com/a/nyu.edu/coda/home

### Others
- [SA paper including names of some datasets](https://www.aclweb.org/anthology/C16-1228.pdf)
- [Speech Recognition](https://groups.csail.mit.edu/sls/downloads/adi17/) 
- [Speech Recognition](http://en.arabicspeechcorpus.com/)
- [Q&A from ask.fm](http://xminers.club/2017/07/22/arabic-qa-dataset/)
- [Hate speech](http://hatespeechdata.com/)
- [NER](https://fsalotaibi.kau.edu.sa/Pages-Arabic-NE-Corpora.aspx)
- [Arabizi - Taha](https://project-rbz.kmi.open.ac.uk/)
- [Other gazeteers](https://github.com/linuxscout/arabicnlptoolslist#gazetteers)
- [ARZ and dialectal resources (mainly for segmentation and POS)](http://alt.qcri.org/resources/da_resources/)
- [Arabic Morphological analysis](https://sourceforge.net/projects/aracomlex/)
- [Egyptian corpora](https://linguistics.byu.edu/thesisdata/CALMcorpusDownload.html)
- [CNN and BBC data](https://sourceforge.net/projects/ar-text-mining/files/)

### Arabic related workshops
- [WANLP - part of coling](https://sites.google.com/view/wanlp-2020)
- [OSACT - part of LREC](http://edinburghnlp.inf.ed.ac.uk/workshops/OSACT4/)
