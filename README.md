# Aquilon Security Website

Official website for Aquilon Security LLC, a cybersecurity products company. Available at [aquilon.dev](https://aquilon.dev).

## Overview

This repository contains the source code for the Aquilon Security website, built with Hugo static site generator and deployed via GitHub Pages.

## Technology Stack

- Hugo (Static Site Generator)
- GitHub Pages (Hosting)
- GitHub Actions (CI/CD)
- HTML/CSS/JavaScript

## Getting Started

### Prerequisites

- Git
- Hugo (0.101.0 or later)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/[username]/aquilon-website.git
cd aquilon-website
```

2. Install Hugo:
```bash
# macOS
brew install hugo

# Windows (Chocolatey)
choco install hugo

# Linux (Snap)
snap install hugo

# Or download from https://gohugo.io/installation/
```

### Development

Run the development server:
```bash
# Start server with live reload
hugo server -D

# Start server on specific port
hugo server -D -p 1313

# Include future and expired content
hugo server -DF
```

The site will be available at http://localhost:1313

### Building for Production

Build the static files:
```bash
# Build site
hugo

# Build with drafts
hugo -D

# Build with verbose output
hugo --verbose
```

The built site will be in the `public/` directory.

## Deployment

The website is automatically deployed to GitHub Pages via GitHub Actions when changes are pushed to the main branch.

### Manual Deployment Setup

1. GitHub Pages should be configured to deploy from the `gh-pages` branch
2. The custom domain (aquilon.dev) should be configured in repository settings
3. A CNAME file with `aquilon.dev` should exist in the `static/` directory

## Project Structure

```
aquilon-website/
├── archetypes/        # Content templates
├── assets/            # Asset files to be processed by Hugo
├── content/           # Site content (Markdown files)
├── data/              # Data files (JSON/YAML/TOML)
├── layouts/           # HTML templates
│   ├── _default/      # Default layouts
│   ├── partials/      # Partial templates
│   └── index.html     # Homepage template
├── public/            # Built site (git-ignored)
├── static/            # Static files (copied as-is)
├── themes/            # Hugo themes
├── hugo.toml          # Hugo configuration
├── CLAUDE.md          # AI assistant guidance
└── README.md          # This file
```

## Creating Content

### New Page
```bash
hugo new content/about.md
```

### Homepage Content
Edit `content/_index.md` or create custom layout in `layouts/index.html`

## Contributing

This is a private repository for Aquilon Security LLC. For any questions or concerns, please contact the repository owner.

## License

© 2024 Aquilon Security LLC. All rights reserved.