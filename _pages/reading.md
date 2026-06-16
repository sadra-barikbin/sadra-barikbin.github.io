---
title: "Reading"
permalink: /reading/
author_profile: false
classes: wide
---

<p class="reading-invite">
  I&rsquo;m always in the middle of a book &mdash; usually two. This is what&rsquo;s
  open on my desk right now. If you&rsquo;ve read it, are reading it, or just have
  opinions about it, I&rsquo;d genuinely love to hear them &mdash;
  <a href="/contact/">start a conversation</a>. Half the pleasure of a book is
  arguing about it afterward.
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
    <h2 class="reading-now__title">{{ book.title }}</h2>
    <p class="reading-now__author">{{ book.author }}</p>
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
