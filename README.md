# AI Consulting Company Website

This repository contains the source code for our company website, built using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## Setup

1. Clone this repository:
```bash
git clone <repository-url>
cd website
```

2. Create and activate a virtual environment:
```bash
uv venv
uv venv activate  # On Windows PowerShell
```

3. Install dependencies:
```bash
uv add mkdocs-material mkdocs-git-revision-date-localized-plugin mkdocs-glightbox mkdocs-material-extensions pillow cairosvg
```

## Local Development

To serve the website locally:

```bash
mkdocs serve
```

The site will be available at `http://127.0.0.1:8000`

## Building the Site

To build the static site:

```bash
mkdocs build
```

The built site will be in the `site` directory.

## Deployment

The site is automatically deployed using GitHub Pages when changes are pushed to the main branch.

## Project Structure

```
.
├── docs/
│   ├── assets/         # Images and other static files
│   ├── blog/           # Blog posts
│   ├── projects/       # Project case studies
│   ├── solutions/      # Solution descriptions
│   ├── team/           # Team member profiles
│   ├── index.md        # Home page
│   ├── contact.md      # Contact page
│   └── testimonials.md # Customer testimonials
├── mkdocs.yml         # MkDocs configuration
└── README.md          # This file
```

## Content Management

### Adding Blog Posts

1. Create a new `.md` file in the `docs/blog` directory
2. Add the blog post metadata at the top of the file:
```yaml
---
title: Your Blog Title
description: Brief description of the post
date: 2024-03-21
authors:
  - name: Author Name
    title: Author Title
---
```

### Adding Projects

1. Create a new `.md` file in the `docs/projects` directory
2. Follow the project template structure:
```yaml
---
title: Project Title
client: Client Name
industry: Industry Type
date: 2024-03-21
---
```

## Customization

### Theme Customization

The theme settings can be modified in `mkdocs.yml`. See the [Material for MkDocs documentation](https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/) for more options.

### Adding New Pages

1. Create a new `.md` file in the appropriate directory
2. Add the page to the navigation in `mkdocs.yml`

## Contributing

1. Create a new branch for your changes
2. Make your changes and test locally
3. Submit a pull request

## License

Copyright © 2024 AI Consulting Company. All rights reserved.
