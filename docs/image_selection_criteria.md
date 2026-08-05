# Image Selection and Review Protocol

## Objective

The purpose of this protocol is to classify each pilot image according to the presence or absence of culturally diagnostic visual cues before experimentation.

Separating culturally neutral and culturally diagnostic portraits reduces potential confounding between visual evidence and supplied geographic metadata and supports a reproducible image-selection process.

---

# Rationale

The pilot study investigates whether geographic metadata influences multimodal AI-generated descriptions of the same portrait.

Images containing strong cultural, religious or national identifiers may influence model outputs independently of the supplied geographic metadata.

Consequently, two related but distinct research questions arise:

1. Does geographic metadata influence model descriptions when the portrait is culturally neutral?

2. When strong cultural cues are present, does the model prioritise visual evidence or supplied geographic metadata?

The primary pilot experiment addresses the first question.

The second question is reserved for future robustness analyses.

---

# Image Categories

## Culturally Neutral Portrait

### Definition

A portrait containing no obvious visual indicators of a specific culture, religion or nationality.

### Typical Characteristics

- Plain or contemporary clothing
- Neutral background
- No religious symbols
- No traditional clothing
- No national flags or emblems
- No culturally distinctive accessories

These images form the primary experimental dataset.

---

## Culturally Diagnostic Portrait

### Definition

A portrait containing clear visual cues commonly associated with a particular culture, religion or nationality.

### Typical Characteristics

- Hijab
- Sari
- Turban
- Traditional African clothing
- Religious jewellery or symbols
- National flags
- Military or ceremonial uniforms
- Hairstyles strongly associated with a particular cultural tradition

These images should be analysed separately as a robustness experiment rather than included in the primary experiment.

---

# Image Review Procedure

Each image is reviewed independently before experimentation.

For every image, the reviewer records:

- Image identifier
- Presence of culturally diagnostic visual cues (Yes/No)
- Assigned classification:
  - Neutral
  - Diagnostic
- Reviewer comments (if applicable)

The image classification is completed before prompt generation and remains fixed throughout the experiment.

---

# Inclusion Criteria

Images included in the primary experiment should:

- contain a single individual;
- provide sufficient facial detail for multimodal description;
- contain no obvious cultural or religious identifiers;
- be of sufficient visual quality for analysis.

---

# Exclusion Criteria

Images should be excluded from the primary experiment if they contain:

- obvious religious attire;
- traditional cultural clothing;
- national symbols;
- ceremonial uniforms;
- strong contextual cues indicating nationality, religion or culture.

Such images may be retained for future robustness analyses.

---

# Expected Outcome

The primary pilot experiment should use culturally neutral portraits to minimise visual confounding.

Culturally diagnostic portraits should be analysed separately to investigate whether multimodal AI models prioritise visual evidence or supplied geographic metadata when both sources of information are available.

This review protocol improves transparency, reproducibility and consistency in image selection before scaling the study to a larger dataset.
