---
layout: post
title: Arabic NLP resources
date: 2020-07-14
description: A non-exhaustive list of linguistic Arabic resources online
---

In this post, I will try to keep a list of any publically available resources that I can find. There are lots of Arabic resources that aren't used since they can't be easily found.

### Datasets

| Dataset | Description | Languages | Published|
|:-----:|:-----:|:-:|:----:|
| [LinCE](https://ritual.uh.edu/lince/home) | A NER dataset (stats?) and Language Identification corpus (each token in the sentence is annotated with the language MSA or EGA)| MSA & ARZ | 2020 |
| [MADAR](https://camel.abudhabi.nyu.edu/madar-shared-task-2019/)| A set of setences manually translated by professional translators from different cities into different dialects from Travel (Subtask 1) and Twitter (Substask 2) data | 26 different dialects from different Arabian cities including MSA| 2019 |
| [CALM](http://linguistics.byu.edu/thesisdata/CALMcorpusDownload.html) ||ARZ|2019|
| [HARD](https://github.com/elnagara/HARD-Arabic-Dataset), [paper](https://link.springer.com/chapter/10.1007/978-3-319-67056-0_3)|93700 hotel reviews in Arabic language collected from Booking.com|MSA & Dialects|2018|
| [ASTD](https://github.com/mahmoudnabil/ASTD)| Arabic Sentiment Tweets Dataset contains over 10k Arabic sentiment tweets classified into four classes subjective positive, subjective negative, subjective mixed, and objective | NA | 2015 |
| [Arabic sentiment analysis](https://archive.ics.uci.edu/ml/datasets/Twitter+Data+set+for+Arabic+Sentiment+Analysis)| A two label dataset of Arabic tweets (2000 positive and 2000 negative) | NA | 2013 |
| [LABR](https://github.com/mohamedadaly/LABR)| Large Scale Arabic Book Reviews Dataset contains over 63,000 book reviews in Arabic collected from goodreads.| NA | 2013 |
| [ANERCorp](https://github.com/EmnamoR/Arabic-named-entity-recognition) | A relatively old Arabic NER (Person, Location, Organisation, Miscellaneous) corpus of 150K tokens (11% are entities) | NA | 2007 |
| [AQMAR](https://www.cs.cmu.edu/~ark/ArabicNER/), [Topcode challenge](https://www.topcoder.com/challenges/f3cf483e-a95c-4a7e-83e8-6bdd83174d38) | Wikipedia-based NER dataset | ARA | 2012 |
|---|---|---|---|
{:.table-borders}

<hr>

### Tools

| Tool name | Description | Programming language | Languages | Published |
|:-:|:-:|:-:|:-:|:-:|
| [stanza](https://stanfordnlp.github.io/stanza/) | TBC (A tool for NER and POS? for multiple languages including Arabic), uses AQMAR and PADT | python (pytorch) | MSA & EGA | 2020 (Christopher D. Manning.) |
|---|---|---|---|---|
{:.table-borders}

<!---
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
-->

<hr>

### Arabic related workshops
- WANLP: [WANLP2020](https://sites.google.com/view/wanlp-2020)
- OSACT: [OSACT4](http://edinburghnlp.inf.ed.ac.uk/workshops/OSACT4/)

<hr>

### Misc. resources
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
- [CNN and BBC data](https://sourceforge.net/projects/ar-text-mining/files/)
- [Tunisian dialect resources repo](https://github.com/chiraz/Definitive-Guide-of-Tunisian-Dialect-NLP-Resources)
- [Random Arabic datasets](https://discuss.huggingface.co/t/open-to-the-community-one-week-team-effort-to-reach-v2-0-of-hf-datasets-library/2176/10)
- [NYU-AD](https://nyuad.nyu.edu/en/research/faculty-labs-and-projects/computational-approaches-to-modeling-language-lab/resources.html)
- [ELXIR](https://github.com/otakar-smrz/elixir-fm/blob/master/Python/ElixirFM/README.ipynb): A program able to inflect words?
