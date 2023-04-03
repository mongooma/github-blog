---
layout: page
permalink: /graphs/
title: On Graphs
---

<div id="archives">
{% for tag in site.tags %} 
  {% capture tag_name %}{{ tag | first }}{% endcapture %}
  {% if tag_name contains "Graph" %} 
    <!-- Currently only predefined vars are usable? -->
    <div class="archive-group">
      <div id="#{{ tag_name | slugize }}"></div>
      <p></p>
      <h3 class="category-head">{{ tag_name }}</h3>

      {% for post in site.tags[tag_name] %}
      <article class="archive-item">
        <h4><a href="{{ post.url }}">{{post.title}}</a></h4>
      </article>
      {% endfor %}
    </div>
  {% endif %}
{% endfor %}
</div>