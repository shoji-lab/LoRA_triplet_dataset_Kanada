# Human-Derived Ranking Ground Truth

This directory provides **ranking ground truth for LoRA retrieval evaluation**
constructed from human similarity judgments.

## Dataset Overview

The released file contains ranking annotations for a set of **query LoRA models**.

Each row in the CSV file represents the ranking position of a candidate LoRA:

```
{query_id,lora_id,rank}
```

- `query_id` — identifier of the query LoRA  
- `lora_id` — identifier of a candidate LoRA  
- `rank` — ground-truth ranking position (smaller is more similar)

Only **LoRA identifiers and ranking annotations** are included.  
LoRA weights, source images, and generated images are not redistributed.

## Construction Procedure

Ranking labels were obtained through the following process:

1. Candidate LoRAs were retrieved for each query using multiple retrieval methods.
2. The **union of retrieved candidates** formed the comparison set.
3. Human annotators performed **pairwise similarity comparisons**
   based solely on LoRA transformation outputs.
4. Pairwise judgments were aggregated into **total order rankings**
   using the **Copeland method**.

## Intended Use

This dataset is designed for evaluating:

- Retrieval performance of LoRA embeddings  
- Ranking quality using metrics such as **Recall@K** and **nDCG@K**  
- Human-aligned similarity search in generative model spaces  

The provided query–candidate ranking annotations may also be useful  
for **learning-to-rank research** in similarity-based retrieval settings.

## Notes on Data Release

Source images and LoRA-transformed images used during ranking annotation  
are **not redistributed** in this repository due to licensing considerations.

Further methodological details will be described in a future publication.