# LLM Fine-Tuning: A Systematic Review

A PRISMA 2020 systematic review of empirical fine-tuning research for Large Language Models, published 2020-2025. Undergraduate thesis, Pontificia Universidad Católica del Ecuador (PUCE), 2026.

> Submitted and archived at PUCE's library (print/physical indexing - no institutional digital repository).

## Why this review

Fine-tuning technique selection for LLMs is usually guided by which method is trending, not by what the empirical evidence across domains actually supports. This review consolidates 84 empirical studies (2020-2025) that quantitatively evaluate a fine-tuning technique, to answer: which techniques are actually used in practice, in which domains, with what methodological rigor, and what patterns hold across all of them.

## Abstract

This monograph presents a systematic review of fine-tuning techniques for Large Language Models (LLMs) published between 2020 and 2025, conducted following the PRISMA 2020 protocol. From an initial search of 140 records in Scopus, 84 empirical studies with quantitative evaluation were selected, distributed across four application domains: Health and Biomedicine (35.7%), Language and Humanities (25.0%), Exact Sciences and Computing (23.8%), and Industry and Business (15.5%). The analysis covered nine techniques organized into three paradigms: Full Fine-Tuning and SFT as full-parameter update approaches, five Parameter-Efficient Fine-Tuning methods (LoRA, QLoRA, Adapter Layers, Prefix Tuning, Prompt Tuning), and two alignment methods (RLHF, DPO). Results reveal the dominance of LoRA and its variants, present in 79.8% of included studies, with an acceptable methodological quality of the corpus (average score of 2.61 out of 3.0). Three cross-domain patterns were identified: the consistent effectiveness of fine-tuning over the unadapted base model, the advantage of PEFT techniques in low-resource languages and underrepresented domains, and the trend toward composite architectures in production applications. The findings enable evidence-based technique selection criteria according to operational context, data privacy constraints, and response alignment requirements.

**Keywords:** fine-tuning, Large Language Models, LoRA, Parameter-Efficient Fine-Tuning, RLHF, DPO, systematic review, PRISMA, natural language processing, empirical evaluation.

## Methodology

PRISMA 2020 protocol, implemented as a three-phase screening pipeline (see `pipeline/`):

1. **Retrieval** - 140 records identified via a Scopus search (`Download_Articles.ipynb`).
2. **Phase 1 - Title/abstract screening** (`Screening-1.ipynb`): eligibility criteria applied to titles and abstracts.
3. **Phase 2 - Full-text eligibility** (`Screening-2.ipynb`): full-text review against 5 inclusion questions (quantitative metrics, fine-tuning technique, dataset, NLP context, empirical evaluation).
4. **Phase 3 - Quality assessment** (`Screening-3.ipynb`): 3-criterion methodological quality scoring (data split reporting, hyperparameter reporting, dataset characterization), yielding the final 84 included studies.
5. **Synthesis** (`Graficos-Monografia.ipynb`): domain/technique distribution analysis and the figures used in the thesis.

## Key findings

- **Technique dominance:** LoRA and its variants appear in 79.8% of included studies, ahead of the other 8 techniques analyzed combined.
- **Domain distribution:** Health and Biomedicine leads (35.7%), followed by Language and Humanities (25.0%), Exact Sciences and Computing (23.8%), and Industry and Business (15.5%).
- **Corpus quality:** average methodological quality score of 2.61/3.0 across the 84 included studies.
- **Cross-domain patterns:** (1) fine-tuning consistently outperforms the unadapted base model, (2) PEFT techniques show a particular advantage in low-resource languages and underrepresented domains, (3) production applications trend toward composite architectures (combining multiple techniques) rather than a single method.

Full detail, per-domain breakdowns, and the evidence-based technique selection criteria are in `monografia/mainMonografia.pdf` (Chapter 6, Results).

## Repository contents

```
monografia/     LaTeX source and compiled PDF of the full thesis
poster/         LaTeX source and compiled PDF of the defense poster
pipeline/       PRISMA screening pipeline notebooks
```

## Reading the work

- Full thesis (Spanish, with English abstract): [`monografia/mainMonografia.pdf`](monografia/mainMonografia.pdf)
- Defense poster: [`poster/mainMonografia.pdf`](poster/mainMonografia.pdf)

## Not included

- The raw PDFs of the 84+ screened papers - copyrighted material from their respective publishers, not redistributable.
- Per-paper screening/QA decision exports - intermediate working data from the review process, not included here to keep the repository focused on the reviewable methodology (the notebooks) and the final results (the thesis itself).

## Citation

```
Flores, F. (2026). LLM Fine-Tuning: A Systematic Review [Undergraduate thesis,
Pontificia Universidad Católica del Ecuador].
```

## License

- Thesis, poster, and figures (`monografia/`, `poster/`): [CC BY-NC 4.0](LICENSE-THESIS) - share and adapt with attribution, non-commercial.
- Pipeline code (`pipeline/`): [MIT](LICENSE).
