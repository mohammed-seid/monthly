# Customization Guide - OAF Ethiopia Newsletter

## Branding Customization

### Colors
Edit `styles.css` to change the OAF branding colors:

```css
:root {
	--oaf-primary: #2b7f68;      /* Main green */
	--oaf-accent: #e8b757;       /* Gold accent */
	--oaf-light: #e8f4f0;        /* Light green background */
	--text-primary: #111111;     /* Main text */
	--text-secondary: #333333;   /* Secondary text */
	--text-muted: #666666;       /* Muted text */
	--bg: #f7f7f7;               /* Page background */
}
```

### Logo
Replace `images/logo.svg` with your OAF Ethiopia logo. The logo will appear in:
- Navigation bar
- Newsletter header

### Newsletter Header
Edit `_includes/newsletter-header.html` to customize:
- Logo alt text
- Newsletter title
- Subscribe button link

### Newsletter Footer
Edit `_includes/newsletter-footer.html` to customize:
- Footer text
- Subscribe button link
- Copyright information

## Layout Customization

### Homepage
Edit `index.qmd` to:
- Change the title and description
- Modify the grid layout (change `grid-columns: 2` to another number)
- Add or remove sections

### Newsletter Archive
Edit `posts/monthly/index.qmd` to:
- Change the archive page title
- Modify the grid layout
- Add additional information

### Newsletter Layout
Edit `_layouts/newsletter.qmd` to:
- Change the newsletter container styling
- Add custom elements before/after content

## Site Configuration

### Website Settings
Edit `_quarto.yml` to customize:

```yaml
website:
  title: "OAF Ethiopia Newsletter"  # Site title
  navbar:
    logo: images/logo.svg           # Logo path
    title: "OAF Ethiopia MEL"        # Navbar title
    right:
      - text: Newsletter
        href: index.html
      - icon: github
        href: https://github.com/    # Your GitHub
      - icon: twitter
        href: https://twitter.com    # Your Twitter
```

### Theme
The site uses the Cosmo theme with custom branding. To change the theme:

```yaml
format:
  html:
    theme:
      - cosmo                        # Change to: default, darkly, journal, etc.
      - brand
    css: styles.css
```

## Newsletter Content Customization

### Sections
Each newsletter can include:
- Editor's Note
- Monthly Highlight
- Program Updates
- Data Insights
- Upcoming Priorities

Add or remove sections as needed in your newsletter content.

### Metadata
Customize newsletter metadata in the YAML front matter:

```yaml
---
title: "OAF Ethiopia MEL — [Month] [Year]"
date: "YYYY-MM-01"
categories: [newsletter]
layout: newsletter
format:
  html: default
  pdf: default
---
```

## Advanced Customization

### Custom CSS
Add custom CSS to `styles.css` to:
- Change fonts
- Modify spacing
- Add animations
- Create custom components

### Custom HTML
Modify `_includes/newsletter-header.html` and `_includes/newsletter-footer.html` to:
- Add custom navigation
- Include social media links
- Add tracking code

### Quarto Extensions
Add Quarto extensions to `_quarto.yml` for:
- Additional themes
- Custom shortcodes
- Advanced formatting

## Responsive Design

The newsletter is designed to be responsive. Key breakpoints:

```css
@media (min-width: 760px) {
	/* Desktop styles */
}

@media (max-width: 759px) {
	/* Mobile styles */
}
```

Modify these breakpoints in `styles.css` as needed.

## Performance Optimization

### Image Optimization
- Use optimized images (PNG/JPG)
- Compress images before adding to newsletters
- Use appropriate image sizes

### CSS Optimization
- Minimize CSS in production
- Remove unused styles
- Use CSS variables for consistency

### Build Optimization
- Use `freeze: true` in `posts/_metadata.yml` to cache computations
- Minimize PDF rendering time
- Optimize asset loading

## Troubleshooting

### Newsletter not appearing
- Check the date format: `YYYY-MM-01`
- Ensure folder is in `posts/monthly/`
- Run `quarto render` to rebuild

### Styling not applied
- Clear browser cache
- Check CSS file path in `_quarto.yml`
- Verify CSS syntax

### PDF not generating
- Ensure XeTeX is installed
- Check for special characters in content
- Review PDF format settings in YAML

## Support

For more information:
- [Quarto Documentation](https://quarto.org/)
- [Quarto Websites](https://quarto.org/docs/websites/)
- [Quarto Styling](https://quarto.org/docs/output-formats/html-basics.html)
