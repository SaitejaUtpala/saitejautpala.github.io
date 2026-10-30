---
title: "Looped Uniform Diffusion Language Models"
date: 2026-10-30 12:00:00 +0400
tldr: "Looping a few early Transformer layers inside each denoising step makes uniform diffusion LMs, the family behind DiffusionGemma, up to 3.3x cheaper to train. Result of ~20,000 H100 hours of experiments."
tags: [diffusion LMs, efficiency, looping]
thumbnail: /assets/updates/looped-udlm/thumb.png
highlight: true
highlight_title: "Looped Uniform Diffusion Language Models"
highlight_venue: "Preprint · 2026"
highlight_summary: "Uniform diffusion LMs, the backbone of Google's DiffusionGemma, revise any token while denoising but are expensive to train. We spent ~20,000 H100 hours studying looping in UDLMs: looped models match a non-looped UDLM trained on ~0.5T tokens with up to 3.3x fewer training FLOPs."
links:
  - name: Paper
    url: https://arxiv.org/abs/2610.30066
---

**Saiteja Utpala**, Chieh-Hsin Lai, Yuki Mitsufuji and Praneeth Vepakomma. Preprint, 2026.

## Why Uniform Diffusion?

Uniform diffusion language models (UDLMs) generate text by iteratively denoising sequences of ordinary
vocabulary tokens, and **any token can be revised** at any step. Masked diffusion LMs (MDLMs) instead
commit tokens once they're unmasked. Uniform-state diffusion is the generation backbone of Google's
[DiffusionGemma](https://ai.google.dev/gemma/docs/diffusiongemma), precisely because it allows continuous
self-correction.

The catch: UDLMs must learn to denoise from a context that may itself be corrupted, which makes them
**more FLOP-intensive to train** than MDLMs, even though they yield stronger downstream reasoning.

## The Compute Behind This Study

We spent **~20,000 H100 hours** systematically studying
**looping** in UDLMs. Looping recursively applies a few early Transformer layers within each denoising
step, keeping the training objective and sampler unchanged.

## Key Result: Up to 3.3x Fewer Training FLOPs

{% include figure.html
   src="/assets/updates/looped-udlm/training-elbow-grid.png"
   caption="**Validation NLL vs. cumulative training FLOPs** on OpenWebText (top) and FineWeb-Edu (bottom), for uniform and FLOP-proportional loop-count sampling. Looped UDLMs (solid) reach the final validation NLL of the non-looped baseline trained for 10⁶ steps (~0.5T tokens; dotted) with **2.7–2.8x fewer FLOPs on OpenWebText** and **3.2–3.3x fewer on FineWeb-Edu**." %}

* **Training efficiency:** up to **2.8x** fewer FLOPs on OpenWebText and **3.3x** on FineWeb-Edu to match the non-looped UDLM.
* **Better generation:** at a matched NFE budget, looped UDLMs reach up to **9.8% lower generation perplexity**, with most gains at moderate loop counts.
* **Cheaper inference:** sampling smaller loop counts more often during training lets the model use **12% fewer loops** on downstream tasks, with no loss in accuracy.
