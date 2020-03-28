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

<snippet>
    <content><![CDATA[
        {% assign ${1:mydata}=${2:site.data.temp} %}
        <table>
            <caption>${3:Table caption}</caption>
            <thead>
            {% for column in ${1:mydata}[0] %}
                <th>{{ column[0] }}</th>
            {% endfor %}
            </thead>
            <tbody>
            {% for row in ${1:mydata} %}
                <tr>
                {% for cell in row %}
                    <td>{{ cell[1] }}</td>
                {% endfor %}
                </tr>
            {% endfor %}
            </tbody>
        </table>
]]></content>
    <tabTrigger>;jekylltable</tabTrigger>
    <!-- Optional: Set a scope to limit where the snippet will trigger -->
    <!-- <scope>source.python</scope> -->
    <description>Create Liquid HTML based on Jekyll datafile</description>
</snippet>

<!-- <ul>
{% for member in site.data.temp %}
  <li>
  	  {{ temp.study_id }}
      {{ temp.,study_name }}
      {{ temp.codeset }}
  </li>
{% endfor %}
</ul> -->