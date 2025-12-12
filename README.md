# OAF Ethiopia Monthly Newsletter

A monthly newsletter for One Acre Fund Ethiopia's Monitoring, Evaluation & Learning (MEL) team.

## Project Overview

This project showcases monthly newsletters with OAF Ethiopia branding. The site features:

- **OAF Branding Colors**: Primary green (#2b7f68) and accent gold (#e8b757)
- **Responsive Design**: Grid-based layout for newsletter listings
- **Monthly Archives**: Easy browsing of all past newsletters
- **PDF Export**: Each newsletter can be exported as PDF

## Project Structure

```
newsletter/
├── _quarto.yml              # Quarto configuration
├── _includes/               # HTML includes for newsletter layout
│   ├── newsletter-header.html
│   └── newsletter-footer.html
├── _layouts/                # Quarto layouts
│   └── newsletter.qmd
├── posts/
│   └── monthly/             # Monthly newsletters
│       ├── 2025-12/         # December 2025 issue
│       ├── 2026-01/         # January 2026 issue
│       └── index.qmd        # Newsletter archive page
├── images/                  # Logo and images
├── styles.css               # OAF branding styles
└── index.qmd                # Homepage
```

## Adding a New Monthly Newsletter

To add a new monthly newsletter:

1. Create a new folder in `posts/monthly/` with the format `YYYY-MM` (e.g., `2026-02` for February 2026)

2. Create an `index.qmd` file in that folder with the following template:

```yaml
---
title: "OAF Ethiopia MEL — [Month] [Year]"
date: YYYY-MM-01
categories: [newsletter]
layout: newsletter
format:
  html: default
  pdf: default
---

## Editor's Note

Welcome to the [Month] [Year] issue of the OAF Ethiopia MEL monthly newsletter.

## Monthly Highlight — [Topic]

A summary of the highlight, followed by an in-depth analysis.

### Background

Provide context for the highlight.

### Key Findings

- Finding 1
- Finding 2

## Upcoming Priority

What we'll focus on next month — key actions and asks for readers.

---

If you'd like to suggest topics or subscribe, click the Subscribe button in the header or footer.
```

3. Render the project:
```bash
quarto render
```

4. The new newsletter will automatically appear on the homepage and archive page.

## Building and Previewing

To build the project:
```bash
quarto render
```

To preview locally:
```bash
quarto preview
```

## Customization

### Colors
Edit `styles.css` to modify OAF branding colors:
- `--oaf-primary`: Main green color (#2b7f68)
- `--oaf-accent`: Gold accent color (#e8b757)
- `--oaf-light`: Light green background (#e8f4f0)

### Header/Footer
Edit the files in `_includes/` to customize newsletter header and footer.

### Layout
Edit `_layouts/newsletter.qmd` to modify the newsletter page layout.

## Deployment

The site can be deployed to GitHub Pages or any static hosting service. The `_site/` folder contains the built HTML files ready for deployment.

## Contact

For questions or suggestions about the newsletter, contact the OAF Ethiopia MEL team.
