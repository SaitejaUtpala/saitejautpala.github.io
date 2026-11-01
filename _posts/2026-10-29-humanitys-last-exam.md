---
title: "Humanity's Last Exam: ~20 questions, a Top-50 hardest pick, and a Kimi K2 showcase"
tldr: "I contributed nearly 20 questions in Differential Geometry and Theoretical Statistics to Humanity's Last Exam (ranked #29 of 1,015 contributors). One symplectic geometry question was selected among the Top 50 hardest, and Kimi K2 Thinking showcased my question on statistics on hyperbolic manifolds."
tags: [benchmarks, LLM evaluation, math]
thumbnail: /assets/updates/humanitys-last-exam/kimi-k2-hyperbolic-question.png
highlight: true
highlight_title: "Humanity's Last Exam"
highlight_badges: ["Won $5,000", "Top 50 Hardest Question"]
highlight_venue: "2024"
highlight_summary: "Ranked #29 of 1,015 contributors. Covered by The New York Times. Contributed nearly 20 frontier-level questions in Differential Geometry and Theoretical Statistics. One of my symplectic geometry questions was selected among the Top 50 hardest in the benchmark, and Moonshot AI used my question on statistics on hyperbolic manifolds to showcase Kimi K2 Thinking."
math: true
links:
  - name: Paper
    url: https://arxiv.org/abs/2501.14249
  - name: HLE Website
    url: https://lastexam.ai/
  - name: NYT Coverage
    url: https://www.nytimes.com/2025/01/23/technology/ai-test-humanitys-last-exam.html
  - name: Kimi K2 Thinking
    url: https://www.kimi.com/en/blog/kimi-k2-thinking
---

[Humanity's Last Exam (HLE)](https://lastexam.ai/) is a benchmark of expert-written questions at the frontier
of human knowledge, built by the Center for AI Safety and Scale AI. Every question had to stump frontier
LLMs before it was accepted. It's now one of the standard benchmarks frontier labs report on.

## Highlights

* **Contributed nearly 20 questions** in **Differential Geometry** and **Theoretical Statistics**.
* **Ranked #29 of 1,015 contributors** by number of contributions (top 3%).
* **Top 50 hardest question, won $5,000.** One of my questions in **symplectic geometry** was selected as one of the
  Top 50 hardest questions in the whole benchmark.
* **Covered by The New York Times.** HLE was featured in
  [*"When A.I. Passes This Test, Look Out"*](https://www.nytimes.com/2025/01/23/technology/ai-test-humanitys-last-exam.html)
  (Kevin Roose, Jan 2025).
* **Showcased in the Kimi K2 Thinking release.** Moonshot AI's
  [Kimi K2 Thinking blog post](https://www.kimi.com/en/blog/kimi-k2-thinking) used a question I designed
  on **statistics on hyperbolic manifolds** to demonstrate the model's step-by-step reasoning on HLE.

## The Kimi K2 Question

{% include figure.html
   src="/assets/updates/humanitys-last-exam/kimi-k2-hyperbolic-question.png"
   caption="**My HLE question as shown in the Kimi K2 Thinking release.** The model must compute the exact log-density $\ell_k(n)$ of a distribution sampled on the hyperbolic space $\mathbb{L}^n$ (Lorentz model), with a structured covariance $\Sigma$, as a closed-form function of $n$ and $k = \ln(\sqrt{2}+1)$." %}

The question requires putting several pieces together: the sampling procedure on the Lorentz model, the
change-of-variables correction for the exponential map on hyperbolic space, and the inverse and determinant
of a non-trivial covariance matrix. A model can't pattern-match its way to the answer. It has to carry
out the derivation correctly end to end.

## Why This Matters

Benchmarks like MMLU are saturated, so measuring frontier reasoning needs questions that experts can verify
but models can't easily answer. Writing them taught me a lot about where LLM reasoning breaks: long chains of
exact symbolic computation, and geometric structure that has to be tracked carefully at every step.
