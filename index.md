---
layout: home
title: "Databayes Technical Blog"
---

# Welcome to Databayes Technical Blog

This blog contains technical posts supporting our data science and engineering work. Here you'll find insights, tutorials, and documentation related to:

- Data Science methodologies
- Machine Learning implementations 
- Engineering best practices
- Technical deep dives
- Project case studies

{% if site.posts.size > 0 %}
## Latest Posts

{% for post in site.posts limit:5 %}
- **{{ post.date | date: "%B %d, %Y" }}** - [{{ post.title }}]({{ post.url | relative_url }})
  {{ post.excerpt | strip_html | truncatewords: 30 }}
{% endfor %}

[View all posts →](/posts/)
{% else %}
## Getting Started

No posts yet! Check back soon for technical content.
{% endif %}