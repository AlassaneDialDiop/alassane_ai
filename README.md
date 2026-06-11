# Alassane.ai - Portfolio Website

Personal portfolio website for Alassane Diop - ML / AI Engineer. Built with Jekyll and designed to match the Notion portfolio aesthetic.

## 🌟 Overview

This website is a pixel-perfect recreation of Alassane's Notion portfolio, featuring a dark theme and modern design. It showcases ML/AI engineering projects, client testimonials, and professional expertise in building and shipping AI systems.

## 🎨 Design Philosophy

- **Notion-Inspired**: Exact replication of the Notion portfolio design
- **Dark Theme**: Clean dark interface with `rgb(25, 25, 25)` background
- **Responsive**: Mobile-friendly layout that works on all devices
- **Minimalist**: Focus on content with clean typography and spacing

## 🛠 Tech Stack

- **Static Site Generator**: Jekyll 4.3.4
- **Hosting**: GitHub Pages (alassane.ai)
- **Styling**: Custom CSS with Notion-style dark theme
- **Integrations**: 
  - Calendly for appointment scheduling
  - YouTube video embeds
  - MCP Notion integration for content sync

## 📁 Project Structure

```
alassane_ai/
├── _includes/         # Reusable components
│   └── navigation.html
├── _layouts/          # Page templates
│   ├── default.html
│   ├── page.html
│   └── project.html
├── _pages/            # Main pages (markdown)
│   ├── projects.md
│   ├── testimonials.md
│   └── contact.md
├── _projects/         # Individual project pages
│   ├── text-classification-nlp.md
│   ├── recommender-system-tastet.md
│   ├── ai-quality-assurance.md
│   └── ...
├── about/            # About page (standalone HTML)
│   └── index.html
├── assets/           # Static assets
│   ├── css/
│   │   ├── main.css
│   │   └── notion-dark.css
│   └── *.png         # Project and profile images
├── _config.yml       # Jekyll configuration
├── index.md          # Homepage
└── why_certain_decisions.md  # Architecture documentation
```

## 🚀 Local Development

### Prerequisites
- Ruby 2.6+ 
- Bundler
- Git

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/AlassaneDialDiop/alassane_ai.git
   cd alassane_ai
   ```

2. Install dependencies:
   ```bash
   bundle config set --local path 'vendor/bundle'
   bundle install
   ```

3. Run locally:
   ```bash
   bundle exec jekyll serve
   ```

4. View at: http://localhost:4000

### Common Tasks

**Adding a new project:**
1. Create a new `.md` file in `_projects/`
2. Add front matter:
   ```yaml
   ---
   layout: project
   title: "Project Title"
   permalink: /projects/project-name/
   description: "Brief description"
   ---
   ```
3. Add project content and images

**Updating navigation:**
- Edit `_includes/navigation.html` for most pages
- Edit `/about/index.html` for the about page navigation
- Edit `_layouts/project.html` for project page navigation

**Working with images:**
- Store all images in `/assets/`
- Use descriptive names (e.g., `project-name-image.png`)
- Profile images are automatically styled as circles

## 📝 Content Management

### Commit Style Guidelines
- Use clear, descriptive commit messages
- Present tense ("Add feature" not "Added feature")
- Keep commits atomic - one logical change per commit
- Include context when helpful

Example:
```
Fix testimonials page layout - ensure image and text display side by side

- Add specific CSS overrides for image display
- Maintain responsive behavior on mobile
- Match Notion design exactly
```

### Design Decisions
See `why_certain_decisions.md` for detailed explanations of:
- Why certain pages are HTML vs Markdown
- CSS architecture choices
- Navigation structure decisions
- Image management approach

## 🌐 Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the main branch. Custom domain configuration is handled via:
- CNAME file in repository
- DNS settings for alassane.ai

## 📄 Pages

- **Home** - Introduction and expertise overview
- **About** - Detailed background with collapsible sections
- **Projects** - Portfolio of ML/AI engineering projects
- **Testimonials** - Client feedback and project outcomes
- **Contact** - Contact information and Calendly integration

## 🎯 Features

- **Dark Theme**: Modern dark interface matching Notion
- **Project Showcase**: Detailed case studies with images
- **Client Testimonials**: Social proof with profile images
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Fast Loading**: Static site with optimized assets
- **SEO Optimized**: Meta tags and structured content
- **Easy Updates**: Markdown-based content management

## 📞 Contact

**Alassane Diop**  
Email: alassanedialdiop@gmail.com  
LinkedIn: [linkedin.com/in/alassanediop](https://linkedin.com/in/alassanediop)  
Website: [alassane.ai](https://alassane.ai)

---

Built with ❤️ using Jekyll and inspired by Notion's clean design aesthetic.