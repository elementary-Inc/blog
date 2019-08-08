---
---

<section class="tag-list">
{% assign tags = site.tags | sort %}
{% for tag in tags %}
  <h2 id="{{ tag[0] | replace: ' ', '-' }}">#{{ tag[0] }}</h2>

  {% assign posts = tag[1] | sort %}
  {% for post in posts %}
    {% include featured.html post=post %}
  {% endfor %}
{% endfor %}
</section>

