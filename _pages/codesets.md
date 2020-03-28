---
layout: archive
permalink: /codesets/
title: "Search the Codesets in the Codeset Library"
author_profile: true
---
{% assign mydata=site.data.temp %}

<table>
    <caption>Table caption</caption>
    <thead>
    {% for column in mydata[0] %}
        <th>{{ column[0] }}</th>
    {% endfor %}
    </thead>
    <tbody>
    {% for row in mydata %}
        <tr>
        {% for cell in row %}
            <td>{{ cell[1] }}</td>
        {% endfor %}
        </tr>
    {% endfor %}
    </tbody>
</table>

<!-- <ul>
{% for member in site.data.temp %}
  <li>
  	  {{ temp.study_id }}
      {{ temp.,study_name }}
      {{ temp.codeset }}
  </li>
{% endfor %}
</ul> -->