---
title: Events
---

<div class="row">
<div class="large-8 large-centered">
<div class="text-center">
{% for event in site.events %}
  {% if event.date-override %}
  <h4 class="subheading subheading--event"><strong>{{ event.date-override }}</strong></h4>
  {% elsif event.date-end %}
  <h4 class="subheading subheading--event">{{ event.date | date: "%A %-d %B" }} - {{ event.date-end | date: "%A %-d %B %Y" }}</h4>
  {% else %}
  <h4 class="subheading subheading--event">{{ event.date | date: "%A %-d %B %Y" }}</h4>
  {% endif %}
  <h1 class="heading heading--event" id="{{event.marker}}">{{ event.title }}</h1>
  {{ event.content | markdownify }}
  {% if event.booking %}
    {% if event.booking contains 'www.brownpapertickets.com' %}
    <a href="{{ event.booking }}" class="button">Book tickets now</a>
    {% endif %}
  {% endif %}
  <hr>
{% endfor %}
</div>
</div>
</div>
