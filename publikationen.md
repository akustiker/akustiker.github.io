---
layout: page
title: Publikationen
permalink: /publikationen/
comments: true
---

<p class="lead">Hier finden Sie eine Liste meiner Publikationen:</p>

<table class="table table-striped">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Datum</th>
      <th scope="col">Titel</th>
      <th scope="col">Kategorie</th>
    </tr>
  </thead>
  <tbody>
    {% assign i = 0 %} {% for post in site.posts %} {% assign date_format = site.minima.date_format | default: "%F" %} {% if post.categories contains "Publikation" %} {% assign i = i | plus:1 %}
    <tr>
      <th scope="row">{{ i }}</th>
      <td>{{ post.date | date: date_format }}</td>
      <td><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></td>
      <td><span class="badge badge-secondary">{{ post.categories }}</span></td>
    </tr>
    {% endif %} {% endfor %}
  </tbody>
</table>
