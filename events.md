---
layout: page
title: Events
---

Upcoming Workshops, Tutorials, and other events run by [Members](/members) of the Autonomy and Verification Network.

<article class="w3-row">
<div class="w3-container">
<section class="w3-threequarter">
<h3>Upcoming Events</h3>

  <ul>
    {% for event in site.events %}
      {% if event.date >= site.time %}
        {% if event.externalURL and event.externalURL != "" and event.externalURL != nil and event.series != true %}
        <li>
          [{{ event.date | date: "%-d %B %Y" }}] <a href="{{ event.externalURL }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }} <i class="fas fa-external-link-alt"></i>{% endif %}</a>
        </li>
        {% elsif event.series != true %}
        <li>
          [{{ event.date | date: "%-d %B %Y" }}] <a href="{{ event.url }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }}{% endif %}</a>
        </li>
       {% endif%}
      {% endif %}
    {% endfor %}
  </ul>

<h3>Past Events</h3>
<ul>
  {% assign dates = site.events | sort: date %}
  {% assign revDates = dates | reverse %}
  {% for event in revDates  %}
  {% if event.date < site.time %}
    {% if event.externalURL and event.externalURL != "" and event.externalURL != nil %}
    <li>
      [{{ event.date | date: "%-d %B %Y" }}] <a href="{{ event.externalURL }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }} <i class="fas fa-external-link-alt"></i>{% endif %}</a>
    </li>
    {% elsif event.series != true %}
    <li>
      [{{ event.date | date: "%-d %B %Y" }}] <a href="{{ event.url }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }}{% endif %}</a>
    </li>
   {% endif%}
  {% endif %}
  {% endfor %}
</ul>

</div>
</section>

<section class="3-container w3-quarter" >
<h3>Event Series</h3>
<ul>
  {% for event in site.events  %}
    {% if event.series == true %}
      {% if event.externalURL and event.externalURL != "" and event.externalURL != nil %}
      <li>
        <a href="{{ event.externalURL }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }} <i class="fas fa-external-link-alt"></i>{% endif %}</a>
      </li>
      {% else %}
      <li>
        <a href="{{ site.url }}{{ event.url }}">{% if site.titlecase %}{{ event.title | titlecase }}{% else %}{{ event.title }}{% endif %}</a>
    </li>
    {% endif %}
    {% endif %}
  {% endfor %}
</ul>
</section>

</article>
