  <header class="post-header">
    <h1 class="post-title p-name" itemprop="name headline">POSTS</h1>
   <ul>
 <!-- This loops through the paginated posts -->
{% for post in paginator.posts %}
  <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
  <p class="author">
    <span class="date">{{ post.date }}</span>
  </p>
  <div class="content">
    {{ post.content }}
  </div>
{% endfor %}
</ul>
  </header>
