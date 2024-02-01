---
layout: page
title: Members
---

<h3>Current Members</h3> 
<section class="w3-row">
{% for institute in site.data.members.CurrentMembers %}  
  <section class="w3-third w3-container">
  <div class="shaded_box">
  <h4 class="w3-margin-left" style="text-decoration: underline;">{{ institute.Institute }} </h4>
  <ul >
  {% assign sortedMembers = institute.MembersList | sort: "secondName" %}
  {% for member in sortedMembers %}
  {% assign name = member.firstName | append: " " | append: member.secondName %}
  <li> {% if member.website != null %}<a href="{{ member.website }}" target="_blank" rel="noopener noreferrer">{{ name }}</a>{% else %}{{name}}{% endif %}{% if member.alt-website != null%}, <a href="{{ member.alt-website }}" target="_blank" rel="noopener noreferrer">see also</a>{% endif %}
  {% if member.orcid != null %}
    <a href="{{ member.orcid }}" target="_blank" rel="noopener noreferrer"><img alt="ORCID logo" src="/images/logos/orcid_32x32.png" width="21" height="21"/></a>
  {% endif %}
  {% if member.scholar != null %}
    <a href="{{ member.scholar }}" target="_blank" rel="noopener noreferrer"><img alt="Google Scholar Logo" src="/images/logos/gscholar32x32.png" width="21" height="21"/></a>
  {% endif%}
  </li>
  {% endfor %}
  </ul>
  </div>
  </section>
{% endfor  %}
 
</section>
<br>

<h3> Affiliated Members </h3>
<section class="w3-row">
{% for institute in site.data.members.AffiliatedMembers %}

  <section class="w3-third w3-container">
  <div class="shaded_box">
  <h4 class="w3-margin-left" style="text-decoration: underline;">{{ institute.Institute }}</h4>

  <ul>
  {% assign sortedAffiliates = institute.MembersList | sort: "secondName" %}
  {% for member in sortedAffiliates %}
  {% assign name = member.firstName | append: " " | append: member.secondName %}
    <li>
    {% if member.website != null %}
      <a href="{{ member.website }}" target="_blank" rel="noopener noreferrer">{{ name }}</a>
    {% else %}
      {{ name }}
    {% endif %}
    {% if member.orcid != null %}
      <a href="{{ member.orcid }}" target="_blank" rel="noopener noreferrer"><img alt="ORCID logo" src="/images/logos/orcid_32x32.png" width="21" height="21"/></a>
    {% endif %}
    </li>
  {% endfor %}
  </ul>
  </div>
  </section>
{% endfor %}
</section>
<br>

<h3> Previous Members </h3>
<section class="w3-row">
<div class="shaded_box w3-container w3-threequarter">
<ul>
{% for member in site.data.members.PreviousMembers %}   
  <li>
  {% if member.website != null %}
    <a href="{{ member.website }}" target="_blank" rel="noopener noreferrer">{{ member.name }}</a>
  {% else %}
    {{ member.name }}
  {% endif %}
  {% if member.orcid != null %}
  <a href="{{ member.orcid }}" target="_blank" rel="noopener noreferrer"><img alt="ORCID logo" src="/images/logos/orcid_32x32.png" width="21" height="21"/></a>
  {% endif %}
  </li>
{% endfor %}
</ul>
</div>
</section>
