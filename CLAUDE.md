# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the official website for Sincloy Games, an independent game development studio. The site is built with Astro framework and deployed to Cloudflare Workers. It serves as the studio's online presence, showcasing games, team information, development blog, and press resources.

## Tech Stack

- **Framework**: Astro 5.1.3 with TypeScript
- **Deployment**: Cloudflare Workers via Wrangler
- **Content**: MDX for blog posts and content management
- **Styling**: CSS with custom properties and global styles
- **Integrations**: Astro sitemap, RSS feed generation

## Development Commands

```bash
# Install dependencies
npm install

# Start development server (with hot reload)
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview

# Type checking and deployment validation
npm run check

# Deploy to Cloudflare Workers
npm run deploy

# Generate TypeScript types for Wrangler
npm run types
```

## Architecture

### Content Management System
- Blog posts are managed through Astro's content collections in `src/content/blog/`
- Content schema defined in `src/content.config.ts` with Zod validation
- Each blog post requires frontmatter: `title`, `description`, `pubDate`, optional `updatedDate` and `heroImage`

### Site Structure
- **Components**: Reusable Astro components in `src/components/` (BaseHead, Header, Footer, etc.)
- **Layouts**: Page templates in `src/layouts/` (BlogPost layout for content)
- **Pages**: Route-based pages in `src/pages/` including dynamic blog routes via `[...slug].astro`
- **Global Config**: Site constants in `src/consts.ts` (SITE_TITLE, SITE_DESCRIPTION)

### Deployment Configuration
- Astro config (`astro.config.mjs`) uses Cloudflare adapter with platform proxy enabled
- Wrangler config (`wrangler.json`) configured for observability and source maps
- TypeScript config extends Astro's strict configuration with Cloudflare Workers types

### SEO and Meta Management
- BaseHead component handles all meta tags, Open Graph, Twitter cards
- Canonical URLs, font preloading, and favicon management
- Google AdSense integration configured

## Content Guidelines

### Adding Blog Posts
Create new `.md` files in `src/content/blog/` with required frontmatter:
```markdown
---
title: "Post Title"
description: "Brief description"
pubDate: "2025-03-15"
heroImage: "/image-path.jpg" # optional
---
```

### Game Pages
Game-specific pages should be created in `src/pages/games/` following the existing pattern established in `project-nova.astro`.

### Static Assets
All images, fonts, and static files go in `public/` directory and are served at root path.

## Important Notes

- Site title and description are centralized in `src/consts.ts`
- The site uses custom fonts (Atkinson Regular/Bold) with preloading optimization
- RSS feed is generated automatically for blog posts via `src/pages/rss.xml.js`
- Cloudflare Workers deployment includes observability and source map upload
- TypeScript strict mode is enabled with Cloudflare Workers types