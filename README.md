# Qwen2.5-Coder-3B-Instruct — QLoRA + RAG Testing

Code-repair evaluation repository for **Qwen2.5-Coder-3B-Instruct** using a QLoRA + retrieval-augmented generation workflow.

## What is published

- Progressive RAG evaluation checkpoint CSVs
- A completed **2,510 / 2,510** evaluation checkpoint in the repository history
- Per-bug-type performance CSV
- Bug-type analysis visualization
- Packaged experiment deliverables
- A later improved-prompt experiment with its own checkpoint series

## Reading the results correctly

This repository contains multiple experiment stages. Do not mix metrics from the original completed run with the later improved-prompt checkpoints unless they were produced under the same protocol and are explicitly being compared.

The many checkpoint CSVs are resume/progress artifacts; the completed run and its final deliverables should be used when reporting final results for that protocol.

## Repository purpose

The repository is an experiment record and result archive rather than a production inference package. It is intended to make model testing, progress, and per-bug-type analysis inspectable.

## Author

MD Alif Ziad Sarkar — CSE, American International University-Bangladesh (AIUB)
