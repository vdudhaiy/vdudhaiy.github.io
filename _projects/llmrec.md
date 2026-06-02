---
title: LLM-Rec Paper Reimplementation
start_date: 2025-01-01
end_date: 2025-04-30
layout: default
summary: An individual reimplementation of LLM-Rec (Lyu et al., 2023) for ECE 570 (AI), studying LLM-augmented recommendation on the MovieLens dataset with several intentional modifications to the original approach.
last_updated: 2026-06-02
---

# LLM-Rec Paper Reimplementation
{% if page.start_date %} {{ page.start_date | date: "%b %Y" }}{% endif %}
{% if page.end_date %} — {{ page.end_date | date: "%b %Y" }}
{% else %} — Present {% endif %}

<p style="text-align: right;">
  <small>Last Updated: {{ page.last_updated | date: "%b %-d, %Y" }}</small>
</p>

**ECE 570 — Artificial Intelligence (Graduate-level)** &nbsp;·&nbsp; Purdue University &nbsp;·&nbsp; Individual project

ECE 570 is a graduate-level AI course I took at Purdue. A major component of the course required each student to independently select a recently published AI research paper and either reimplement its core results or explore a new angle on its ideas — using limited compute resources, on their own.

For my project, I chose to reimplement (with several intentional modifications) **[LLM-Rec: Personalized Recommendation via Prompting Large Language Models](https://arxiv.org/abs/2307.02046)** by Lyu et al. (2023), which explores using large language models to augment traditional collaborative filtering pipelines.

## Modifications from the original paper

Rather than a straight reproduction, I made deliberate changes to address limitations or adapt to available resources:

1. **Movie descriptions via TMDB instead of GPT-3 prompting** — The original paper uses GPT-3 to generate movie descriptions from titles, which is prone to hallucination. I instead fetched official synopses from the [TMDB API](https://developer.themoviedb.org/), resulting in grounded, factually accurate descriptions.

2. **Adjusted hyperparameters** — Used an early stopping patience of 10 (vs. 5 in the paper) and adapted other hyperparameters to account for time and compute constraints.

3. **Stricter implicit feedback handling** — The original paper converts explicit ratings (1–5) to binary labels by marking any watched movie as a 1. I assigned a 1 only to movies rated ≥ 2, so that the model treats poorly-rated movies similarly to unwatched ones — capturing whether the user actually liked the movie, not just whether they watched it.

4. **Llama-3.1-8B-Instruct instead of GPT-3** — Used an open-source LLM to avoid API costs and enable local inference.

5. **Basic + recommendation-driven prompts only** — Due to computational overhead, I implemented the two most impactful prompt strategies from the paper rather than all five.

## Evaluation

The model was evaluated on the **MovieLens** dataset using standard recommendation metrics (Hit Rate, NDCG). Key findings:

- LLM-augmented embeddings improved recommendation quality for items with rich textual metadata
- The TMDB-sourced descriptions produced more reliable augmentation than GPT-generated ones
- Cold-start performance improved notably, since the model can reason about an item's description even without interaction history

## Tech stack

Python · PyTorch · Hugging Face Transformers (Llama-3.1-8B-Instruct) · TMDB API · MovieLens dataset · NumPy · Pandas
