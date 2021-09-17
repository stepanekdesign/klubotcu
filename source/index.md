---
layout: default
pagination:
  enabled: true # Enable pagination on this page
---

<!-- This loops through the paginated posts -->
{% for post in paginator.posts %}
  <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
  <span class="date">{{ post.date }}</span>
  <div class="content">
	{{ post.content }}
  </div>
{% endfor %}

<!-- Pagination links -->
<div class="pagination">
  {% if paginator.previous_page %}
	<a href="{{ paginator.previous_page_path }}" class="previous">
	  Předchozí
	</a>
  {% endif %}
  {% if paginator.next_page %}
	<a href="{{ paginator.next_page_path }}" class="next">Další</a>
  {% endif %}
</div>