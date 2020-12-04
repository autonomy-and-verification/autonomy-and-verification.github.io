---
layout: page
title: Tools
---

[Members](/members) of the network have produced a variety of software tools related to the verification of autonomous systems.

The list below gives a short description of each tool. Click "More Details" for the tool's page.


{% assign rows = site.tools.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
<article class="row">
 {% assign offset = forloop.index0 | times: 2 %}
   {% for tool in site.tools limit:2 offset:offset % }
      <section class="columns large-6">
          <a href="{{ site.url }}{{ tool.url }}">
          <h3> {{tool.title}}</h3>
          <h4> {{tool.author}} </h4>
          </a>
        <p>{{tool.blurb}}</p>
        <p><a href="{{ site.url }}{{ tool.url }}">More Details</a></p>
      </section>       
   {% endfor %}      
</article>
<br>
{% endfor %}
