# Automatic Visual Triplets

This directory contains **automatically constructed triplets of LoRA models**
based on visual similarity of LoRA-transformed images.

## Dataset Overview

Two triplet datasets are provided:

- `train_triplets.jsonl` — constructed from LoRA models used for training  
- `eval_triplets.jsonl` — constructed from LoRA models used for evaluation  

Each file is stored in **JSON Lines format**, where each line represents one triplet:

```json
{"anchor": "<LoRA_ID>", "positive": "<LoRA_ID>", "negative": "<LoRA_ID>"}
```

Only LoRA identifiers are included in the released files.
LoRA weights, source images, and generated images are not redistributed.

## Construction Procedure

The triplets were generated through the following pipeline:

1. A shared set of source images was transformed using each LoRA model.
2. Generated outputs were embedded using **DINOv2 visual representations**.
3. Pairwise cosine similarity between LoRA transformations was computed.
4. Triplets were constructed by selecting:
   - visually similar pairs as **positives**
   - visually dissimilar pairs as **negatives**

## Intended Use

This dataset is designed for:

- Training and validating metric learning models  
- Learning embedding representations of LoRA transformations  
- Automatic similarity supervision without human annotation  

## Notes on Data Release

Source images and LoRA-transformed images used during triplet construction  
are **not redistributed** in this repository due to licensing considerations.

Further methodological details will be described in a future publication.