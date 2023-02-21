---
layout: page
title: News
icon: teapot.png
permalink: /news
---

<div class="row">
  <div class="col-sm-12">
    <dl class="newslist">
      {% assign news = site.data.news | sort: 'date' | reverse %}
      {% for n in news %}
        <dt>{{ n.date }}</dt>
        <dd>{{ n.news }}</dd>
      {% endfor %}
    </dl>
  </div>
</div>