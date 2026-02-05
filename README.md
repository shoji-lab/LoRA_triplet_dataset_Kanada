# LoRA Triplet Dataset

This repository provides benchmark datasets for evaluating  
**similarity-based retrieval of style-transfer LoRA adapters**.

The datasets were constructed as part of an **ongoing academic research project**
on LoRA embedding and retrieval.  
Further technical details will be released in a future publication.

---

## Overview

This repository releases **derived evaluation datasets only**  
and does **not redistribute any LoRA model weights**.

The datasets support reproducible research in:

- LoRA embedding learning from internal parameters  
- Triplet-based metric learning  
- Human-aligned similarity evaluation  
- Retrieval ranking evaluation for generative models  

---

## Repository Structure

```
data/
├── triplets_auto_visual/
│   ├── train_triplets.jsonl
│   ├── eval_triplets.jsonl
│   └── README.md
│
├── triplets_human_visual/
│   ├── human_labeled_triplets.jsonl
│   └── README.md
│
└── ranking_human_visual/
    ├── ranking_gt_30_queries.csv
    └── README.md

metadata/
├── train_ids_549.txt
├── eval_ids_150.txt
├── lora_metadata_used.csv
└── split_description.md
```

Each directory in `data/` contains dataset files and a brief README.  
See the README in each subdirectory for details.

---


## Reproducibility

The file:

metadata/lora_metadata_used.csv


provides metadata for all LoRA models used in the experiments,  
including identifiers, source URLs, and dataset splits.

Together with:

- `train_ids_549.txt`
- `eval_ids_150.txt`

this information enables reproducibility of the dataset construction.

---

## Access to Original LoRA Models

This repository **does not include LoRA model weights**.  
Original models must be obtained from their official sources using  
the URLs provided in `lora_metadata_used.csv`.

---

## License

This repository distributes **annotations, metadata, and evaluation splits only**.  
Original LoRA models remain subject to their respective licenses.

---

## Maintainer

Yuro Kanada  
Shoji Laboratory, Shizuoka University
