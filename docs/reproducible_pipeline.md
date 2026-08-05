# Reproducible Experimental Pipeline

## Overview

This document describes the complete experimental workflow used in the pilot study.

The objective of the pilot is to validate a transparent, reproducible and scalable experimental pipeline for investigating whether geographic metadata influences multimodal AI-generated descriptions of the same portrait.

The pilot is designed to demonstrate that the complete workflow—from image selection to statistical analysis—can be reproduced before scaling to a larger dataset.

---

# Step 1 – Image Selection

A pilot dataset of **10 portrait photographs** was selected from openly licensed image collections.

Images were reviewed to distinguish:

- culturally neutral portraits;
- culturally diagnostic portraits.

The primary pilot experiment focuses on culturally neutral portraits to minimise visual confounding between image content and supplied geographic metadata.

---

# Step 2 – Prompt Generation

Each image is evaluated under five experimental conditions:

- Control (no geographic metadata)
- Nigeria
- India
- Saudi Arabia
- United Kingdom

The prompt template remains identical across all conditions except for the supplied country label.

This isolates geographic metadata as the only experimental variable.

---

# Step 3 – Response Generation

Responses are generated using **Google Gemini 3.5 Flash**.

Each image is generated:

- under five experimental conditions;
- with three repeated generations per condition.

These repeated generations capture normal model variability.

---

# Step 4 – Stochasticity Baseline

Repeated generations under identical prompts provide a baseline estimate of the model's intrinsic stochasticity.

This baseline is compared with country-conditioned generations to determine whether observed semantic differences exceed normal generation variability.

---

# Step 5 – Data Storage

Every generated response is saved before analysis.

Each record contains:

- image identifier;
- experimental condition;
- repetition number;
- generated response.

Both raw and processed datasets are preserved to ensure complete reproducibility.

---

# Step 6 – NLP Analysis

Each generated response is analysed using multiple quantitative measures.

## Semantic Shift

Sentence embeddings are used to compare every country-conditioned description with its corresponding control description.

## Sentiment Analysis

VADER compound sentiment scores are computed for every generated description.

## Adjective Analysis

Adjectives are extracted using spaCy and grouped into predefined semantic categories.

## Statement Extraction

Each generated response is decomposed into individual statements before annotation.

---

# Step 7 – Statement-Level Annotation

Every extracted statement is evaluated independently.

Each statement is first verified using the constrained question:

> **Is this statement directly supported by visual evidence in the image?**

Possible evidence labels are:

- Supported
- Unsupported
- Uncertain

Each verified statement is then assigned to one of five annotation categories:

- Visible Description
- Visually Supported Interpretation
- Metadata Repetition
- Unsupported Social Inference
- Incorrect Visual Hallucination

This two-stage annotation process improves transparency and reproducibility.

---

# Step 8 – Statistical Analysis

The image remains the primary experimental unit.

The analysis includes:

- descriptive statistics;
- semantic shift analysis;
- sentiment analysis;
- adjective frequency analysis;
- statement-level annotation summaries;
- Friedman tests;
- pairwise Wilcoxon signed-rank tests;
- Bonferroni correction where appropriate.

Repeated generations are aggregated at image level to avoid treating individual model outputs as independent observations.

---

# Step 9 – Visualisation

The pipeline automatically generates:

- processed datasets;
- descriptive summary tables;
- statistical test results;
- semantic shift figures;
- adjective analysis figures;
- unsupported inference figures.

These outputs are exported for inclusion in the dissertation.

---

# Step 10 – Reproducibility

The repository contains all materials required to reproduce the pilot experiment, including:

- methodology documentation;
- prompt templates;
- annotation protocol;
- Google Colab notebook;
- raw responses;
- processed datasets;
- figures;
- statistical outputs;
- weekly development logs.

Running the notebook using the same images, prompts and generation parameters reproduces the complete analysis workflow.

---

# Pipeline Summary

The experimental workflow follows the sequence below:

1. Select pilot images.
2. Generate experimental prompts.
3. Generate repeated model responses.
4. Estimate stochasticity baseline.
5. Save raw responses.
6. Extract NLP measures.
7. Decompose responses into statements.
8. Verify statement-level visual evidence.
9. Categorise verified statements.
10. Perform statistical analyses.
11. Generate figures and tables.
12. Save processed outputs.
