---
layout: default
---

<!-- <div class="articles full-width">
  <article>
    <h1>Programme</h1>
    This page is aligned with the programme of the symposium. It features a brief summary of each element. Click on the title to find the presentations and more information about each of the talks.
  </article>
</div> -->

<div class="articles">
  {% for post in site.posts reversed %}
  <article class="post">
    <h1 class="post-title">
      <a href="{{ site.baseurl}}{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>
    <b>{{post.author}}</b>
    {% if post.excerpt %}
      {{ post.excerpt }}
    {% endif %}
    <div class="pagination nugget-info tc">
      <a href="{{ site.baseurl}}{{ post.url }}" class="button">More info and presentation</a>
    </div>
  </article>
  {% endfor %}

  <aside class="read-more">
    <ul>
      {% for post in site.posts reversed %}
      <li>
        <a href="#">
          <em>{{post.title}}</em>
          <b>{{post.author}}</b>
          <svg x="0px" y="0px" width="36px" height="36px" viewBox="0 0 36 36"><circle fill="none" stroke-width="2" cx="18" cy="18" r="16" stroke-dasharray="100 100" stroke-dashoffset="100" transform="rotate(-90 18 18)"></circle></svg>
        </a>
      </li>
      {% endfor %}
    </ul>
  </aside>
</div>
