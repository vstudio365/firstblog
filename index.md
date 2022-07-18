  <header class="post-header">
    <h1 class="post-title p-name" itemprop="name headline">POSTS</h1>
   <ul>
{% for post in site.posts %}
  <a href="{{ post.url  | prepend: site.baseurl  }}">{{ post.title }}</a>
{% endfor %}
</ul>
  </header>
