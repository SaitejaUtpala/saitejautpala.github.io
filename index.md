---
layout: default
---

## About Me

Currently I am a researcher at MBZUAI, working on diffusion language models.
Previously, I was a Research Engineer at Princeton University working on the reliability of AI agents, and a
Research SDE at Microsoft Research.
Before that, I worked on geometric machine learning and statistics, differential privacy, and nonparametric statistics.
I hold a Masters in Computer Science and Engineering from IIT Kanpur.

[Email](mailto:saitejautpala@gmail.com) / [GitHub](https://github.com/SaitejaUtpala) / [Google Scholar](https://scholar.google.com/citations?hl=en&user=5oBTAV8AAAAJ&view_op=list_works&sortby=pubdate)

{% assign highlights = site.posts | where: "highlight", true %}
{% if highlights.size > 0 %}
## Selected Work

<div class="highlight-list">
{% for post in highlights %}
  <div class="highlight">
    <div class="highlight-thumb"><img src="{{ post.thumbnail | relative_url }}" alt="" loading="lazy"></div>
    <div class="highlight-body">
      <span class="highlight-title">{{ post.highlight_title | default: post.title }}</span>
      {% if post.highlight_badges or post.highlight_venue %}<p class="highlight-venue">{% for badge in post.highlight_badges %}<span class="highlight-badge">{{ badge }}</span> {% endfor %}{{ post.highlight_venue }}</p>{% endif %}
      {{ post.highlight_summary | default: post.tldr | markdownify }}
    </div>
  </div>
{% endfor %}
</div>
{% endif %}
