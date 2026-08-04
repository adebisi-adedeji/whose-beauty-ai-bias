# Stochasticity Baseline

## Objective

Large Language Models (LLMs) and Multimodal Large Language Models (MLLMs) are probabilistic systems. As a result, repeated generations using the same image and identical prompt may produce slightly different responses.

Before attributing differences in generated descriptions to geographic metadata, it is necessary to establish the model's intrinsic variability under identical prompting conditions.

This baseline provides a reference against which the effect of geographic conditioning can be compared.

---

# Motivation

If Gemini naturally produces different descriptions for the same image, some variation is expected even when the prompt does not change.

Therefore, observed differences between country-conditioned responses and the control should only be interpreted as evidence of geographic conditioning if they exceed the model's normal generation variability.

---

# Experimental Design

For each pilot image:

- Use the control prompt only.
- Generate multiple responses using identical generation parameters.
- Repeat the prompt the same number of times used in the main experiment.

No country metadata should be included.

---

# Baseline Measurement

For each image, semantic distance is calculated between repeated control generations.

For example:

- Control (Run 1) vs Control (Run 2)
- Control (Run 1) vs Control (Run 3)
- Control (Run 2) vs Control (Run 3)

These distances represent the model's intrinsic stochasticity.

---

# Country-Conditioned Measurement

Semantic distances are also calculated between:

- Country-conditioned responses
- The corresponding control response for the same image

These distances measure the effect of geographic metadata.

---

# Interpretation

Two quantities are compared:

- Baseline semantic variation under identical prompts.
- Semantic variation introduced by geographic metadata.

If the country-conditioned semantic distances are consistently larger than the baseline distances, this suggests that geographic metadata contributes additional variation beyond the model's normal stochastic behaviour.

If both quantities are similar, the observed differences may simply reflect normal generation variability rather than an effect of geographic metadata.

---

# Purpose

The stochasticity baseline improves the internal validity of the experiment by distinguishing variation caused by normal model randomness from variation associated with geographic conditioning.

This comparison strengthens the interpretation of semantic shift results and reduces the risk of attributing normal model variability to geographic metadata.
