# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is the website for Aquilon Security, a cybersecurity products company. Built with Hugo static site generator and deployed via GitHub Pages.

## Technology Stack
- Hugo (static site generator)
- GitHub Pages for hosting
- HTML/CSS/JavaScript for custom components

## Common Development Tasks

### Local Development
```bash
# Install Hugo (macOS)
brew install hugo

# Install Hugo (other systems)
# See: https://gohugo.io/installation/

# Run development server
hugo server -D

# Run with drafts and future posts visible
hugo server -DF

# Build for production
hugo

# Build with drafts included
hugo -D
```

### Creating Content
```bash
# Create new page
hugo new content/page-name.md

# Create new post (if using blog)
hugo new posts/post-title.md
```

### Deployment
- The site is built and deployed automatically via GitHub Actions
- Push to main branch triggers deployment
- Static files are generated in the `public/` directory
- GitHub Actions workflow handles building and deploying to gh-pages branch

## Project Structure
```
/
├── archetypes/        # Content templates
├── assets/            # Processed assets (SCSS, JS that needs processing)
├── content/           # Markdown content files
├── data/              # Data files (JSON, YAML, TOML)
├── layouts/           # HTML templates
│   ├── _default/      # Default layouts
│   ├── partials/      # Reusable template parts
│   └── index.html     # Homepage template
├── public/            # Generated site (git-ignored)
├── static/            # Static files (copied as-is)
├── themes/            # Hugo themes
├── hugo.toml          # Hugo configuration
├── CLAUDE.md          # This file
└── README.md          # Project documentation
```

## Hugo-Specific Guidelines
- Use Hugo's built-in functions and pipes when possible
- Keep templates DRY using partials
- Use Hugo's asset pipeline for SCSS/JS processing
- Leverage Hugo's image processing for optimization
- Use front matter for page-specific configurations

## Design Guidelines
- Keep the initial splash page simple and professional
- Focus on security-oriented aesthetic
- Ensure responsive design for mobile and desktop
- Optimize for fast loading times
- Use Hugo's minification features for production

## GitHub Pages Configuration
- Use GitHub Actions for automated deployment
- Build output goes to `public/` directory
- Deploy to gh-pages branch or docs/ folder
- Custom domain configuration via CNAME file in static/ directory