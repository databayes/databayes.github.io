# Databayes Website

This is the GitHub Pages website for Databayes, featuring a blog focused on data science insights and analysis.

## 🚀 Quick Start

This website is built with Jekyll and automatically deploys via GitHub Pages when you push changes to the main branch.

### Viewing the Website
- **Live Site**: https://databayes.github.io
- **GitHub Pages Settings**: Go to your repository Settings > Pages to configure deployment

### Local Development (Optional)
To run the site locally for testing:

```bash
# Install dependencies
bundle install

# Serve the site locally
bundle exec jekyll serve

# View at http://localhost:4000
```

## 📝 Adding Blog Posts

### Step 1: Create a New Post File
1. Navigate to the `_posts` directory
2. Create a new file with the format: `YYYY-MM-DD-title.md`
   - Example: `2024-01-20-analyzing-customer-data.md`

### Step 2: Add Front Matter
Start your post with YAML front matter:

```yaml
---
layout: post
title: "Your Post Title Here"
date: 2024-01-20 10:00:00 -0000
author: "Sue @ Databayes"
tags: [data-science, analysis, tutorial]
excerpt: "A brief description of your post that appears in previews"
---
```

### Step 3: Write Your Content
Write your post content in Markdown below the front matter:

```markdown
# Your Post Content

This is where you write your blog post content using **Markdown** formatting.

## Subheadings
- Bullet points
- More content

```python
# Code blocks are supported
import pandas as pd
data = pd.read_csv('data.csv')
```

### Step 4: Publish
1. Commit your new file
2. Push to GitHub
3. Your post will be live within a few minutes!

## 📁 Website Structure

```
databayes.github.io/
├── _config.yml          # Site configuration
├── _layouts/            # Page templates
├── _includes/           # Reusable components
├── _posts/              # Blog posts
├── _sass/               # CSS styles
├── assets/              # Images, CSS, JS
├── index.md             # Homepage
├── about.md             # About page
├── blog.md              # Blog archive page
└── Gemfile              # Ruby dependencies
```

## ⚙️ Configuration

### Site Settings (`_config.yml`)
Key settings you might want to customize:
- `title`: Site title
- `email`: Contact email
- `description`: Site description
- `url`: Your site URL

### Customizing Design
- **Colors**: Modify CSS variables in `assets/css/style.scss`
- **Layout**: Edit files in `_layouts/` and `_includes/`
- **Navigation**: Update `_includes/header.html`

## 🎨 Writing Tips

### Markdown Formatting
- Use `#` for headings
- Use `**bold**` and `*italic*` for emphasis
- Use ``` for code blocks
- Use `[text](url)` for links

### Tags
Add relevant tags to help organize content:
- `data-science`
- `python`
- `visualization`
- `statistics`
- `tutorial`
- `case-study`

### Images
1. Add images to `assets/images/`
2. Reference in posts: `![Alt text](/assets/images/filename.jpg)`

### Code Highlighting
Supported languages include:
```python
# Python code
```

```r
# R code
```

```sql
-- SQL code
```

## 📊 Analytics and SEO

The site includes:
- **SEO optimization** via `jekyll-seo-tag`
- **RSS feed** at `/feed.xml`
- **Sitemap** automatically generated
- **Google Analytics** (configure in `_config.yml` if needed)

## 🔧 Troubleshooting

### Common Issues

**Site not updating?**
- Check GitHub Pages settings in repository settings
- Verify your changes are on the correct branch
- Check for Jekyll build errors in the Actions tab

**Local development issues?**
```bash
# Update dependencies
bundle update

# Clear cache
bundle exec jekyll clean
bundle exec jekyll serve
```

**Need help with Markdown?**
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/)

## 📞 Support

For questions about the website:
- Check the [Jekyll documentation](https://jekyllrb.com/docs/)
- Review [GitHub Pages documentation](https://docs.github.com/en/pages)
- Contact: {{ site.email }}

---

**Ready to start blogging?** Create your first post in the `_posts` directory and push to GitHub!
