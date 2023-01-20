---
layout: page
title: Members
---

<section class="row">
  <h2>Current Members</h2>  

{% for institute in site.data.members.CurrentMembers %}  
  <section class="small-5 medium-4 columns">
  <div class="shaded_box">
  <h3 style="text-decoration: underline;">{{ institute.Institute }} </h3>
  <ul >
  {% for member in institute.MembersList %}
  <li> {% if member.website != null %}<a href="{{ member.website }}" target="_blank" rel="noopener noreferrer">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}{% if member.alt-website != null%}, <a href="{{ member.alt-website }}" target="_blank" rel="noopener noreferrer">see also</a>{% endif %}
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

<section class="row">

<h2> Affiliated Members </h2>
{% for institute in site.data.members.AffiliatedMembers %}
  <section class="small-5 medium-4 columns">
  <div class="shaded_box">
  <h3 style="text-decoration: underline;">{{ institute.Institute }}</h3>

  <ul>
  {% for member in institute.MembersList %}
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
{% endfor %}
</section>
<br>

<section class="row">
<h2> Previous Members </h2>
<div class="shaded_box">
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
