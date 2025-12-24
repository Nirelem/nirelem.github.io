---
layout: default
title: Home
---

<section class="intro">
  <h2>Welcome to {{ site.title }}</h2>

  <p class="intro-text">
    We are a student writing organization celebrating creative work
    across all genres — poetry, fiction, essays, and more.
  </p>
</section>

<section class="featured">
  <h3>Featured Work</h3>

  {% for post in site.posts %}
    {% if post.featured %}
      <article class="work-card featured-card">
        <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
        <p class="meta">
          by {{ post.penname | default: post.author }} • {{ post.genre }}
        </p>
        <p>{{ post.excerpt }}</p>
        <a class="read-more" href="{{ post.url }}">Read more →</a>
      </article>
    {% endif %}
  {% endfor %}
</section>

<section class="recent">
  <h3>Recent Works</h3>

  {% for post in site.posts limit:5 %}
    <article class="work-card">
      <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
      <p class="meta">
        by {{ post.penname | default: post.author }} • {{ post.genre }}
      </p>
      <p>{{ post.excerpt }}</p>
      <a class="read-more" href="{{ post.url }}">Read →</a>
    </article>
  {% endfor %}
</section>
