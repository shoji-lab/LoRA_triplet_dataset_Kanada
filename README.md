# LoRA Triplet Dataset (Kanada, Shoji Lab)

This repository provides benchmark datasets for evaluating  
**similarity-based retrieval of style-transfer LoRA adapters**.

The datasets were constructed for research submitted to **ICMR 2026**.  
For full methodological details and experimental settings,  
please refer to the corresponding paper:

> ここに論文のリンクを貼る？

---

## Overview

This repository releases **derived evaluation datasets only**  
and does **not redistribute any LoRA model weights**.

The datasets support reproducible research in:

- LoRA embedding learning  
- Similarity-based LoRA retrieval  
- Triplet-based metric learning  
- Human-aligned ranking evaluation for generative models  

---

## Repository Structure

data/
├── triplets_auto_visual/
├── triplets_human_visual/
└── ranking_human_visual/


Each directory contains:

- Dataset files  
- A brief description of the dataset and annotation procedure  

Please refer to the **README inside each directory** for details.

---

## Relation to ICMR 2026 Submission

These datasets were created for the following research:

> **Learning LoRA Embeddings from Internal Parameters for  
> Similarity-Based Retrieval of Style-Transfer Adapters**

Complete preprocessing, model design, and evaluation methodology  
are described in the paper.

📄 Please refer to the paper for full details.  
(ここにもリンク？)

---

## Important Notice

- This repository **does not include LoRA safetensors or model weights**.
- Original LoRA models must be obtained from their **official distribution sources**.
- Only **evaluation annotations and metadata** are provided.

---

## Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{kanada2026lora,
  title     = {Learning LoRA Embeddings from Internal Parameters for Similarity-Based Retrieval of Style-Transfer Adapters},
  author    = {Kanada, Yuro and others},
  booktitle = {Proceedings of ICMR 2026},
  year      = {2026}
}
