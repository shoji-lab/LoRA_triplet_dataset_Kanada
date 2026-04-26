# Human-Labeled Visual Triplets

This directory provides **triplets annotated by human relative similarity judgments**
based on visual comparison of LoRA transformation outputs.

## Dataset Overview

The released file contains triplets constructed from **evaluation LoRA models**.

Each file is stored in **JSON Lines format**, where each line represents one triplet:

```json
{"anchor": "<LoRA_ID>", "positive": "<LoRA_ID>", "negative": "<LoRA_ID>"}
```

Only LoRA identifiers and annotation results are included.
LoRA weights, source images, and generated images are not redistributed.

## Annotation Procedure

Triplets were obtained through the following process:

1. LoRA transformation outputs were visually compared by human annotators.
2. Annotators selected the candidate whose transformation appeared  
   **more similar to the anchor**.
3. Multiple annotations were collected for each comparison.
4. Final triplet labels were determined using **majority agreement**.

## Intended Use

This dataset enables evaluation of:

- Alignment between learned embeddings and **human perceptual similarity**
- Quality of similarity learning in generative model retrieval
- Human-grounded validation of metric learning approaches

## Notes on Data Release

Source images and LoRA-transformed images used during annotation  
are **not redistributed** in this repository due to licensing considerations.

Further methodological details are described in the ICMR 2026 paper cited in
the top-level README.

## Citation

If you use this dataset, please follow the citation information in the
top-level `README.md`.
