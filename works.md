---
layout: default
title: Works
---

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})

By {{ post.author }}  
*{{ post.genre }}* — {{ post.date | date: "%B %d, %Y" }}

{{ post.excerpt }}

---
{% endfor %}
