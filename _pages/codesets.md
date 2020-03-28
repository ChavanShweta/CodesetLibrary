---
layout: archive
permalink: /codesets/
title: "Search the Codesets in the Codeset Library"
author_profile: true
---
<!-- <script src="http://d3js.org/d3.v3.min.js"></script> -->
<script src="d3.min.js?v=3.2.8"></script>

<script type="text/javascript"charset="utf-8">
    d3.text("site.data.temp", function(data) {
        var parsedCSV = d3.csv.parseRows(data);

        var container = d3.select("body")
            .append("table")

            .selectAll("tr")
                .data(parsedCSV).enter()
                .append("tr")

            .selectAll("td")
                .data(function(d) { return d; }).enter()
                .append("td")
                .text(function(d) { return d; });
    });
</script>
<!-- <ul>
{% for member in site.data.temp %}
  <li>
  	  {{ temp.study_id }}
      {{ temp.,study_name }}
      {{ temp.codeset }}
  </li>
{% endfor %}
</ul> -->