# Project Architecture Decisions & Context

This document explains key decisions made during the development of alassane.ai and provides context for future Claude instances working on this project.

## Project Overview
This is a Jekyll-based portfolio website that replicates the design from Alassane's Notion portfolio. The goal was to create a pixel-perfect match of the Notion design while maintaining clean, maintainable code.

## Key Architecture Decisions

### 1. Page Structure
- **`/about/index.html`** - Standalone HTML file instead of markdown in `_pages/`
  - Reason: Complex toggle sections and custom styling that required full HTML control
  - The Notion about page has collapsible sections that needed custom JavaScript
  - Easier to maintain exact Notion design with direct HTML

- **`_pages/` directory** - Contains markdown files for simpler pages
  - `projects.md`, `testimonials.md`, `contact.md`
  - These pages have simpler layouts that work well with Jekyll's markdown processing

- **`_projects/` directory** - Individual project pages
  - Each project has its own markdown file
  - Uses custom `project.html` layout to maintain consistent styling

### 2. Styling Approach
- **Two CSS files:**
  - `main.css` - Default Jekyll styles
  - `notion-dark.css` - Custom dark theme matching Notion exactly
  - Dark theme only applied to specific pages via conditional loading in `default.html`

- **Why separate CSS files?**
  - Maintains compatibility with default Jekyll setup
  - Easy to toggle between themes if needed
  - Clear separation of custom vs default styles

### 3. Navigation Structure
- Removed "Case Studies" page per user request
- Navigation order: Home → About → Projects → Testimonials → Contact
- All navigation links updated across multiple layout files

### 4. Image Management
- All images downloaded from Notion and stored locally in `/assets/`
- Named descriptively: `elise-tastet-profile.png`, `tastet-project-image.png`, etc.
- Profile images styled as circles to match Notion

## Commit Message Style Preferences

The user prefers **regular and clean commits** with the following characteristics:

### Good Commit Examples:
```
Fix testimonials page layout - ensure image and text display side by side
Transform contact page to match Notion design exactly
Remove case studies page and update navigation
Add project images and implement YouTube video embed
```

### Commit Style Guidelines:
1. **Clear and descriptive** - Explain what was changed and why
2. **Atomic commits** - Each commit should represent one logical change
3. **Present tense** - "Fix" not "Fixed", "Add" not "Added"
4. **No excessive detail** - Keep it concise but informative
5. **Include context** when helpful - e.g., "to match Notion design"

### Multi-line Commit Format:
```
Short summary line (50 chars or less)

- Bullet point for specific change 1
- Bullet point for specific change 2
- Include "Co-Authored-By: Claude" attribution
```

## Design Principles

### 1. Notion Fidelity
- **EXACT match** to Notion design is priority #1
- Dark theme: `rgb(25, 25, 25)` background
- Typography matches Notion's font stack
- Spacing and layout identical to source

### 2. Content Accuracy
- All text content pulled directly from Notion
- No editorial changes or additions
- Preserve formatting (bold, italics, links)
- Keep testimonials and quotes exact

### 3. User Preferences
- **"ultrathink"** - Be thorough and comprehensive
- Don't create documentation unless asked
- Prefer editing existing files over creating new ones
- No emojis unless specifically requested

## Technical Context

### Jekyll Configuration
- Using Jekyll 4.3.4
- Minimal plugins (just jekyll-feed and jekyll-seo-tag)
- Collections enabled for projects
- Permalinks set to pretty URLs

### Deployment
- GitHub Pages compatible
- Repository: https://github.com/AlassaneDialDiop/alassane_ai
- Main branch deployment

### Known Issues & Solutions
1. **Bundle install permissions** - Use `bundle config set --local path 'vendor/bundle'`
2. **Image display in testimonials** - Required CSS overrides with `!important`
3. **Dark theme not applying** - Fixed by adding page URLs to conditional in `default.html`

## Future Development Notes

### When Adding New Pages:
1. Decide: Simple content → `_pages/` markdown, Complex layout → standalone HTML
2. Add page URL to dark theme conditional in `_layouts/default.html`
3. Update navigation in `_includes/navigation.html` AND standalone HTML pages
4. Test responsive design on mobile

### When Updating Styles:
1. Check both `main.css` and `notion-dark.css` for conflicts
2. Use `!important` sparingly, only for overrides
3. Test on all pages - some use different layouts

### Working with Notion Content:
1. Use MCP Notion tools to fetch latest content
2. Download images locally rather than hotlinking
3. Preserve exact formatting and structure
4. Check for expired image URLs and re-download as needed

## Common Tasks

### Updating navigation:
- Edit `_includes/navigation.html` for Jekyll-processed pages
- Edit `/about/index.html` navigation section for the about page
- Edit `_layouts/project.html` for project pages

### Adding a new project:
1. Create markdown file in `_projects/` 
2. Add front matter with title, permalink, description
3. Download any associated images to `/assets/`
4. Update main projects page if needed

### Fixing image displays:
- Check CSS for conflicting max-width rules
- Ensure proper path to `/assets/`
- Add specific overrides in `notion-dark.css` if needed

Remember: The goal is always to match Notion exactly while maintaining clean, maintainable code.