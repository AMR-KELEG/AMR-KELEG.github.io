---
layout: page
title: Resources
permalink: /resources/
description: 
nav: true
---

## Arabic Level of Dialectness (ALDi)
* <u>Sentence-ALDi</u>
  * A model that predicts the Arabic Level of Dialectness (ALDi) of sentence-like units. The ALDi score is in the range [0, 1], where 0 implies pure Modern Standard Arabic (MSA) and 1 means highly dialectal language.
  * **Model:** [https://huggingface.co/AMR-KELEG/Sentence-ALDi](https://huggingface.co/AMR-KELEG/Sentence-ALDi)
  * **Demo:** [https://huggingface.co/spaces/AMR-KELEG/ALDi](https://huggingface.co/spaces/AMR-KELEG/ALDi)
  * **Baseline (Token Dialect Identification):** [https://huggingface.co/AMR-KELEG/ALDi-Token-DI](https://huggingface.co/AMR-KELEG/ALDi-Token-DI)
  * **Dataset:** The model was fine-tuned on the AOC-ALDi dataset - [https://github.com/AMR-KELEG/ALDi/raw/master/data/AOC-ALDi.tar.gz](https://github.com/AMR-KELEG/ALDi/raw/master/data/AOC-ALDi.tar.gz)
  * **Papers:**
    * [Amr Keleg, Sharon Goldwater, and Walid Magdy. 2023. ALDi: Quantifying the Arabic Level of Dialectness of Text.](https://aclanthology.org/2023.emnlp-main.655/) In Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing, pages 10597–10611, Singapore.
    * [Amr Keleg, Walid Magdy, and Sharon Goldwater. 2024. Estimating the Level of Dialectness Predicts Inter-annotator Agreement in Multi-dialect Arabic Datasets.](https://aclanthology.org/2024.acl-short.69/) In Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers), pages 766–777, Bangkok, Thailand.

<br/>

## Arabic Dialect Identification (ADI)

* <u>Multilabel Arabic Dialect Identification (MLADI) Dataset and Leaderboard</u>
  * **Dataset Description:**  Each sample's validity in 11 different country-level dialects is manually assessed by 3 annotators from each country. Each sample is also labeled for its Level of Dialectness.
  * **Dataset Access Form:** [https://forms.gle/gdgTToxG2tH5xT27A](https://forms.gle/gdgTToxG2tH5xT27A)
  * **Leadeboard:** [https://huggingface.co/spaces/AMR-KELEG/MLADI](https://huggingface.co/spaces/AMR-KELEG/MLADI)
  * **Baseline Model:** [https://huggingface.co/AMR-KELEG/NADI2024-baseline](https://huggingface.co/AMR-KELEG/NADI2024-baseline)
  * **Leaderboard Description:** The MLADI leaderboard serves as a public interface for benchmarking ADI models using an 'extended version' of the NADI 2024 test set, the first multi-label country-level ADI dataset.
  * **Papers:**
    *  [Amr Keleg, Sharon Goldwater, Walid Magdy. 2025. Revisiting Common Assumptions about Arabic Dialects in NLP](https://arxiv.org/abs/2505.21816) In Proceedings of ACL 2025.
    *  [Muhammad Abdul-Mageed, Amr Keleg, AbdelRahim Elmadany, Chiyu Zhang, Injy Hamed, Walid Magdy, Houda Bouamor, and Nizar Habash. 2024. NADI 2024: The Fifth Nuanced Arabic Dialect Identification Shared Task.](https://aclanthology.org/2024.arabicnlp-1.79/) In Proceedings of the Second Arabic Natural Language Processing Conference, pages 709–728, Bangkok, Thailand.

<br/>

* <u>Error Analysis for the predictions of a SOTA single-label ADI model.</u>
  * **Description:** Recruited speakers from 7 different Arab countries to check if the model's predictions for the system's errors are also valid.
  * **Annotations:** [https://github.com/AMR-KELEG/ADI-under-scrutiny/blob/master/data/annotations.tar.gz](https://github.com/AMR-KELEG/ADI-under-scrutiny/blob/master/data/annotations.tar.gz)
  * **Model:** [https://huggingface.co/AMR-KELEG/ADI-NADI-2023](https://huggingface.co/AMR-KELEG/ADI-NADI-2023)
  * **Original Evaluation Dataset:** [QADI's test set](https://github.com/qcri/QADI/tree/master/testset)
  * **Paper:** [Amr Keleg and Walid Magdy. 2023. Arabic Dialect Identification under Scrutiny: Limitations of Single-label Classification](https://aclanthology.org/2023.arabicnlp-1.31/). In Proceedings of ArabicNLP 2023, pages 385–398, Singapore (Hybrid).

## Factual Knowledge
* <u>DLAMA-v1</u>
  * **Dataset Description:** benchmark of factual triples from three pairs of contrasting cultures having a total of 78,259 triples from 20 relation predicates. The three pairs comprise facts representing the (Arab and Western), (Asian and Western), and (South American and Western) countries respectively.
  * **Link on HF datasets:** [https://huggingface.co/datasets/AMR-KELEG/DLAMA-v1](https://huggingface.co/datasets/AMR-KELEG/DLAMA-v1)
  * **Codebase:** [https://github.com/AMR-KELEG/DLAMA](https://github.com/AMR-KELEG/DLAMA)
  * **Paper:** [Amr Keleg and Walid Magdy. 2023. DLAMA: A Framework for Curating Culturally Diverse Facts for Probing the Knowledge of Pretrained Language Models.](https://aclanthology.org/2023.findings-acl.389/) In Findings of the Association for Computational Linguistics: ACL 2023, pages 6245–6266, Toronto, Canada.
