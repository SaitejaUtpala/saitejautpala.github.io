---
title: "METR Task Bounty: 10 tasks for measuring AI agents' time horizons"
tldr: "Won $70,214 in METR's Task Bounty for designing 10 ML R&D tasks for evaluating LLM agents. Several are used in METR's time-horizon evaluations of frontier models: some private, some public."
tags: [AI agents, evaluations, ML R&D]
thumbnail: /assets/updates/metr-task-bounty/metr-time-horizon.png
highlight: true
highlight_title: "METR Task Bounty: Time Horizon Evaluations"
highlight_badges: ["Won $70,214"]
highlight_venue: "10 tasks · Used in METR's time-horizon evals · 2024"
highlight_summary: "Designed and implemented 10 ML R&D tasks for evaluating LLM agents. Several are part of METR's time-horizon suite, the benchmark behind the widely cited finding that the length of tasks AI agents can complete is doubling every few months. Some tasks are private, some are public."
links:
  - name: METR Time Horizons
    url: https://metr.org/time-horizons/
  - name: Paper
    url: https://arxiv.org/abs/2503.14499
  - name: METR Blog
    url: https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/
  - name: Public Tasks
    url: https://github.com/METR/public-tasks
---

[METR](https://metr.org/) measures how long a task a frontier AI agent can complete autonomously, where
task length is how long the same task takes a human expert. To do that, they need a large suite of
realistic, well-specified tasks with reliable scoring. Their Task Bounty paid outside experts to build them.

## Highlights

* **Won $70,214** in METR's Task Bounty for designing and implementing ML R&D tasks for evaluating LLM agents.
* **Contributed 10 tasks.** Several of them are private, held out so models can't train on them, and some are public.
* **Used in METR's time-horizon evaluations**, the measurement METR reports for every new frontier model.

## METR's Time Horizon Measurements

{% include figure.html
   src="/assets/updates/metr-task-bounty/metr-time-horizon.png"
   caption="**METR's time-horizon chart.** The length of tasks (measured by human expert time) that frontier models complete with 50% success, by model release date. Doubling time is roughly 4 months. Figure: [METR](https://metr.org/time-horizons/), CC-BY." %}

## What Makes a Good Agent Task

A task for measuring time horizons has to:

* **Take a human expert real time.** Hours, not minutes, so it measures long-horizon work.
* **Be scored automatically and robustly**, so there's no ambiguity about whether the agent succeeded.
* **Resist shortcuts.** The agent shouldn't be able to look the answer up or reward-hack the scorer.
* **Stay uncontaminated.** That's why many tasks are kept private.
