# Quick Start Guide - OAF Ethiopia Newsletter

## Creating Your First Monthly Newsletter

### Step 1: Create a New Folder
Create a new folder in `posts/monthly/` with the format `YYYY-MM`:
```
posts/monthly/2026-02/
```

### Step 2: Copy the Template
Copy the content from `NEWSLETTER_TEMPLATE.qmd` and create `index.qmd` in your new folder.

### Step 3: Update the Template
Replace the placeholders:
- `[MONTH] [YEAR]` → e.g., "February 2026"
- `YYYY-MM-01` → e.g., "2026-02-01"
- Add your content in each section

### Step 4: Render the Project
```bash
quarto render
```

### Step 5: Preview
Open `_site/index.html` in your browser to see the newsletter.

## Example Newsletter Structure

```
posts/monthly/2026-02/
└── index.qmd
```

## File Content Example

```yaml
---
title: "OAF Ethiopia MEL — February 2026"
date: "2026-02-01"
categories: [newsletter]
layout: newsletter
format:
  html: default
  pdf: default
---

## Editor's Note

Welcome to the February 2026 issue...

## Monthly Highlight — [Your Topic]

Your content here...
```

## Customizing the Newsletter

### Add Images
Place images in the newsletter folder and reference them:
```markdown
![Alt text](image.jpg)
```

### Add Code Blocks
```markdown
```{r}
# Your R code here
```
```

### Add Tables
```markdown
| Column 1 | Column 2 |
|----------|----------|
| Data 1   | Data 2   |
```

### Add Callouts
```markdown
:::{.callout-note}
This is a note
:::

:::{.callout-warning}
This is a warning
:::
```

## Deployment

Once you're happy with your newsletter:

1. Commit changes to git
2. Push to your repository
3. Deploy to GitHub Pages or your hosting service

The `_site/` folder contains all the HTML files ready for deployment.

## Need Help?

- Check the README.md for more detailed information
- Review existing newsletters in `posts/monthly/` for examples
- Refer to [Quarto documentation](https://quarto.org/) for advanced features

## OAF Branding Colors

- **Primary Green**: #2b7f68
- **Accent Gold**: #e8b757
- **Light Green**: #e8f4f0

These colors are automatically applied to all newsletters through the CSS styling.
