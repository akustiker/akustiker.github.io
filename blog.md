---
layout: page
title: Blog
permalink: /blog/
comments: true
---

  <p class="lead">Hier finden Sie meine letzten Beiträge.</p>

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
      {% for post in site.posts %}
      {% assign date_format = site.minima.date_format | default: "%F" %}
      <tr>
        <th scope="row">{{ forloop.index }}</th>
        <td>{{ post.date | date: date_format }}</td>
        <td><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></td>
        <td><span class="badge badge-secondary">{{ post.categories }}</span></td>
      </tr>
      {% endfor %}
    </tbody>
  </table>

  <p class="rss-subscribe"><a href="{{ "/feed.xml" | relative_url }}"> RSS <i class="fas fa-rss-square"></i></a> abonieren.</p>
