---
layout: page
title: Members
---

<section class="row">
  <h2>Current Members</h2>

{% for institute in site.data.members.CurrentMembers %}
  <section class="small-5 medium-4 columns">
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
  </section>
{% endfor %}

</section>


<section class="row">

<h2> Affiliated Members </h2>
{% for institute in site.data.members.AffiliatedMembers %}
  <section class="small-5 medium-4 columns">
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
  </section>
{% endfor %}
</section>


<section class="row">

<h2> Previous Members </h2>
<section>
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

</section>
