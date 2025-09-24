---
layout: default
---

<div class="home">
  <h1 class="page-heading">Welcome to Databayes</h1>
  
  <div class="intro">
    <p>Welcome to Databayes, where we explore the fascinating world of data science, statistics, and business intelligence. Our blog features insights, tutorials, and analysis that help make sense of complex data challenges.</p>
  </div>

  <h2>Latest Posts</h2>

  {% if site.posts.size > 0 %}
    <ul class="post-list">
      {% for post in site.posts limit:5 %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
          <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          </h3>
          {% if post.excerpt %}
            <div class="post-excerpt">
              {{ post.excerpt | markdownify | strip_html | truncate: 200 }}
            </div>
          {% endif %}
        </li>
      {% endfor %}
    </ul>

    <p class="rss-subscribe">
      <a href="{{ "/feed.xml" | relative_url }}">RSS Feed</a> | 
      <a href="{{ "/blog" | relative_url }}">View All Posts</a>
    </p>
  {% else %}
    <p>No posts yet. Check back soon for data science insights and analysis!</p>
    <p><em>To add your first post, create a file in the <code>_posts</code> directory with the format <code>YYYY-MM-DD-title.md</code></em></p>
  {% endif %}

</div>