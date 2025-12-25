# rlbisbe.github.io

Personal blog of Roberto Luis - Software Engineer and tech enthusiast.

## 🌐 About

This is my personal blog where I share thoughts, experiences, and technical content about software development. The blog is written in Spanish and covers topics ranging from software engineering to technical tutorials.

**Blog URL**: [https://rlbisbe.net](https://rlbisbe.net)

## 🛠️ Technology Stack

- **Jekyll**: Static site generator
- **GitHub Pages**: Free hosting platform
- **Markdown**: Content written in Markdown format
- **Twenty Twelve**: WordPress theme adapted for Jekyll
- **Rouge**: Syntax highlighting for code blocks

## ✨ Features

- 📱 **Mobile-responsive design**: Optimized for all screen sizes
- 🌙 **Dark mode**: Automatic dark mode based on browser preferences (`prefers-color-scheme`)
- 🎨 **Syntax highlighting**: Beautiful code blocks with Rouge
- 📰 **RSS feed**: Subscribe at [/atom.xml](https://rlbisbe.net/atom.xml)
- 🔍 **SEO optimized**: With sitemap and feed plugins

## 🚀 Local Development

### Prerequisites
- Ruby (2.7 or higher recommended)
- Bundler (`gem install bundler`)

### Setup
```bash
# Clone the repository
git clone https://github.com/rlbisbe/rlbisbe.github.io.git
cd rlbisbe.github.io

# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Visit http://localhost:4000 in your browser
```

### Development workflow
1. Create new posts in `_posts/` directory with format: `YYYY-MM-DD-title.md`
2. Edit layouts in `_layouts/` directory
3. Modify styles in `/css/` directory
4. Test locally before pushing to GitHub

## 📁 Project Structure

```
.
├── _layouts/           # HTML templates
│   ├── default.html    # Main layout
│   ├── post.html       # Blog post layout
│   └── page.html       # Static page layout
├── _posts/             # Blog posts (Markdown)
├── css/                # Stylesheets
│   ├── main.css        # Legacy styles
│   ├── style.css       # Primary styles
│   ├── syntax.css      # Code highlighting
│   └── dark-mode.css   # Dark mode styles
├── _config.yml         # Jekyll configuration
├── index.html          # Home page
└── atom.xml            # RSS feed
```

## 📝 Creating a New Post

Create a new file in `_posts/` directory:

```bash
# File name format: YYYY-MM-DD-post-title.md
# Example: 2025-12-24-my-new-post.md
```

Basic post template:
```markdown
---
layout: post
title: "My Post Title"
date: 2025-12-24 12:00:00
---

Your content here...
```

## 🎨 Dark Mode

The blog automatically adapts to your browser's color scheme preference. Dark mode is implemented using CSS media queries:

```css
@media (prefers-color-scheme: dark) {
  /* Dark mode styles */
}
```

To test dark mode:
- **macOS**: System Preferences → General → Appearance → Dark
- **Windows 10/11**: Settings → Personalization → Colors → Choose your color → Dark
- **Chrome/Edge**: DevTools → Command Menu (Ctrl+Shift+P) → "Rendering" → Emulate CSS media feature prefers-color-scheme

## 📄 License

Blog content and code are maintained by Roberto Luis (@rlbisbe).

## 👤 Author

**Roberto Luis**
- Twitter: [@rlbisbe](https://twitter.com/rlbisbe)
- GitHub: [@rlbisbe](https://github.com/rlbisbe)
- Blog: [rlbisbe.net](https://rlbisbe.net)

Software Engineer at [VS Anywhere](https://vsanywhere.com)
Computer Science Engineer, UAM 2012
Microsoft Active Professional (MAP) since 2013

## 🤝 Contributing

This is a personal blog, but if you spot any issues or have suggestions, feel free to open an issue!

---

*Blog created in 2007 • Migrated to Jekyll • Hosted on GitHub Pages*
