---
layout: page
title: Members
---

<article class="row">
  <section class="columns large-4">

<h2>Current Members</h2>

{% for institute in site.data.members.CurrentMembers %} 
  <h3>{{ institute.Institute }}</h3>
  <ul>
  {% for member in institute.MembersList %}
    <li>
    {% if member.website != null %}
      <a href="{{ member.website }}">{{ member.name }}</a>
    {% else %}
      {{ member.name }}
    {% endif %}
    {% if member.orcid != null %}
      <a href="{{ member.orcid }}"><img alt="ORCID logo" src="/images/logos/orcid_32x32.png" width="21" height="21"/></a>
    {% endif %}
    </li>
  {% endfor %}
  </ul>
{% endfor %}

</section>

<section class="columns large-6">

<h2> Affiliated Members </h2>

{% for institute in site.data.members.AffiliatedMembers %}
  <h3>{{ institute.Institute }}</h3>
  <ul>
  {% for member in institute.MembersList %}
    <li>
    {% if member.website != null %}
      <a href="{{ member.website }}">{{ member.name }}</a>
    {% else %}
      {{ member.name }}
    {% endif %}
    {% if member.orcid != null %}
      <a href="{{ member.orcid }}"><img alt="ORCID logo" src="/images/logos/orcid_32x32.png" width="21" height="21"/></a>
    {% endif %}
    </li>
  {% endfor %}
  </ul>
{% endfor %}

</section>
</article>

<article class="row">

<section class="columns large-6">
<h2> Previous Members </h2>

<ul>
{% for member in site.data.members.PreviousMembers %}
  <li>
  {% if member.website != null %}
    <a href="{{ member.website }}">{{ member.name }}</a>
  {% else %}
    {{ member.name }}
  {% endif %}
  {% if member.orcid != null %}
  <a href="{{ member.orcid }}"><img alt="ORCID logo" src="/images/logos/orcid_32x32.png" width="21" height="21"/></a>
  {% endif %}
  </li>
{% endfor %}
</ul>

</section>

</article>
