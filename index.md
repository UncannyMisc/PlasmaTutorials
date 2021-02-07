---
layout: default
title: Plasma Tutorials
---

Welcome to the main page for Tutorials about (Plasma Engine)[https://github.com/PlasmaEngine/PlasmaEngine], a custom engine built from the ground up with a variety of features. Documentation about various aspect of the engine can be found (Here)[https://github.com/PlasmaEngine/PlasmaDocs].

<div class="grid">
  {% assign startrow = true %}
  {% for post in site.posts %}
    <div class="grid-item">
		{% if startrow == true%}
			<div style = "width: 100%; float:left;">
				<a href="{{ post.url }}" title = "{{ post.title }}">
					<div style = "float:left; background-image:url({{ post.post_image }});">{{ post.title }}</div>
				</a>
				<div style = "width: -webkit-fill-available;">
					<p style = "text-align: center; line-height: normal;">
						{{ post.summary }}
					</p>
				</div>
			</div>
			{% assign startrow = false %}
		{% else %}
			<div style = "width: 100%; float:right;" >
				<a href="{{ post.url }}" title = "{{ post.title }}">
					<div style = "float:right; background-image:url({{ post.post_image }});">{{ post.title }}</div>
				</a>
				<div style = "width: -webkit-fill-available;" >
					<p style = "text-align: center; line-height: normal;">
						{{ post.summary }}
					</p>
				</div>
			</div>
			{% assign startrow = true %}
		{% endif %}
    </div>
  {% endfor %}
</div>