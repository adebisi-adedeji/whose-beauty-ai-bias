# Reproducible Pipeline

## Overview

This document describes the full generation-to-analysis pipeline, for reproducibility.

## Frozen Generation Configuration

Every API call in the final run used the following configuration, logged automatically:

| Parameter | Value |
|---|---|
| Model | gemini-3.5-flash |
| API library | google-genai |
| Temperature | 1.0 |
| Top-p | 0.95 |
| Top-k | 40 |
| Max output tokens | 2048 |
| Generation date | 2026-09-17 |

## Pipeline Steps

1. **Image screening** — see `image_selection_criteria.md`. Ten images selected; nine main-analysis, one robustness.
2. **Prompt construction** — matched control and country-conditioned prompts, differing only in the presence of a country name (see `methodology.md`).
3. **Generation** — 10 images × 5 conditions × 3 repeats = 150 API calls, each logged with image ID, condition, repeat number, and any retries. Output: `data/processed/final_run_raw_responses.csv`.
4. **Parsing** — raw JSON responses parsed into structured fields (description, appearance_adjectives, social_or_cultural_inferences, occupation_inferences, personality_inferences). Output: `data/processed/final_dataset_structured.csv`.
5. **Statement extraction** — each response decomposed into individual sentence-level or list-entry-level statements across all four fields. Output: 525 total statements.
6. **Stratified sampling** — a proportional sample drawn across all five conditions and four source fields for full manual annotation, with scarce fields (occupation, personality) retained in full.
7. **Manual annotation** — using the interactive annotation tool in the notebook; see `annotation_protocol.md` and `annotation_examples.md`. Output: `data/processed/primary_annotation_sample.csv`.
8. **Inter-rater reliability check** — a separate stratified 27-statement subset, independently double-coded. Output: `reliability_subset_ADEBISI_LABELS.csv` and `reliability_subset_ZIMUZO_LABELS.csv`.
9. **Statistical analysis** — aggregation to image level, Friedman tests, Wilcoxon post-hoc with Holm correction, Kendall's W. See the dissertation report for full results.

## Reproducing This Pipeline

The notebook (`notebooks/whose_beauty_pipeline.ipynb`) contains the full code for every step above. Note: three cells that were used once to *build* the stratified samples (statement extraction, reliability subset construction, primary sample construction) have been removed from the shared notebook after use, since re-running them would generate a fresh random sample rather than reproducing the existing one. The output files in `data/processed/` are the actual data used in the dissertation's analysis and should be treated as the source of truth, not regenerated from the notebook.

## Known Limitations

- Generation-configuration parameters for the original pilot run (prior to the final run documented here) were not fully recorded, since the analysis notebook used for pilot-stage work loaded pre-generated data rather than containing the original generation code.
- The stochasticity baseline (see `stochasticity_baseline.md`) is a diagnostic control, not yet formally compared against condition-level effects.
