# Reproducible Experimental Pipeline

## Overview

This document describes the complete experimental workflow used in the pilot study. The objective is to ensure that the methodology is transparent, reproducible and can be repeated using additional images without modifying the analysis pipeline.

---

# Step 1 – Image Selection

Portrait images are selected according to the image selection criteria described in `image_selection_criteria.md`.

The primary experiment uses culturally neutral portraits to minimise visual confounding.

---

# Step 2 – Prompt Generation

Each image is evaluated under five prompt conditions:

- Control (no country metadata)
- Nigeria
- India
- Saudi Arabia
- United Kingdom

The prompt template remains identical across all conditions except for the country label.

---

# Step 3 – Response Generation

Responses are generated using Gemini 3.5 Flash.

Each prompt condition is repeated three times using identical generation parameters.

This produces repeated generations for each image under every experimental condition.

---

# Step 4 – Data Storage

All generated responses are saved before analysis.

The dataset records:

- Image identifier
- Prompt condition
- Generation repeat
- Model response

This ensures that both the raw outputs and processed results remain reproducible.

---

# Step 5 – NLP Analysis

Each generated response is analysed using the following measures:

## Semantic Shift

Sentence embeddings are used to compare each country-conditioned response with the corresponding control response.

## Sentiment Analysis

VADER sentiment analysis is applied to each generated response.

## Adjective Analysis

Adjectives are extracted and grouped into predefined semantic categories.

## Unsupported Social Inference

Responses are manually annotated using the protocol defined in `annotation_protocol.md`.

---

# Step 6 – Statistical Analysis

Statistical analyses are performed at the image level.

The primary analyses include:

- Descriptive statistics
- Friedman test
- Pairwise Wilcoxon signed-rank tests
- Bonferroni correction where appropriate

Repeated generations are aggregated at image level to avoid treating individual model responses as independent observations.

---

# Step 7 – Visualisation

The analysis pipeline automatically generates:

- Summary tables
- Statistical output
- Figures
- Processed datasets

These outputs are saved for inclusion in the dissertation.

---

# Step 8 – Reproducibility

The repository contains all materials required to reproduce the pilot study, including:

- Experimental documentation
- Prompt templates
- Analysis notebook
- Annotation protocol
- Raw responses
- Processed datasets
- Figures
- Statistical outputs

Running the notebook using the same inputs and generation parameters reproduces the complete analysis workflow.

---

# Pipeline Summary

The experimental workflow follows the sequence below:

1. Select pilot images.
2. Generate prompts.
3. Generate Gemini responses.
4. Save raw responses.
5. Extract NLP measures.
6. Annotate unsupported social inference.
7. Perform statistical analysis.
8. Generate figures and tables.
9. Save processed outputs.
