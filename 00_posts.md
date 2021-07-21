---
layout: page 
title: Posts
permalink: /posts/
---

<div class="home">

  {%for post in site.posts %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <h3>{{ post.date | date: '%Y' }}</h3>
      {% endif %}
      <li>
		<a href="{{ post.url }}">{{ post.title }}</a>
		-
		<time>{{ post.date | date:"%b %d" }}</time>
      </li>
  {% endfor %}
</div>
