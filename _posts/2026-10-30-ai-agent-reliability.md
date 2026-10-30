---
title: "Towards a Science of AI Agent Reliability (ICML 2026)"
tldr: "Agents keep getting more accurate, but not much more reliable. We propose 12 metrics across consistency, robustness, predictability and safety, evaluate 15 frontier agents, and find reliability lagging far behind accuracy. Accepted at ICML 2026."
tags: [AI agents, reliability, evaluations]
thumbnail: /assets/updates/agent-reliability/thumb.png
highlight: true
highlight_title: "Towards a Science of AI Agent Reliability"
highlight_badges: ["ICML 2026"]
highlight_venue: "15 agents · 12 reliability metrics · 2025"
highlight_summary: "Rising accuracy hides how unpredictably agents fail. We decompose agent reliability into 12 metrics across consistency, robustness, predictability and safety, and show that over two years of frontier models, accuracy climbed steeply while reliability barely moved."
links:
  - name: Paper (ICML 2026)
    url: https://arxiv.org/abs/2602.16666
  - name: Interactive Dashboard
    url: https://hal.cs.princeton.edu/reliability/
  - name: Code
    url: https://github.com/steverab/hal-harness
---

**Accepted at ICML 2026.**
Stephan Rabanser, Sayash Kapoor, Peter Kirgis, Kangheng Liu, **Saiteja Utpala**, Arvind Narayanan.

AI agents are increasingly deployed to carry out important tasks, and benchmark accuracy is climbing fast.
In practice, though, agents still fail unpredictably. A single success rate hides whether an agent behaves
**consistently** across runs, stays **robust** to perturbations, fails **predictably**, and keeps errors
**safe** and bounded. Drawing on safety-critical engineering, we propose **12 concrete metrics** across these
four dimensions and use them to evaluate **15 frontier agents** on GAIA and τ-bench.

## Key Finding: Reliability Lags Behind Accuracy

{% include figure.html
   src="/assets/updates/agent-reliability/reliability-trends.png"
   caption="**Reliability trends across Anthropic, Google and OpenAI agents.** *Left:* accuracy rises steeply with release date (+0.22/yr). *Middle:* overall reliability improves far more slowly (+0.06/yr). *Right:* reliability vs. accuracy. From the [interactive dashboard](https://hal.cs.princeton.edu/reliability/)." %}

* **Capability ≠ reliability.** Over 24 months of model releases, accuracy improved roughly 4x faster than overall reliability.
* **Consistency is still low.** Agents that *can* solve a task often fail to solve it *every time*.
* **Gains are uneven.** Structured environments show moderate reliability gains, while open-ended tasks show barely any, even for the latest models.

## My Role

I was a **Research Engineer** on this project at Princeton. I built evaluation infrastructure using
[Inspect AI](https://inspect.aisi.org.uk/) and [Inspect SWE](https://github.com/meridianlabs-ai/inspect_swe)
for evaluating agents at scale.
