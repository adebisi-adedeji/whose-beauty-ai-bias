# Whose Beauty? Geographic and Cultural Bias in AI Representations of Gender and Appearance

**Student:** Adebisi Adedeji  
**Supervisor:** Giovanni Quattrone  
**Programme:** MSc Data Science, Middlesex University London

---

# Project Overview

This repository contains the experimental pipeline developed for my MSc Data Science dissertation investigating whether geographic metadata influences multimodal AI-generated descriptions of people.

The project evaluates whether providing country information alongside the same portrait image changes the model's visual descriptions or encourages unsupported higher-level inferences. The current repository contains the validated pilot workflow that will be used for larger-scale experimentation.

---

# Research Question

**Does providing geographic metadata influence how multimodal AI models describe the same portrait image?**

---

# Pilot Study Objective

The purpose of the pilot study is to validate a reproducible experimental pipeline before scaling the experiment to a larger dataset.

Specifically, the pilot demonstrates that:

- The prompting framework generates consistent structured outputs.
- The NLP pipeline extracts the intended quantitative metrics.
- The statement-level annotation protocol is reproducible.
- The statistical workflow is appropriate.
- The complete methodology is suitable for larger-scale evaluation.

---

# Experimental Design

| Component | Details |
|-----------|---------|
| Model | Gemini 3.5 Flash |
| Images | 10 culturally neutral portrait images |
| Conditions | Control, Nigeria, India, Saudi Arabia, United Kingdom |
| Repeats | 3 |
| Total Responses | 150 |

---

# Experimental Pipeline

The experimental workflow consists of the following stages:

1. Image selection
2. Prompt generation
3. Gemini response generation
4. JSON parsing
5. Statement extraction
6. Statement-level visual-evidence verification
7. NLP analysis
8. Statistical analysis
9. Results visualisation
10. Reproducible export

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
├── docs/
│   ├── methodology.md
│   ├── weekly_logs/
│   └── supervision_notes/
│
├── presentations/
│
├── requirements.txt
│
└── README.md
```

---

# How to Run

1. Clone this repository.

```bash
git clone https://github.com/<username>/whose-beauty-pipeline.git
```

2. Install the required packages.

```bash
pip install -r requirements.txt
```

3. Configure your API credentials.

Set your Gemini API key before running the notebook.

4. Open the notebook in Google Colab or Jupyter Notebook.

```
notebooks/whose_beauty_pipeline.ipynb
```

5. Run all notebook cells sequentially.

---

# Technologies

- Python
- Google Colab
- Gemini 3.5 Flash
- pandas
- NumPy
- spaCy
- Sentence Transformers
- NLTK / VADER
- SciPy
- Matplotlib

---

# Current Status

The repository currently contains:

- A validated pilot experimental pipeline.
- A reproducible Google Colab notebook.
- Automated response generation and JSON parsing.
- Statement-level visual-evidence verification.
- NLP analysis pipeline.
- Statistical analysis workflow.
- Figures, tables and supporting documentation for the pilot study.

---

# Next Steps

Future work will focus on:

- Increasing the number of culturally neutral portrait images.
- Evaluating additional multimodal AI models.
- Applying the validated annotation protocol to larger datasets.
- Comparing metadata effects across more countries and image sets.
- Investigating culturally diagnostic portraits as a separate experiment.

---

# Licence

This repository is maintained for academic research conducted as part of the MSc Data Science programme at Middlesex University London.
