---
layout: page
title: Tools
---

[Members](/members) of the network have produced a variety of software tools related to the verification of autonomous systems.

The list below gives a short description of each tool. Click "More Details" for the tool's detail page.

<br>

{% assign rows = site.tools.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
<article class="w3-row w3-margin-bottom">
 {% assign offset = forloop.index0 | times: 2 %}
   {% for tool in site.tools limit:2 offset:offset %}
      <section class="w3-half w3-container">
      <div class="shaded_box w3-container w3-display-container" style="min-height:270px">

          <a href="{{ tool.url }}"><h3 style="text-decoration: underline;">{{tool.title}}</h3></a>
          <h4> {{tool.author}} </h4>
        <p>{{tool.blurb}}</p>
        <div class="w3-display-bottommiddle"><a class="w3-button w3-leftbar w3-rightbar w3-topbar w3-bottombar w3-round-large" href="{{ tool.url }}">More Details >></a></div>

        </div>
      </section>   
     
   {% endfor %}      
</article>
<br>
{% endfor %}
