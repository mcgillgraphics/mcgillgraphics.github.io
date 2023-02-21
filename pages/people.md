---
layout: page
title: People
icon: user.png
permalink: /people
---

<!-- Lab people -->
<div class="row">
  <div class="col-md-12">
    <h2 class="page-header">Faculty & Staff</h2>
  </div>
</div>

<div class="row">
  <div class="col-md-12">
    <!-- Faculty -->
    {% assign members = site.data.members.faculty %}
    {% for member in members %}
      {% include member_card.html
      photo=member.photo
      first=member.first last=member.last
      title=member.title
      department=member.department
      begin-year=member.begin-year
      email=member.email
      office=member.office
      website=member.website
      google-scholar=member.google-scholar
      icon="i"
      %}
    {% endfor %}
  </div>
</div>

{% assign students = site.data.members.grads %}

<div class="row">
  <div class="col-md-12">
    <h2 class="page-header">Postdoctoral Researchers</h2>
  </div>
</div>

<div class="row">
  <div class="col-md-12">
    <!-- Postdocs -->
    {% assign members = site.data.members.postdocs %}
    {% for member in members %}
      {% include member_card.html
      photo=member.photo
      first=member.first last=member.last
      pronouns=member.pronouns
      title=member.title
      begin-year=member.begin-year
      email=member.email
      office=member.office
      website=member.website
      google-scholar=member.google-scholar
      icon="r"
      %}
    {% endfor %}
  </div>
</div>

<div class="row">
  <div class="col-md-12">
    <h2 class="page-header">Ph.D. Students</h2>
  </div>
</div>

<div class="row">
  <div class="col-md-12">
    <!-- PhD students -->
    {% assign phds = students | where: "title", "Ph.D." | sort: "begin-year" %}
    {% for member in phds %}
      {% include member_card.html
      photo=member.photo
      first=member.first last=member.last
      pronouns=member.pronouns
      title=member.title
      begin-year=member.begin-year
      email=member.email
      office=member.office
      website=member.website
      google-scholar=member.google-scholar
      icon="b"
      %}
    {% endfor %}
  </div>
</div>

{% assign students = site.data.members.grads %}
<div class="row">
  <div class="col-md-12">
    <h2 class="page-header">Master Students</h2>
  </div>
</div>

<div class="row">
  <div class="col-md-12">
    <!-- Master students -->
    {% assign masters = students | where: "title", "Master" | sort: "begin-year" %}
    {% for member in masters %}
      {% include member_card.html
      photo=member.photo
      first=member.first last=member.last
      pronouns=member.pronouns
      title=member.title
      begin-year=member.begin-year
      office=member.office
      email=member.email
      website=member.website
      google-scholar=member.google-scholar
      icon="c"
      %}
    {% endfor %}
  </div>
</div>

<div class="row">
  <div class="col-md-12">
    <h2 class="page-header">Alumnis</h2>
  </div>
</div>

<div class="row">
  <div class="col-md-12">
    <!-- Alumni -->
    {% assign alumnis = site.data.members.alumnis | sort: "end_year" | reverse %}
    {% for member in alumnis %}
    <ul class="fa-ul">
      <li><span class="fa-li"><i class="fa-solid fa-graduation-cap"></i></span>
        {{ member.first }} {{ member.last }} ({{ member.title }}, {{ member.end_year }})
        {% if member.now_at %}
          <i class="fa-solid fa-arrow-right"></i><em> {{ member.now_at }}</em>
        {% endif %}
      </li>
    </ul>
    {% endfor %}
  </div>
</div>