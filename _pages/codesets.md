---
layout: archive
permalink: /codesets/
title: "Search the Codesets in the Codeset Library"
author_profile: true
--- 
<!-- <script type="text/javascript">
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
</script> -->
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.20/css/jquery.dataTables.min.css">
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/buttons/1.6.1/css/buttons.dataTables.min.css">

{% assign mydata=site.data.temp %}

<table id="example" class="display nowrap" style="width:100%">
    <caption>Codeset Library</caption>
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

<script type="text/javascript" src="https://code.jquery.com/jquery-3.3.1.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/1.10.20/js/jquery.dataTables.min.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.6.1/js/dataTables.buttons.min.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.6.1/js/buttons.flash.min.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.1.3/jszip.min.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/pdfmake/0.1.53/pdfmake.min.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.6.1/js/buttons.html5.min.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.6.1/js/buttons.print.min.js"></script>

<script type="text/javascript">
    $('#example').DataTable( {
        dom: 'Bfrtip',
        buttons: [
            'copy', 'csv', 'excel', 'pdf', 'print'
        ]
    } );
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