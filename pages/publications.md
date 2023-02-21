---
layout: page
title: Publications
icon: quill-ink.png
permalink: /publications/
---

{% assign pubs-by-year = site.publications | group_by_exp: "item", "item.year" | reverse %}

<nav aria-label="Page navigation">
  <ul class="pagination">
  {% for year in pubs-by-year %}
    <li><a href="#pubs-{{ year.name }}"> {{ year.name }}</a></li>
  {% endfor %}
  </ul>
</nav>

{% for year in pubs-by-year %}
  <h2 class="page-header" id="pubs-{{ year.name }}">{{ year.name }} </h2>

  {% assign pubs = year.items | sort: "publication-date" | reverse %}
  {% for p in pubs %}
  <div class="row row-m-t">
    <div class="col-lg-2">
      <a href="{{ p.permalink }}">
      {% if p.thumbnail %}
        <img class="img-responsive img-thumbnail center-cropped shadowed" src="{{ p.thumbnail }}">
      {% else %}
        <img class="img-responsive img-thumbnail shadowed" src="http://placehold.it/200x200">
      {% endif %}
      </a>
    </div>
    <div class="col-lg-10">
      <div>
        <!-- Paper title -->
        <h3 style="margin-top: 8px;"><a href="{{ p.permalink }}">{{ p.title }}</a></h3>

        <!-- Authors -->
        <h4>
        {% for a in p.authors %}
          {% if forloop.last and forloop.length != 1 %}
            and {% if a.mgl-member %} <span class="mgl-member">{{ a.name }}</span> {% else %} {{ a.name }} {% endif %}
          {% else %}
            {% if a.joint-first %}
              {% if a.mgl-member %} <span class="mgl-member">{{ a.name }}</span>*, {% else %} {{ a.name }}*, {% endif %}
            {% else %}
              {% if a.mgl-member %} <span class="mgl-member">{{ a.name }}</span>, {% else %}
              {{ a.name }}, {% endif %}
            {% endif %}
          {% endif %}
        {% endfor %} 
        </h4>

        <!-- Journal information -->
        <div>
          {{ p.journal }}
          {% if p.journal-note %}
            ({{ p.journal-note }}),
          {% endif %}
          {%- if p.spotlight-note -%}<em>{{ p.spotlight-note }}, </em>{%- endif -%} 
          {% if p.downloads.published %} {{ p.month }} {% endif %} 
          {{ p.year }}
        </div>

        <!-- Links -->
        {% assign dl = p.downloads %}
        <div style="margin-top: 8px;">
          <div class="btn-group" role="group" aria-label="Quick Links">
            <button type="button" class="btn btn-default"><i class="fa-solid fa-bookmark"></i><a href="{{ p.permalink }}"> Project webpage</a></button>
            <button type="button" class="btn btn-default"><i class="fa-solid fa-file-pdf"></i><a href="{{ dl.paper.first.file }}"> Paper ({{ dl.paper.first.size }} pdf)</a></button>
            {% if dl.publisher.url %}
              <button type="button" class="btn btn-default"><i class="fas fa-sm fa-atlas"></i><a href="{{ dl.publisher.url }}"> Publisher's version</a></button>
            {% endif %}
            {% if dl.supplementary.file %}
              <button type="button" class="btn btn-default"><i class="fa-solid fa-file-archive"></i><a href="{{ dl.supplementary.url }}"> Supp. ({{ dl.supplementary.size }} .zip)</a></button>
            {% endif %}
            {% if dl.videos.size > 0 %}
              <button type="button" class="btn btn-default"><i class="fa-brands fa-youtube"></i> <a href="{{ dl.videos.first.url }}"> Video</a></button>
            {% endif %}
            {% if dl.code.url %}
              <button type="button" class="btn btn-default"><i class="fa-brands fa-github"></i> <a href="{{ dl.code.url }}"> Code</a></button>
            {% endif %}
          </div>
        </div>
      </div>
    </div>
  </div>

  {% endfor %}
{% endfor %}