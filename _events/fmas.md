---
layout: event
title: "Workshop on Formal Methods for Autonomous Systems (FMAS)"
series : true
redirect_to:
  - https://fmasworkshop.github.io/
---
<img alt="FMAS Workshop Logo" style="float: left; margin: 1em" src="{{site.images}}logos/FMAS-Logo.png">

The Workshop on Formal Methods for Autonomous Systems bring together researchers working on a range of techniques for formal verification of autonomous systems, to present recent work in the area, discuss key difficulties, and stimulate collaboration between the robotics and formal methods communities.

This workshop is concerned with the use of formal methods to specify, model, or verify autonomous or robotic systems; in whole or in part. Submissions may focus on case studies that identify the challenges for formal methods in this area, or experience reports that provide guidelines for tackling these challenges. Work using integrated formal methods, or describing the future directions of this field, are particularly welcome.

## Organisers

Originally researchers are the University of Liverpool, but now at the University of Manchester, FMAS is primarily organised by:

<article class="row">
  <section class="columns large-4" markdown="1">
 [Dr Marie Farrell](http://cgi.csc.liv.ac.uk/~marie/)
</section>
<section class="columns large-4" markdown="1">
  [Dr Matt Luckcuck](https://cgi.csc.liv.ac.uk/~mattlck/)
</section>
</article>


## Editions of FMAS
<ul>
{% for event in site.events  %}
{% if event.belogsToSeries contains 'fmas' %}
<li> [{{ event.date | date: "%-d %B %Y" }}] <a href="{{site.url}}{{event.url}}" alt="{{event.title}}"> {{event.title}} </a>  </li>
{% endif %}
{% endfor %}
</ul>
