# ALL/AML Gene Expression Classification

A machine learning project for classifying acute lymphoblastic leukemia (ALL) and acute myeloid leukemia (AML) using microarray gene expression data.

## Overview

This project investigates how gene expression patterns can distinguish between two leukemia subtypes: ALL and AML.

The study focuses on the challenges of high-dimensional biomedical data, where the number of measured features greatly exceeds the number of samples. It includes exploratory data analysis, literature review, feature selection, and comparative machine learning experiments.

> Both ALL and AML are leukemia subtypes. This project does not classify cancer versus non-cancer samples.

## Project Status

**Current stage:** Project setup and interim report preparation.

Planned tasks:

- [ ] Review relevant scientific literature.
- [ ] Load and validate the Golub dataset.
- [ ] Select an additional public gene expression dataset.
- [ ] Perform exploratory data analysis on both datasets.
- [ ] Prepare the interim report.
- [ ] Implement leakage-free preprocessing and feature selection.
- [ ] Compare at least three machine learning methods.
- [ ] Evaluate results and prepare the final report.

## Research Questions

1. To what extent do ALL and AML samples show distinct patterns in exploratory gene expression visualizations?
2. How do preprocessing and feature selection affect classification performance?
3. Are the observed patterns and method comparisons consistent across an additional public dataset?

## Datasets

### Primary Dataset: Golub ALL/AML

The primary dataset contains gene expression measurements from 72 patients, with 7,129 gene probes.

| Subset | Samples | ALL | AML |
|---|---:|---:|---:|
| Training | 38 | 27 | 11 |
| Independent test | 34 | 20 | 14 |
| Total | 72 | 47 | 25 |

Required files:

- `data_set_ALL_AML_train.csv`
- `data_set_ALL_AML_independent.csv`
- `actual.csv`

Patient labels will be matched using patient identifiers rather than column order. Non-numeric call columns will be separated from gene expression measurements.

The exact download source and applicable usage conditions will be documented during data acquisition.

### Additional Dataset

An additional public gene expression dataset will be selected from the literature.

Its accession number, publication, platform, sample counts, class distribution, and usage conditions will be documented before analysis.

## Exploratory Data Analysis

The analysis will cover:

- Data dimensions and patient-label alignment.
- Missing, infinite, negative, and extreme values.
- Class distributions and descriptive statistics.
- Expression distributions before and after an appropriate transformation.
- Principal component analysis with explained variance.
- t-SNE or UMAP visualizations.
- Class-wise statistical comparisons with multiple-testing correction.
- Heatmaps and hierarchical clustering of selected genes.
- Training/test distribution differences and possible batch effects.
- Differences between the primary and additional datasets.

Exploratory findings will be distinguished from validated predictive results.

## Planned Modeling Approach

At least three machine learning methods will be compared. Candidate methods include:

- Decision Tree.
- Support Vector Machine.
- Logistic Regression.

The final choices and hyperparameter search spaces will be justified in the report.

Preprocessing, imputation, scaling, and feature selection will be fitted within the appropriate training folds.

Evaluation will include:

- The original 38/34 training/test split.
- Nested stratified cross-validation.
- Accuracy and balanced accuracy.
- Precision, recall, specificity, and F1-score.
- ROC-AUC and confusion matrices.
- Variability across repeated experiments.

The independent test set will not be used for model or hyperparameter selection.

## Planned Repository Structure

```text
all-aml-gene-expression-classification/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── src/
├── results/
│   ├── figures/
│   └── tables/
├── reports/
├── .gitignore
├── README.md
└── requirements.txt
```

This structure will be populated as the project progresses.

Raw datasets will not be committed to the repository. Download instructions and data preparation steps will be provided instead.

## Reproducibility

The project will document:

- Python and package versions.
- Dataset sources and preparation steps.
- Random seeds.
- Instructions for reproducing figures, tables, and experiments.

Setup and execution commands will be added once the initial analysis workflow is implemented.

## Reports and Video

Links will be added when the deliverables are available:

- Interim report.
- Final report.
- Presentation videos.
- Supplementary analysis and AI usage declaration.

## Generative AI Usage

Any use of generative AI for coding assistance, writing, or explanation will be documented.

The declaration will describe the tool used, its purpose, the affected files or sections, changes made by the author, and verification steps. The author remains responsible for all code, interpretations, and reported results.

## Limitations

The primary dataset has a small sample size and a large number of features. Overfitting, class imbalance, platform differences, and batch effects will be considered when interpreting the results.

This repository is an academic research project and is not intended for clinical diagnosis.

## References

The verified bibliography and dataset references will be added as the literature review progresses.
