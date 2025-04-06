# ButterflAI Website

This repository contains the source code for the ButterflAI website, built using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## Website Structure

The website is organized into key sections, each with multiple articles:

- **Build**: Technical guides for building AI systems
- **Deploy**: Resources for deploying AI systems to production
- **Blog**: Articles on various AI-related topics
- **Team**: Team member profiles
- **Testimonials**: Customer testimonials
- **Contact**: Contact information and form

## Setup

1. Clone this repository:
```bash
git clone <repository-url>
cd butterflai
```

2. Create and activate a virtual environment:
```bash
# Using venv
python -m venv venv
source venv/bin/activate  # On Linux/macOS
.\venv\Scripts\activate   # On Windows

# Or using uv
uv venv
uv venv activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
# or
uv add mkdocs-material mkdocs-git-revision-date-localized-plugin mkdocs-glightbox mkdocs-material-extensions pillow cairosvg
```

## Local Development

To serve the website locally:

```bash
mkdocs serve
```

The site will be available at `http://127.0.0.1:8000`

## Adding New Articles

### Article Structure

Each article should be placed in its own directory with an `index.md` file. This allows for easy organization of related assets and makes URLs cleaner.

Example structure for an article:
```
docs/
├── blog/
│   ├── my-new-article/
│   │   ├── index.md          # Main content
│   │   ├── image1.png        # Related images
│   │   └── code-sample.py    # Code samples
```

### Article Metadata

Each article should include front matter metadata at the top:

```yaml
---
title: Article Title
description: Brief description of the article
date: 2024-09-10
updated: 2024-09-10  # Optional, only if updated after initial publication
authors:
  - name: Author Name
    title: Author Title
tags:
  - Tag1
  - Tag2
categories:
  - Category1
difficulty: Beginner  # Optional: Beginner, Intermediate, Advanced
---

# Article Content Starts Here
```

### Adding to Navigation

After creating a new article, add it to the navigation in `mkdocs.yml`:

```yaml
nav:
  - Build:
      - Overview: build/index.md
      - Existing Articles: ...
      - Your New Article: build/your-new-article/index.md
```

### Organization Tips

1. **For the Build section**:
   - Keep technical guides organized by topic
   - Use clear, descriptive names
   - Group related articles under "Topics"

2. **For the Deploy section**:
   - Organize by deployment phase or technology
   - Include practical examples and code samples
   - Reference related articles when appropriate

3. **For the Blog section**:
   - Organize by topic categories
   - Include publishing date in metadata
   - Use consistent tagging

## Adding Images

Store images in the relevant article directory or in `docs/assets/` for shared images:

```markdown
![Image Alt Text](image1.png)  # Image in the same directory as the article
![Shared Image](../assets/shared-image.png)  # Shared image
```

## Article Templates

### Blog Post Template

```markdown
---
title: Title Here
description: Brief description here
date: YYYY-MM-DD
authors:
  - name: Author Name
    title: Author Title
tags:
  - Tag1
  - Tag2
categories:
  - Category
---

# Title

Introduction paragraph that explains what the article is about and why it matters.

## First Section

Content here...

## Second Section

More content here...

## Conclusion

Summarize key points and provide next steps or related resources.
```

### Technical Guide Template

```markdown
---
title: Title Here
description: Brief description here
date: YYYY-MM-DD
updated: YYYY-MM-DD
authors:
  - name: Author Name
    title: Author Title
tags:
  - Tag1
  - Tag2
categories:
  - Category
difficulty: Beginner/Intermediate/Advanced
---

# Title

Introduction that explains what this guide covers and what the reader will learn.

## Prerequisites

* Requirement 1
* Requirement 2

## Step 1: First Task

Instructions and explanation...

```bash
# Code example
command --option value
```

## Step 2: Second Task

More instructions...

## Common Issues and Solutions

Issue 1: Description
Solution: How to fix it

## Next Steps

Suggest related guides or advanced topics.
```

## Deployment

The site is automatically deployed using GitHub Pages when changes are pushed to the main branch:

```bash
# Deploy manually
mkdocs gh-deploy
```

## Contributing

1. Create a new branch for your changes
2. Make your changes and test locally
3. Submit a pull request

## License

Copyright © 2025 ButterflAI. All rights reserved.
