# Dataset Split and Metadata Description

This directory provides the **LoRA ID splits and metadata**
used in the experiments for similarity learning and retrieval evaluation.

---

## Split Files

### `train_ids_549.txt`

Contains the **LoRA identifiers used for training**.

- One LoRA ID per line  
- Total: **549 LoRA models**

These IDs were used to construct:

- Automatic training triplets  
- Metric learning supervision  

---

### `eval_ids_150.txt`

Contains the **LoRA identifiers used for evaluation**.

- One LoRA ID per line  
- Total: **150 LoRA models**

These IDs were used for:

- Automatic evaluation triplets  
- Human-labeled triplet annotations  
- Ranking ground-truth construction  

---

## Metadata File

### `lora_metadata_used.csv`

Provides metadata for **all LoRA models used in the study**
(including both training and evaluation splits).

Each row contains:

- `Model_id` — unique identifier of the LoRA model  
- `Model Name` — model name from the original source  
- `URL` — URL of the official distribution page  
- `split` — dataset split (`train` or `eval`)  

This file enables **full reproducibility of dataset construction**.

---

## Access to Original LoRA Models

This repository **does not redistribute LoRA model weights**.

To reproduce the experiments, users must obtain the original LoRA models
from their **official distribution sources** using the URLs provided in
`lora_metadata_used.csv`.

Users are responsible for complying with the **license terms**
of each individual LoRA model.

---

## Notes on Reproducibility

- All evaluation datasets released in this repository
  are derived solely from the LoRA IDs listed above.
- No additional hidden data or private annotations are used.
- The provided splits are sufficient to reproduce:

  - Automatic triplet construction  
  - Human triplet evaluation  
  - Retrieval ranking benchmarks  

Further methodological details will be described in a future publication.
