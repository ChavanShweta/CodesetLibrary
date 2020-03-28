---
layout: archive
permalink: /codesets/
title: "Search the Codesets in the Codeset Library"
author_profile: true
--- 
<script type="text/javascript">
$.get('/_data/temp.csv', function(data) {
var build = '<table border="1" cellpadding="2" cellspacing="0" style="border-collapse: collapse" width="100%">\n';
var head = data.split("\n");
for(var i=0;i<1;i++){
build += "<tr><th>" + head[i] + "</th></tr>";
for(var i=1;i<head.length;i++){
build += "<tr><td>" + head[i].split("\n") + "</td></tr>";
}
}
build += "</table>";
$('#wrap').append(build);
});
</script>

<!-- {% assign mydata=site.data.temp %}

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
 -->
<!-- <ul>
{% for member in site.data.temp %}
  <li>
  	  {{ temp.study_id }}
      {{ temp.,study_name }}
      {{ temp.codeset }}
  </li>
{% endfor %}
</ul> -->