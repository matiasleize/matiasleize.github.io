---
layout: archive
title: "Code"
permalink: /code/
author_profile: true
---

{% include base_path %}

Open-source software I develop for my research. You can find all my repositories on [GitHub](https://github.com/{{ site.author.github }}).

{% for repo in site.data.code %}
<div class="repo-card">
  <h2 class="repo-card__title"><a href="{{ repo.github }}"><i class="fab fa-fw fa-github" aria-hidden="true"></i> {{ repo.name }}</a></h2>
  <p class="repo-card__language"><i class="fas fa-fw fa-code" aria-hidden="true"></i> {{ repo.language }}</p>
  <p>{{ repo.description }}</p>
  {% if repo.install %}<pre class="repo-card__install"><code>{{ repo.install }}</code></pre>{% endif %}
  {% if repo.paper_url %}<p class="repo-card__paper">Related paper: <a href="{{ repo.paper_url }}">{{ repo.paper_title }}</a></p>{% endif %}
  <p class="publication__links">
    <a class="btn" href="{{ repo.github }}"><i class="fab fa-fw fa-github" aria-hidden="true"></i> GitHub</a>
    {% if repo.pypi %}<a class="btn" href="{{ repo.pypi }}"><i class="fab fa-fw fa-python" aria-hidden="true"></i> PyPI</a>{% endif %}
  </p>
</div>
{% endfor %}
