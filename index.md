  <header class="post-header">
    <h1 class="post-title p-name" itemprop="name headline">POSTS</h1>
   <ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
  </header>



  <a class="u-url" href="{{ page.url | relative_url }}" hidden></a>