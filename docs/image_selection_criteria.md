# Review the Image Set

## Objective

The pilot image set should be reviewed to identify whether each image is culturally neutral or culturally diagnostic.

This distinction is important because images containing strong cultural or religious cues may confound the experiment. In these cases, the model may respond to the visual evidence rather than the supplied geographic metadata.

Separating the images into these categories helps distinguish two different research questions:

1. Does geographic metadata influence the model when the portrait is culturally neutral?

2. Does the model prioritise visual evidence or supplied geographic metadata when strong cultural cues are present?

---

# Image Categories

## Culturally Neutral Portrait

A portrait containing no obvious cultural, religious or national identifiers.

Typical characteristics include:

- Plain clothing
- Neutral background
- No religious symbols
- No traditional clothing
- No visible national identifiers

These images should form the primary experimental dataset.

---

## Culturally Diagnostic Portrait

A portrait containing obvious visual cues associated with a particular culture, religion or nationality.

Examples include:

- Hijab
- Sari
- Turban
- Traditional African clothing
- Religious jewellery or symbols
- National flags
- Military or ceremonial uniforms
- Traditional hairstyles strongly associated with one culture

These images should be analysed separately as a robustness experiment rather than included in the primary experiment.

---

# Image Review Procedure

Each image should be reviewed before experimentation.

The reviewer should determine whether the portrait contains obvious cultural or religious identifiers.

Images should then be assigned to one of two groups:

- Neutral
- Diagnostic

The classification should be documented before any prompts are generated.

---

# Expected Outcome

The primary experiment should use culturally neutral portraits.

Culturally diagnostic portraits may be retained for a secondary robustness analysis investigating whether the model prioritises visual evidence or supplied geographic metadata.
