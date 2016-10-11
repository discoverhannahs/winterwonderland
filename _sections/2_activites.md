---
title: Activities
---

{% for activity in site.activities %}
  <div class="site__section site__section--activity">
    <div class="row">
      <div class="large-5 columns">
        <img src="{{site.baseurl}}/img/{{activity.image}}" alt="" class="">
      </div>
      <div class="large-7 columns">
        <h2 class="heading heading--section" id="{{activity.title}}">{{ activity.title }}</h2>
        <h3 class="subheading subheading--section">{{ activity.intro }}</h3>  
        {{ activity.content | markdownify }}
      </div>
    </div>
  </div>
{% endfor %}
