# LLM Fine-Tuning: A Systematic Review

Undergraduate thesis (Pontificia Universidad Católica del Ecuador) - a PRISMA 2020 systematic review of fine-tuning techniques for Large Language Models published between 2020 and 2025.

> Published in PUCE's institutional repository (link pending).

## Abstract

This monograph presents a systematic review of fine-tuning techniques for Large Language Models (LLMs) published between 2020 and 2025, conducted following the PRISMA 2020 protocol. From an initial search of 140 records in Scopus, 84 empirical studies with quantitative evaluation were selected, distributed across four application domains: Health and Biomedicine (35.7%), Language and Humanities (25.0%), Exact Sciences and Computing (23.8%), and Industry and Business (15.5%). The analysis covered nine techniques organized into three paradigms: Full Fine-Tuning and SFT as full-parameter update approaches, five Parameter-Efficient Fine-Tuning methods (LoRA, QLoRA, Adapter Layers, Prefix Tuning, Prompt Tuning), and two alignment methods (RLHF, DPO). Results reveal the dominance of LoRA and its variants, present in 79.8% of included studies, with an acceptable methodological quality of the corpus (average score of 2.61 out of 3.0). Three cross-domain patterns were identified: the consistent effectiveness of fine-tuning over the unadapted base model, the advantage of PEFT techniques in low-resource languages and underrepresented domains, and the trend toward composite architectures in production applications. The findings enable evidence-based technique selection criteria according to operational context, data privacy constraints, and response alignment requirements.

**Keywords:** fine-tuning, Large Language Models, LoRA, Parameter-Efficient Fine-Tuning, RLHF, DPO, systematic review, PRISMA, natural language processing, empirical evaluation.

## Repository contents

- `monografia/` - LaTeX source and compiled PDF of the full thesis.
- `poster/` - LaTeX source and compiled PDF of the defense poster.
- `pipeline/` - Jupyter notebooks for the PRISMA screening pipeline (article retrieval, three-phase screening, results visualization) and the resulting per-phase screening data (`pipeline/exports/`).

## Not included

The raw PDFs of the 84+ screened papers are excluded from this repository - they are copyrighted material from their respective publishers and cannot be redistributed. The pipeline notebooks document the retrieval and screening methodology; the results CSVs in `pipeline/exports/` record the screening outcomes.
