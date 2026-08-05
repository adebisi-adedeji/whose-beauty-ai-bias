# Stochasticity Baseline

## Objective

Large Language Models (LLMs) and Multimodal Large Language Models (MLLMs) are probabilistic systems. Consequently, repeated generations using the same image and identical prompt may produce slightly different responses.

Before attributing observed differences in generated descriptions to geographic metadata, it is important to estimate the model's intrinsic variability under identical prompting conditions.

The stochasticity baseline provides a reference against which the effect of geographic conditioning can be evaluated.

---

# Motivation

Semantic differences between model outputs may arise for two reasons:

1. Normal stochastic variation in the model.
2. Geographic metadata supplied in the prompt.

Without estimating the model's intrinsic variability, semantic differences observed between experimental conditions may simply reflect normal generation randomness rather than an effect of geographic metadata.

Establishing a stochasticity baseline improves the internal validity of the experimental design.

---

# Experimental Design

For each pilot image:

- Use the **control prompt only**.
- Generate multiple responses using identical generation parameters.
- Repeat the prompt the same number of times used in the primary experiment.
- Do not provide any country metadata.

This procedure isolates the model's natural variability under identical experimental conditions.

---

# Baseline Measurement

For each image, semantic distances are calculated between repeated control generations.

Example comparisons include:

- Control (Run 1) vs Control (Run 2)
- Control (Run 1) vs Control (Run 3)
- Control (Run 2) vs Control (Run 3)

These distances estimate the model's intrinsic stochasticity.

---

# Country-Conditioned Measurement

Semantic distances are also calculated between:

- each country-conditioned response;
- the corresponding control response for the same image.

These distances estimate the semantic variation associated with geographic conditioning.

---

# Interpretation

Two sources of variation are compared:

1. Baseline semantic variation under identical prompts.
2. Semantic variation introduced by geographic metadata.

If country-conditioned semantic distances consistently exceed the baseline variation, this provides evidence that geographic metadata contributes additional variation beyond the model's normal stochastic behaviour.

If both quantities are similar, the observed differences are more likely to reflect normal generation variability rather than an effect of geographic conditioning.

---

# Planned Statistical Comparison

The stochasticity baseline will be compared with country-conditioned semantic shift distributions using the same repeated-measures framework adopted throughout the pilot study.

The image will remain the primary experimental unit.

---

# Role Within the Pilot Study

The stochasticity baseline forms an important methodological validation step.

Although the pilot primarily focuses on validating the experimental pipeline, establishing this baseline demonstrates that the methodology can distinguish variation introduced by geographic metadata from normal model variability.

The baseline will therefore be incorporated into the full-scale experiment before the study is expanded beyond the pilot dataset.

---

# Expected Outcome

The stochasticity baseline is expected to provide a quantitative reference for interpreting semantic shift measurements.

By separating normal model variability from the effects of geographic conditioning, the methodology becomes more transparent, reproducible and statistically robust.
