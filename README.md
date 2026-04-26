# LoRA Triplet Dataset

This repository provides benchmark datasets for evaluating  
**similarity-based retrieval of style-transfer LoRA adapters**.

The datasets were constructed as part of an academic research project
on LoRA embedding and retrieval accepted to **ICMR 2026**.

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

## Publication

This dataset was used in the following paper:

Retrieval of LoRA Models based on Layer-Wise Weight Embedding without Metadata, Yuro Kanada, Yuma Oe, Huu-Long Pham, Makoto P. Kato, Hiroaki Ohshima, Sumio Fujita and Yoshiyuki Shoji, Proc. of The 16th ACM International Conference on Multimedia Retrieval (ICMR2026), to appear, 2026.

---

## Citation

If you use this dataset in your research, please cite the paper below. If a dataset DOI is assigned to this repository, please cite both the paper and the dataset DOI.

```bibtex
@inproceedings{kanada2026retrieval,
  title = {Retrieval of LoRA Models based on Layer-Wise Weight Embedding without Metadata},
  author = {Kanada, Yuro and Oe, Yuma and Pham, Huu-Long and Kato, Makoto P. and Ohshima, Hiroaki and Fujita, Sumio and Shoji, Yoshiyuki},
  booktitle = {Proceedings of the 16th ACM International Conference on Multimedia Retrieval},
  year = {2026},
  note = {To appear}
}
```

For maintainability, citation information is maintained in this top-level README. Subdirectory README files refer back to this section instead of duplicating the full citation.

---

## License

This repository distributes **annotations, metadata, and evaluation splits only**.  
Original LoRA models remain subject to their respective licenses.

---

## Maintainer

Yuro Kanada  
Shoji Laboratory, Shizuoka University
