---
title:
layout: default
permalink: /things/
published: true
---


<div class="things">

	<div>


  {% for thing in site.things %}

  {% if thing.redirect %}

          <span>
              <a href="{{ thing.redirect }}" target="_blank"><h3>{{ thing.title }}</h3></a>
              <p><small>{{ thing.description }}</small></p>
          </span>

  {% else %}

          <span>
              <a href="{{ thing.url | prepend: site.baseurl | prepend: site.url }}"><h3>{{ thing.title }}</h3></a>
              <p><small>{{ thing.description }}</small></p>
          </span>

  {% endif %}

  {% endfor %}

	</div>

</div>
