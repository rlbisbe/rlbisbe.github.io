# Project Context for AI Agents

## Overview
This is a personal blog built with **Jekyll**, a static site generator. The blog is hosted on **GitHub Pages** and serves content in Spanish.

## Technology Stack
- **Jekyll**: Static site generator
- **GitHub Pages**: Hosting platform
- **Markdown**: Content format (using Kramdown)
- **Rouge**: Syntax highlighter
- **Twenty Twelve**: WordPress theme adapted for Jekyll

## Project Structure
- `_layouts/`: HTML templates for pages and posts
  - `default.html`: Main layout template
  - `post.html`: Template for blog posts
  - `page.html`: Template for static pages
- `_posts/`: Blog posts in Markdown format
- `css/`: Stylesheets
  - `main.css`: Legacy styles
  - `style.css`: Primary styles (Twenty Twelve theme)
  - `syntax.css`: Code syntax highlighting
  - `dark-mode.css`: Dark mode styles based on browser preferences
- `_config.yml`: Jekyll configuration

## Key Features
- **Mobile-responsive design**: Optimized for various screen sizes
- **Dark mode**: Automatic dark mode based on `prefers-color-scheme` media query
- **Syntax highlighting**: Code blocks with Rouge
- **RSS feed**: Available at `/atom.xml`
- **Pagination**: 5 posts per page

## Build & Development
- Jekyll builds the site from Markdown to static HTML
- No server-side processing - everything is static
- Assets are served directly from the repository

## Important Notes
- Content is in **Spanish** (language: `es`)
- Blog owner: Roberto Luis (@rlbisbe)
- Blog title: "rlbisbe @ dev"
- Tagline: "Tengo muchas cosas en la cabeza… sobre todo punteros a null"

## Configuration Details
- Markdown engine: Kramdown with GitHub Flavored Markdown (GFM)
- Syntax highlighter: Rouge
- Permalink structure: `/:year/:month/:day/:title`
- Plugins:
  - jekyll-sitemap
  - jekyll-feed

## When Making Changes
1. **Content**: Add/edit Markdown files in `_posts/` or root directory
2. **Styling**: Modify CSS files in `/css/` directory
3. **Layout**: Edit HTML templates in `_layouts/`
4. **Configuration**: Update `_config.yml` for site-wide settings
5. **Testing**: Build locally with `jekyll serve` before committing

## Testing

### Local Development Server
```bash
# Install dependencies
gem install jekyll bundler jekyll-sitemap jekyll-feed

# Build the site
jekyll build

# Serve locally
jekyll serve --port 4000

# Visit http://localhost:4000
```

### Dark Mode Testing
The blog implements automatic dark mode using `@media (prefers-color-scheme: dark)`.

**Method 1: Browser DevTools (Recommended)**
1. Open the site in your browser
2. Open DevTools (F12)
3. Press Cmd/Ctrl + Shift + P → type "Rendering"
4. Find "Emulate CSS media feature prefers-color-scheme"
5. Toggle between `light` and `dark`

**Method 2: System Settings**
- **macOS**: System Preferences → General → Appearance → Dark
- **Windows**: Settings → Personalization → Colors → Dark
- **Linux**: Settings → Appearance → Dark

### Important Testing Notes
- Dark mode automatically activates based on browser/OS preferences
- No JavaScript required - purely CSS-based
- For dark mode verification, use real browsers with DevTools
- See `TESTING.md` for comprehensive testing guide
