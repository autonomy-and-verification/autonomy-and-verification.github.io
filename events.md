---
layout: page
title: Events
---

Upcoming Workshops, Tutorials, and other events run by [Members](/members) of the Autonomy and Verification Network.

<article class="row">

<section class="columns large-7" >
<h2>Upcoming Events</h2>
  <ul>
    {% for event in site.events %}
      {% if event.date >= site.time %}

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

<h2>Past Events</h2>
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


</section>

<section class="columns large-3" >
<h2>Event Series</h2>
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
