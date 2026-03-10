# Automated VDM with Open Source LLMs — Prompts and Datasets

This repository contains the prompts and datasets associated with the paper
**"Automated VDM with Open Source LLMs"**.

## Prompts

The `prompts/` directory contains all prompt versions used in the CVE-to-CWE
and CVE-to-ATT&CK mapping experiments, including manually written baseline
prompts, few-shot augmented variants, and the GEPA-optimized prompts for
Gemma3:12B and Qwen2.5:7b. Prompts are organized by task and model.

## Datasets

Two novel CVE-to-ATT&CK evaluation datasets are provided in the `datasets/`
directory, both derived from the BRON-sourced benchmark used in prior work.

**ATT&CK-Curated** is a curated positive-only dataset containing high-confidence
CVE--technique pairs. Low-quality and ambiguous pairs from the original source
have been removed, retaining only validated mappings accompanied by both entity
descriptions.

**ATT&CK-Extended** extends the ATT&CK-Curated dataset with 4,500 hard negative pairs constructed
from the lowest-scoring candidates produced by the semantic similarity filter,
yielding a balanced evaluation set suitable for binary classification analysis.
Each row represents a single CVE--ATT&CK technique pair labeled as positive or negative.