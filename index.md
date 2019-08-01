<section class="newest">
  {% assign post = site.posts.first %}
  <article>
    <heading>
      <h1>{{ post.title }}</h1>
      {% if post.subtitle %}
        <h2>{{ post.subtitle }}</h2>
      {% endif %}

      {% assign author = site.authors[post.author] %}
      {% if post.author %}
        {%
          include byline.html
          name=author.name
          gravatar=author.gravatar
          description=author.description
          date=post.date
        %}
      {% endif %}
    </heading>

    <section>
      <p>{{ post.excerpt }}</p>
      <p><a href="{{ post.url | prepend: site.baseurl }}">Read more…</a></p>
    </section>
  </article>

</section>

<section class="recent">
  <h2>Older Stories</h2>

  <ul>
  {% for post in site.posts offset:1 limit:10 %}
    <li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
  {% endfor %}
  </ul>
</section>

