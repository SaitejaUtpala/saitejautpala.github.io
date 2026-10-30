---
layout: default
---

## About Me

Hi! I am a researcher at [MBZUAI](https://mbzuai.ac.ae/), Abu Dhabi, working on **diffusion language models**.
Previously, I was a Research Engineer at Princeton University working on the reliability of AI agents, and a
Research SDE at Microsoft Research on the GitHub Copilot Workspace team.
I hold a Masters in Computer Science and Engineering from IIT Kanpur.

[Email](mailto:saitejautpala@gmail.com) / [GitHub](https://github.com/SaitejaUtpala) / [Google Scholar](https://scholar.google.com/citations?hl=en&user=5oBTAV8AAAAJ&view_op=list_works&sortby=pubdate) / [Resume](resume.pdf)

{% assign highlights = site.posts | where: "highlight", true %}
{% if highlights.size > 0 %}
## Selected Work

<div class="highlight-list">
{% for post in highlights %}
  <div class="highlight">
    <a class="highlight-thumb" href="{{ post.url | relative_url }}"><img src="{{ post.thumbnail | relative_url }}" alt="" loading="lazy"></a>
    <div class="highlight-body">
      <a class="highlight-title" href="{{ post.url | relative_url }}">{{ post.highlight_title | default: post.title }}</a>
      {% if post.highlight_badges or post.highlight_venue %}<p class="highlight-venue">{% for badge in post.highlight_badges %}<span class="highlight-badge">{{ badge }}</span> {% endfor %}{{ post.highlight_venue }}</p>{% endif %}
      <p>{{ post.highlight_summary | default: post.tldr }}</p>
    </div>
  </div>
{% endfor %}
</div>
{% endif %}
