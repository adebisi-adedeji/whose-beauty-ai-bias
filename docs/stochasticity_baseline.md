# Stochasticity Baseline

## Purpose

To establish a reference level of ordinary generation variability in the model's outputs, against which any apparent condition effect can be judged. This exists to answer a specific question: if two descriptions of the same image differ, is that difference due to the experimental condition (the country label), or is it simply normal variation the model would show even under identical, unchanged conditions?

## Design

Repeated generations from an identical prompt (same image, same condition, no variation) are compared against each other using semantic similarity, establishing a baseline distribution of "normal" variability between generations that share every input.

## Status in This Study

The stochasticity baseline was implemented as a **diagnostic control**, built into the pipeline as a permanent component. It was not itself used as a formal inferential outcome in the primary statistical battery (the Friedman/Wilcoxon tests reported in the dissertation's Results chapter). A direct, formal comparison between the stochasticity baseline and the condition-level effect sizes is identified as a direction for future work in the dissertation's Recommendations section — specifically, quantifying how much of any observed condition-level difference exceeds what ordinary generation noise alone would produce.

## Why This Matters

Without a baseline of this kind, any observed difference between conditions is ambiguous: it could reflect genuine sensitivity to the supplied country label, or it could simply be noise. Building this baseline in from the start, as a standing pipeline component rather than an afterthought, is part of this project's broader methodological approach of not accepting an apparent effect at face value without first checking whether a simpler explanation (like ordinary variability) accounts for it.
