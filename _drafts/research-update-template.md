---
# HOW TO PUBLISH
# 1. Copy this file to _posts/YYYY-MM-DD-short-slug.md   (e.g. _posts/2026-11-02-looped-udlm.md)
# 2. Put images/videos in assets/updates/short-slug/
# 3. Fill in the fields below, delete sections you don't need, commit & push.
# Files in _drafts/ are never published on GitHub Pages.
#
# Preview locally (with drafts):  bundle exec jekyll serve --drafts

title: "TEMPLATE: Headline result in one line"
tldr: "One-sentence takeaway. This shows on the Updates list, the homepage and at the top of the post."
tags: [diffusion LMs, efficiency]                         # shown as small chips
authors: "Saiteja Utpala, Chieh-Hsin Lai, Yuki Mitsufuji, Praneeth Vepakomma"   # optional
thumbnail: /assets/updates/example-update/thumb.png      # optional, used on the Updates list
math: true                                               # enables $inline$ and $$display$$ LaTeX
links:                                                   # optional buttons under the title
  - name: Paper
    url: https://arxiv.org/abs/2610.30066
  - name: Code
    url: https://github.com/SaitejaUtpala
  - name: Thread
    url: https://x.com/
---

## Key Update

What changed since last time, in 2-3 sentences. Lead with the result, not the setup.

{% include figure.html
   src="/assets/updates/example-update/main-result.png"
   caption="**Figure 1.** Main result. Say what the reader should notice: *looped models reach the AR baseline at half the training FLOPs.*" %}

## Key Results

| Model | Params | Train FLOPs | Val PPL ↓ | Notes |
|---|---|---|---|---|
| AR baseline | 350M | 1.0x | 18.2 | |
| Uniform diffusion | 350M | 1.0x | 21.5 | |
| **Looped uniform diffusion (ours)** | 350M | **0.5x** | **18.0** | 4 loops |
{: .update-results}

* **Finding 1:** short claim, backed by a number.
* **Finding 2:** short claim, backed by a number.
* **Surprise / negative result:** what didn't work and why that matters.

## Method in One Paragraph

Plain-language description of the idea. Equations work when `math: true`, e.g. inline $p_\theta(x_0 \mid x_t)$ or display:

$$
\mathcal{L}(\theta) = \mathbb{E}_{t, x_0, x_t}\left[ w(t)\, \mathrm{KL}\big(q(x_{t-1}\mid x_t, x_0) \,\|\, p_\theta(x_{t-1}\mid x_t)\big) \right]
$$

## Visualizations

A video file (mp4/webm) stored in the repo. Drop `autoplay=true` to show player controls instead of a silent looping GIF-style clip:

{% include video.html
   src="/assets/updates/example-update/denoising.mp4"
   poster="/assets/updates/example-update/thumb.png"
   autoplay=true
   caption="**Video 1.** Denoising trajectory: tokens are refined in parallel across loop iterations." %}

Side-by-side comparison:

{% include compare.html
   left="/assets/updates/example-update/baseline.png" left_label="Baseline"
   right="/assets/updates/example-update/ours.png" right_label="Ours"
   caption="**Figure 2.** Same prompt, same compute budget." %}

A YouTube talk or demo (just the video id):

{% include youtube.html id="dQw4w9WgXcQ" caption="**Video 2.** 5-minute talk." %}

Optional sizes for figures and videos: `size="small"` (60% width) or `size="wide"` (wider than the text on desktop).

## What's Next

* Next experiment / open question.
* What I'd love feedback on. Reach out at [saitejautpala@gmail.com](mailto:saitejautpala@gmail.com).
