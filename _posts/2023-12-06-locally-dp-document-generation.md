---
title: "Locally Differentially Private Document Generation Using Zero Shot Prompting"
tldr: "DP-Prompt paraphrases documents with an LLM under local differential privacy, cutting author-identification F1 by up to 73% while keeping downstream utility. EMNLP 2023 (Findings)."
tags: [LLMs, differential privacy]
thumbnail: /assets/updates/ldp-prompt/thumb.png
highlight: true
highlight_title: "Locally Differentially Private Document Generation"
highlight_badges: ["EMNLP 2023"]
highlight_venue: "Findings · with Sara Hooker and Pin-Yu Chen"
highlight_summary: "DP-Prompt uses zero-shot LLM paraphrasing to rewrite documents under local differential privacy. It cuts author-identification F1 by up to 73% on IMDB and Yelp while keeping sentiment utility close to the clean text."
links:
  - name: Paper
    url: https://arxiv.org/abs/2310.16111
---

**Saiteja Utpala**, Sara Hooker and Pin-Yu Chen. Accepted at EMNLP 2023 (Findings).

Large language models can be prompted to paraphrase a document. We use that as a
**local differentially private** rewriting mechanism, **DP-Prompt**: the document never leaves
the user's machine in the clear, and the paraphrased text is what gets released.

{% include figure.html
   src="/assets/updates/ldp-prompt/privacy-utility.png"
   caption="**Privacy–utility trade-off.** Author-identification F1 (x) vs. sentiment F1 (y) on IMDB and Yelp, under static and adaptive attackers. DP-Prompt (ChatGPT) sits at the top-left of each panel: large drops in author identification (up to **73%** on Yelp) with utility close to the clean documents." %}
