# The Security Attack Pattern (TTP) Recognition or Mapping Task
[![License](https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-lightgrey)](https://creativecommons.org/licenses/by/4.0/)
[![arXiv](https://img.shields.io/badge/arXiv-2109.05105-29d634.svg)](https://arxiv.org/abs/2401.10337)

We share in this repo the MITRE ATT&amp;CK mapping datasets, with `training`, `validation` and `test` splits. 
The datasets can be considered as an emerging and challenging `multilabel classification` NLP task, with over 600 hierarchical classes.

## Datasets

### TRAM

This dataset belongs to  [CTID](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/), is originally provided in this [github link](https://github.com/center-for-threat-informed-defense/tram). 

We processed the original files (i.e., gather from all sources, remove duplicates, resolve noisy / too short text and noisy labels, remap to MITRE ATTACK 12.0) and split  into training, dev and test splits.

### Procedure+

The dataset consists of two sub- datasets:
- Procedures: belong to [MITRE](https://github.com/mitre/cti/tree/master). All procedure examples from v12.0 are gathered and processed (i.e., remove markups) and split  into training, dev and test splits.
- Derived procedures: we crawled the URL references for each procedure example, and extract original text from the articles that are determined to be relevant to the procedure examples. The text are processed and split  into training, dev and test splits.

### Expert

The dataset is constructed from a large pool of high-quality threat reports.  
The rich textual paragraphs are carefully selected and then annotated by seasoned security experts.

The dataset is also pre-split into `training`, `dev` and `test` splits. There are ~4 labels per text in the `test` split, on average.

## Citations
If you use the datasets in your research or want to refer to our work, please cite:
```
@inproceedings{nguyen-srndic-neth-ttpm,
    title = "Noise Contrastive Estimation-based Matching Framework for Low-resource Security Attack Pattern Recognition",
    author = "Nguyen, Tu and Šrndić, Nedim and Neth, Alexander",
    booktitle = "Proceedings of the 18th Conference of the European Chapter of the Association for Computational Linguistics",
    month = mar,
    year = "2024",
    publisher = "Association for Computational Linguistics",
    abstract = "Tactics, Techniques and Procedures (TTPs) represent sophisticated attack patterns in the cybersecurity domain, described encyclopedically in textual knowledge bases. Identifying TTPs in cybersecurity writing, often called TTP mapping, is an important and challenging task. Conventional learning approaches often target the problem in the classical multi-class or multilabel classification setting. This setting hinders the learning ability of the model due to a large number of classes (i.e., TTPs), the inevitable skewness of the label distribution and the complex hierarchical structure of the label space. We formulate the problem in a different learning paradigm, where the assignment of a text to a TTP label is decided by the direct semantic similarity between the two, thus reducing the complexity of competing solely over the large labeling space. To that end, we propose a neural matching architecture with an effective sampling-based learn-to-compare mechanism, facilitating the learning process of the matching model despite constrained resources.",
}
```

## License
This project is licensed under the Creative Commons CC BY License, version 4.0.
