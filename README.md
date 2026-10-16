# Qwen2.5-Coder-3B-Instruct — QLoRA + RAG Evaluation

Artifact repository for a thesis-related **Python code-repair experiment** using **Qwen2.5-Coder-3B-Instruct**. It preserves the public evaluation outputs, checkpoints, summaries, and packaged model/deliverable artifacts used in the experiment.

## Repository scope

This repository is primarily an **experiment-artifact archive**, not a standalone application or complete training pipeline. The public contents include:

- packaged QLoRA/model deliverables
- row-level evaluation checkpoints from the original run
- a completed **2,510-sample** checkpoint for the original evaluation
- improved-prompt checkpoints currently published through **1,000 samples**
- bug-type summary metrics and analysis figures
- intermediate checkpoints retained for experiment provenance and recovery

The training/evaluation notebooks and full end-to-end reproduction code are not currently published in this repository.

## Main artifacts

| Artifact | Purpose |
|---|---|
| `Qwen2.5-Coder-3B-Instruct_QLoRA_3epochs.zip` | Packaged QLoRA training artifact |
| `qwen25_coder_3b_qlora_rag_pathB_deliverables_qwen25coder3b-qlora-rag-pathB-run1.zip` | Packaged experiment deliverables |
| `rag_pathB_checkpoint_qwen25coder3b-qlora-rag-pathB-run1_*samples.csv` | Original evaluation checkpoints, including the final 2,510-sample output |
| `rag_pathB_checkpoint_qwen25coder3b-qlora-rag-pathB-run1_improved_*samples.csv` | Improved-prompt checkpoints currently published through 1,000 samples |
| `bug_type_performance_qwen25coder3b-qlora-rag-pathB-run1.csv` | Bug-type performance summary |
| `bug_type_analysis_qwen25coder3b-qlora-rag-pathB-run1.png` | Bug-type analysis visualization |

The row-level checkpoint CSVs record fields such as dataset source, bug type, buggy code, gold fix, QLoRA prediction/correctness, retrieved fix, RAG prediction/correctness, RAG activation/stage, and error diagnostics.

## Evaluation note

The original public evaluation reaches **2,510 test rows**. Intermediate checkpoint files are intentionally retained to document progress and support recovery/audit of the run.

The bug-type summary is an aggregate view of the completed evaluation and should be interpreted within this experiment's recorded protocol rather than as a general benchmark claim.

## Research caveat

Some retrieval-augmented experiments in the broader thesis workflow use **gold-reference gating** to determine whether retrieval produced a rescue. Those experiments are **oracle-assisted diagnostic upper bounds**, not deployable inference performance.

The broader thesis also studies confidence calibration and adaptive repair decisions. Those stages are separate from the static artifacts published here and remain part of the ongoing research workflow.

## Reproducibility

The repository is useful for inspecting saved predictions, checkpoints, and aggregate outcomes. Reproducing the complete experiment from scratch requires the corresponding training/evaluation code, dataset split, model configuration, and retrieval artifacts, which are not all included here.

## Maintainer

**MD Alif Ziad Sarkar**  
BSc in Computer Science and Engineering, American International University-Bangladesh (AIUB)
