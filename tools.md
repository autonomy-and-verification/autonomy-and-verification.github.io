---
layout: page
title: Tools
---

[Members](/members) of the network have produced a variety of software tools related to the verification of autonomous systems.

The list below gives a short description of each tool. Click "More Details" for the tool's detail page.

<br>

{% assign rows = site.tools.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
<article class="row">
 {% assign offset = forloop.index0 | times: 2 %}
   {% for tool in site.tools limit:2 offset:offset %}
      <section class="columns large-6">
      <div class="shaded_box" style="min-height:270px">
        <div style="margin:0 25px">
          <a href="{{ tool.url }}"><h3 style="text-decoration: underline;">{{tool.title}}</h3></a>
          <h4> {{tool.author}} </h4>
        <p>{{tool.blurb}}</p>
        <p><a href="{{ tool.url }}">More Details</a></p>
        </div>
        </div>
      </section>       
   {% endfor %}      
</article>
<br>
{% endfor %}
