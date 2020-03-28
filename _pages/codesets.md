---
layout: archive
permalink: /search-codesets/
title: "Search the Codesets in the Codeset Library"
author_profile: true
header:
  image: "/images/pedsnet_qr.png"
---
{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
	{% assign posts = group_items[forloop.index0] %}
	<h2 id="{{ tag | sluify }}" class="archive__subtitle">{{ tag }}</h2>
	{% for post in posts %}
  	   {% include archive-single.html %}
	{% endfor %}
{% endfor %}