---
layout: page
title: Projects
---

The current research projects the the Autonomy and Verification Network is involved in. Clicking the project's logo or picture will take you to the project's page or external website. This page also has information about our [Previous Projects](#previous-projects)

## Current projects
<br>

{% assign rows = site.projects.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
<article class="w3-row w3-margin-bottom">
 {% assign offset = forloop.index0 | times: 2 %}
   {% for project in site.projects limit:2 offset:offset %}
       <section class="w3-half w3-container">
      <div class="shaded_box w3-container w3-display-container" style="min-height:270px">
          <h3 class="w3-margin-left" style="text-decoration: underline;"> {{project.title}}</h3>
          
          {{project.content}}
      </div>
      </section>     
   {% endfor %}   
</article>
{% endfor %}




## Previous Projects

{% assign rows = site.projects-previous.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
<article class="w3-row">
 {% assign offset = forloop.index0 | times: 2 %}
   {% for project in site.projects-previous limit:2 offset:offset %}
      <section class="w3-half w3-container">
        <div class="shaded_box">
          <h3 style="text-decoration: underline;"> {{project.title}}</h3>
          
          {{project.content}}
      </div>
      </section>     
   {% endfor %}   
</article>
{% endfor %}
