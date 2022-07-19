
This blog is a place to share knowledge around `SharePoint, Azure, M365 & Power Platform`

### Posts
{% for post in site.posts %}
  <a href="{{ post.url  | prepend: site.baseurl  }}">{{ post.title }}</a>
{% endfor %}



