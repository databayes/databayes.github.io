---
layout: default
title: Blog
permalink: /blog/
---

# All Blog Posts

{% if site.posts.size > 0 %}
  <div class="post-list">
    {% for post in site.posts %}
      <article class="post-preview">
        <header>
          <h2><a href="{{ post.url | relative_url }}" class="post-link">{{ post.title | escape }}</a></h2>
          <p class="post-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
            {% if post.author %} • {{ post.author }}{% endif %}
          </p>
        </header>
        
        {% if post.excerpt %}
          <div class="post-excerpt">
            {{ post.excerpt | markdownify | strip_html | truncate: 300 }}
          </div>
        {% endif %}
        
        {% if post.tags %}
          <div class="post-tags">
            <strong>Tags:</strong>
            {% for tag in post.tags %}
              <span class="tag">{{ tag }}</span>{% unless forloop.last %} {% endunless %}
            {% endfor %}
          </div>
        {% endif %}
      </article>
    {% endfor %}
  </div>
{% else %}
  <p>No blog posts have been published yet. Check back soon for data science insights and analysis!</p>
  
  <h3>How to Add Posts</h3>
  <p>To add a new blog post:</p>
  <ol>
    <li>Create a new file in the <code>_posts</code> directory</li>
    <li>Name it with the format: <code>YYYY-MM-DD-title.md</code></li>
    <li>Add front matter and content (see the sample post for an example)</li>
    <li>Commit and push your changes</li>
  </ol>
{% endif %}