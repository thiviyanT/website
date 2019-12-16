---
title: "Posts · Thiviyan Thanapalasingam"
permalink: /blog/
layout: default
---

{% include header.html %}
<section>
    <h2>Blog posts</h2>

    {% for post in site.posts %}
    <p>
        <a href="{{ post.url }}"><b>{{ post.title }}</b></a>
        <br>
        {{ post.excerpt | strip_html | strip_newlines | truncate: 200 }}
        <br>
        <span class="date">Published on {{ post.date | date_to_string }}</span>
    </p>
    {% endfor %}
<section>