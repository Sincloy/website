# Sincloy Games Official Website

This is the official website for Sincloy Games, built with the Astro framework. The website showcases our games, team, and development progress, providing a window into our studio for players and media.

## Tech Stack

- [Astro](https://astro.build/) - Website framework
- [Cloudflare Workers](https://workers.cloudflare.com/) - Deployment and hosting

## Project Structure

```
sincloy-website/
├── public/             # Static assets (images, fonts, etc.)
├── src/
│   ├── components/     # Reusable components
│   ├── content/        # Blog and other content
│   ├── layouts/        # Page layouts
│   ├── pages/          # Website pages
│   └── styles/         # Global styles
├── astro.config.mjs    # Astro configuration
└── package.json        # Project dependencies
```

## Development Guide

### Local Development

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build the website
npm run build

# Preview the build
npm run preview
```

### Deployment

```bash
# Build and deploy to Cloudflare
npm run deploy
```

## Content Management

### Blog Posts

Blog posts are stored in the `src/content/blog/` directory using Markdown format. Each post should include the following frontmatter:

```markdown
---
title: "Post Title"
description: "Post description"
pubDate: "Publication date (e.g., Mar 15 2025)"
heroImage: "/image-path.jpg"
---

Post content...
```

### Game Content

Game-related content is stored in the `src/content/games/` directory using Markdown format.

### Images and Media

All static media files should be placed in the `public/` directory.

## Website Content Maintenance Guide

### Home Page

The home page should include:
- Studio introduction
- Latest game showcase
- Recent news/blog posts
- Development progress updates

### Games Pages

Each game should have a dedicated page including:
- Game overview
- Features and highlights
- Screenshots and videos
- Development progress
- Technical specifications
- Download/purchase links (if applicable)

### Team Page

The team page should include:
- Team introduction
- Member profiles and roles
- Studio culture and values

### Blog

The blog should be regularly updated with:
- Development logs
- Game design insights
- Technical articles
- Team updates
- Industry perspectives

### Media Resources

The media resources page should provide:
- High-resolution game screenshots
- Game logos and artwork
- Press releases
- Contact information

## Contact

- Email: contact@sincloy.com
- Twitter: [@Sincloy](https://x.com/Sincloy)

## License

© Sincloy Games. All rights reserved.
