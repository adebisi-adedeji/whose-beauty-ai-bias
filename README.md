# Whose Beauty? Geographic and Cultural Bias in AI Representations of Gender and Appearance

**Student:** Adebisi Adedeji  
**Supervisor:** Giovanni Quattrone  
**Programme:** MSc Data Science, Middlesex University London

---

# Project Overview

This repository contains the experimental pipeline developed for my MSc Data Science dissertation investigating whether geographic metadata influences multimodal AI-generated descriptions of people.

The project evaluates whether providing country information alongside the same portrait image changes the model's visual descriptions or encourages unsupported higher-level social, cultural, occupational or personality inferences.

The current repository contains the validated pilot workflow that will be used for larger-scale experimentation.

---

# Research Question

> **Does providing geographic metadata influence how multimodal AI models describe the same portrait image?**

---

# Pilot Study Objective

The pilot study is designed to validate a reproducible experimental pipeline before scaling the experiment to a larger dataset.

Specifically, the pilot demonstrates that:

- the prompting framework produces consistent structured outputs;
- the NLP pipeline extracts the intended quantitative metrics;
- the statement-level annotation protocol is transparent and reproducible;
- the statistical workflow is appropriate for repeated-measures analysis;
- the complete methodology is suitable for larger-scale evaluation.

---

# Experimental Design

| Component | Details |
|-----------|---------|
| **Model** | Gemini 3.5 Flash |
| **Images** | 10 pilot portrait images |
| **Conditions** | Control, Nigeria, India, Saudi Arabia, United Kingdom |
| **Repeats** | 3 per condition |
| **Total Responses** | 150 |

---

# Experimental Pipeline

The experimental workflow consists of the following stages:

```text
Image Selection
      ↓
Prompt Generation
      ↓
Gemini 3.5 Flash
      ↓
Structured JSON Responses
      ↓
Statement Extraction
      ↓
Statement-Level Evidence Verification
      ↓
NLP Analysis
      ↓
Statistical Analysis
      ↓
Figures, Tables & Documentation
```

---

# Key Outputs

The pilot pipeline automatically produces:

- Raw model responses
- Processed datasets
- Semantic shift analysis
- Sentiment analysis
- Adjective frequency analysis
- Statement-level annotation summaries
- Unsupported inference analysis
- Statistical test results
- Publication-ready figures
- Summary tables
- Reproducible documentation

---

# Repository Structure

```text
whose-beauty-pipeline/

├── notebooks/
│   └── whose_beauty_pipeline.ipynb
│
├── data/
│   ├── raw/
│   └── processed/
│
├── figures/
│
├── tables/
│
├── documentation/
│   ├── methodology.md
│   ├── unsupported_inference_coding_protocol.md
│   ├── annotation_examples.md
│   ├── reproducible_pipeline.md
│   ├── image_selection_review.md
│   └── stochasticity_baseline.md
│
├── weekly_meetings/
│
├── requirements.txt
│
└── README.md
```

---

# How to Run

Clone the repository.

```bash
git clone https://github.com/<username>/whose-beauty-pipeline.git
```

Install the required packages.

```bash
pip install -r requirements.txt
```

Configure your Gemini API key.

Open the notebook:

```text
notebooks/whose_beauty_pipeline.ipynb
```

Run all notebook cells sequentially.

---

# Technologies

- Python 3.11
- Google Colab
- Gemini 3.5 Flash
- pandas
- NumPy
- Sentence Transformers
- spaCy
- NLTK (VADER)
- SciPy
- Matplotlib

---

# Pilot Findings

The pilot demonstrates that:

- Geographic metadata produced relatively small semantic shifts across conditions.
- Unsupported inference rates varied across country conditions.
- The control condition exhibited the highest unsupported inference rate in the pilot dataset.
- Statement-level annotation provides a transparent and reproducible framework for evaluating unsupported social inferences.
- The complete experimental pipeline successfully generates reproducible quantitative outputs suitable for larger-scale experimentation.

The primary contribution of the pilot is the validation of the experimental methodology rather than confirmation of the final research hypothesis.

---

# Current Status

The repository currently contains:

- A validated pilot experimental pipeline ready for larger-scale experimentation.
- A reproducible Google Colab notebook.
- Automated response generation and structured JSON parsing.
- Statement-level visual-evidence verification.
- NLP analysis pipeline.
- Statistical analysis workflow.
- Figures, tables and supporting documentation.
- Weekly supervision logs documenting project development.

---

# Next Steps

Future work will focus on:

- Increasing the number of culturally neutral portrait images.
- Implementing the stochasticity baseline.
- Evaluating additional multimodal large language models (MLLMs).
- Applying the validated annotation protocol to larger datasets.
- Comparing geographic metadata effects across additional countries.
- Investigating culturally diagnostic portraits as a separate robustness experiment.

---

# Licence

This repository is maintained for academic research conducted as part of the MSc Data Science programme at Middlesex University London.

---

# Citation

If you use this repository for academic purposes, please cite:

> **Adedeji, A. (2026).**  
> *Whose Beauty? Geographic and Cultural Bias in AI Representations of Gender and Appearance.*  
> MSc Data Science Dissertation, Middlesex University London.
