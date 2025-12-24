---
layout: default
title: Works
---

<section class="works-list">
  {% for post in site.posts %}
    <article class="work-card">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p class="meta">
        by {{ post.penname | default: post.author }} •
        {{ post.genre }} •
        {{ post.date | date: "%B %d, %Y" }}
      </p>
      <p>{{ post.excerpt }}</p>
      <a class="read-more" href="{{ post.url }}">Read →</a>
    </article>
  {% endfor %}
</section>
