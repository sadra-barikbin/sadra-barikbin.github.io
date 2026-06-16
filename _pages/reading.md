---
title: "On my nightstand"
permalink: /reading/
author_profile: false
classes: wide
---

<p class="reading-invite">
  I read slowly &mdash; on purpose. I&rsquo;d rather live with a book for a while
  than rush through it, so what sits here tends to stay a while. Whatever it is,
  I&rsquo;m always glad to talk about it: if you&rsquo;ve read it, are reading it,
  or just have opinions, <a href="/contact/">come argue with me</a>.
</p>

{% assign book = site.data.reading.current %}
{% if book %}
<div class="reading-now">
  <div class="reading-now__cover">
    {% if book.link and book.link != "" %}<a href="{{ book.link }}">{% endif %}
    <img src="{{ book.cover | default: '/assets/images/book-cover.svg' }}" alt="Cover of {{ book.title }}">
    {% if book.link and book.link != "" %}</a>{% endif %}
  </div>
  <div class="reading-now__body">
    <p class="reading-now__label">Currently reading</p>
    <h2 class="reading-now__title">{% if book.link and book.link != "" %}<a href="{{ book.link }}">{{ book.title }}</a>{% else %}{{ book.title }}{% endif %}</h2>
    <p class="reading-now__author">{{ book.author }}{% if book.edition %} <span class="reading-now__edition">&middot; {{ book.edition }}</span>{% endif %}</p>
    {% if book.note %}<p class="reading-now__note">{{ book.note }}</p>{% endif %}
    <p class="reading-now__cta"><a href="/contact/">Read it too? Let&rsquo;s talk &rarr;</a></p>
  </div>
</div>
{% endif %}

{% if site.data.reading.finished %}
<h2 class="reading-shelf__title">Recently finished</h2>
<ul class="reading-shelf">
  {% for b in site.data.reading.finished %}
  <li><span class="reading-shelf__book">{{ b.title }}</span> &mdash; <span class="reading-shelf__author">{{ b.author }}</span></li>
  {% endfor %}
</ul>
{% endif %}
