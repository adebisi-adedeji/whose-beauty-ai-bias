# Whose Beauty? Geographic and Cultural Bias in AI Representations of Gender and Appearance

**Student:** Adebisi Adedeji
**Supervisor:** Giovanni Quattrone
**Programme:** MSc Data Science, Middlesex University London

## Research Question
Does providing geographic context influence how multimodal AI models describe the same person?

## Hypothesis
**H0:** Geographic context does not affect the description produced by multimodal models.
**H1:** Geographic context systematically changes the descriptions produced by multimodal models.

## Repository Structure
- README.md
- docs/ — Project report and documentation
- src/ — Source code including main pipeline
- data/raw/ — Raw images (gitignored)
- data/processed/ — Model outputs and results CSV
- weekly_meetings/ — Weekly progress logs and slides
- tests/ — Test scripts
- requirements.txt

## How to Run the Pipeline
1. Install dependencies: pip install -r requirements.txt
2. Set your API keys in the notebook — GEMINI_API_KEY and OPENAI_API_KEY
3. Open src/main.py in Google Colab and run all cells

## Models Used
- Google Gemini 3.5 Flash
- OpenAI GPT-4o Vision

## Regions Covered
- Sub-Saharan Africa — Nigeria, Kenya
- South and South-East Asia — India, Indonesia
- Middle East — Saudi Arabia, Jordan
- Western Europe — United Kingdom, Sweden
- Control — No country provided

## Current Status
- 40 images collected across 4 regions with full metadata
- Pilot experiment completed — 45 responses across 5 images and 9 country conditions
- First evidence of geographic bias identified in pilot results
