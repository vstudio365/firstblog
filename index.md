### Purpose

This blog is a colloborative place to publish articles around `SharePoint, Azure, M365 & Power Platform`

#### Posts
{% for post in site.posts %}
  <a href="{{ post.url  | prepend: site.baseurl  }}">{{ post.title }}</a>
{% endfor %}


<header class="post-header">
    <h1 class="post-title p-name" itemprop="name headline">Posts</h1>
   <ul>
{% for post in site.posts %}
  <a href="{{ post.url  | prepend: site.baseurl  }}">{{ post.title }}</a>
  </br>
{% endfor %}
</ul>
  </header>
