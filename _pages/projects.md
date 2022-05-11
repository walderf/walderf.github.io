---
title:
layout: default
permalink: /things/
published: true
---


<div class="ProjectContainer">

	<div class="gallery">


  {% for project in site.projects %}

  {% if project.redirect %}

          <span>
              <a href="{{ project.redirect }}" target="_blank"><h3>{{ project.title }}</h3></a>
              <p><small>{{ project.description }}</small></p>
          </span>

  {% else %}

          <span>
              <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}"><h3>{{ project.title }}</h3></a>
              <p><small>{{ project.description }}</small></p>
          </span>

  {% endif %}

  {% endfor %}

	</div>

</div>
