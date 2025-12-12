# OAF Ethiopia Newsletter - Documentation Index

Welcome to the OAF Ethiopia Newsletter project! This document provides an overview of all available documentation.

## 📋 Quick Navigation

### Getting Started
- **[PROJECT_SUMMARY.md](PROJECT_SUMMARY.md)** - Overview of what's been done and current state
- **[QUICKSTART.md](QUICKSTART.md)** - Quick start guide for creating your first newsletter

### Detailed Guides
- **[README.md](README.md)** - Complete project documentation
- **[CUSTOMIZATION.md](CUSTOMIZATION.md)** - How to customize branding and layout
- **[DEPLOYMENT.md](DEPLOYMENT.md)** - How to deploy your newsletter online

### Templates
- **[NEWSLETTER_TEMPLATE.qmd](NEWSLETTER_TEMPLATE.qmd)** - Template for creating new newsletters

---

## 📚 Documentation Overview

### PROJECT_SUMMARY.md
**What it covers:**
- Project overview and what's been completed
- Current newsletter issues
- Key features
- File structure
- How to add new newsletters
- Next steps

**When to read:**
- First time reviewing the project
- Understanding what's been done
- Getting an overview of the project

---

### QUICKSTART.md
**What it covers:**
- Step-by-step guide to create a new newsletter
- Example newsletter structure
- How to add images, code, tables, and callouts
- Deployment basics
- OAF branding colors

**When to read:**
- Creating your first newsletter
- Need quick instructions
- Want to get started immediately

---

### README.md
**What it covers:**
- Complete project overview
- Project structure explanation
- Detailed instructions for adding newsletters
- Building and previewing
- Customization options
- Deployment information

**When to read:**
- Need comprehensive documentation
- Understanding the full project structure
- Reference guide for all features

---

### CUSTOMIZATION.md
**What it covers:**
- Branding customization (colors, logo, text)
- Layout customization (homepage, archive, newsletter)
- Site configuration
- Newsletter content customization
- Advanced customization options
- Responsive design
- Performance optimization
- Troubleshooting

**When to read:**
- Want to change colors or branding
- Need to modify layout
- Want to customize the site
- Troubleshooting styling issues

---

### DEPLOYMENT.md
**What it covers:**
- Pre-deployment checklist
- Multiple deployment options:
  - GitHub Pages (recommended)
  - Netlify
  - Vercel
  - Manual deployment
- Custom domain setup
- SSL certificates
- Monitoring deployments
- Troubleshooting
- Performance optimization
- Analytics setup

**When to read:**
- Ready to deploy your newsletter
- Need to set up a custom domain
- Want to enable automatic updates
- Troubleshooting deployment issues

---

### NEWSLETTER_TEMPLATE.qmd
**What it covers:**
- Template structure for new newsletters
- All standard sections
- Placeholder text for customization

**When to read:**
- Creating a new monthly newsletter
- Need a starting point for content

---

## 🎯 Common Tasks

### I want to...

#### Create a new newsletter
1. Read: [QUICKSTART.md](QUICKSTART.md)
2. Use: [NEWSLETTER_TEMPLATE.qmd](NEWSLETTER_TEMPLATE.qmd)
3. Reference: [README.md](README.md) - Adding a New Monthly Newsletter section

#### Change the colors/branding
1. Read: [CUSTOMIZATION.md](CUSTOMIZATION.md) - Branding Customization section
2. Edit: `styles.css`

#### Deploy the newsletter online
1. Read: [DEPLOYMENT.md](DEPLOYMENT.md)
2. Choose your hosting option
3. Follow the setup steps

#### Understand the project structure
1. Read: [PROJECT_SUMMARY.md](PROJECT_SUMMARY.md)
2. Reference: [README.md](README.md) - Project Structure section

#### Customize the layout
1. Read: [CUSTOMIZATION.md](CUSTOMIZATION.md) - Layout Customization section
2. Edit: `_layouts/newsletter.qmd` or `_includes/` files

#### Add images to a newsletter
1. Read: [QUICKSTART.md](QUICKSTART.md) - Add Images section
2. Place images in the newsletter folder
3. Reference in markdown

#### Troubleshoot an issue
1. Check: [CUSTOMIZATION.md](CUSTOMIZATION.md) - Troubleshooting section
2. Check: [DEPLOYMENT.md](DEPLOYMENT.md) - Troubleshooting section
3. Check: [README.md](README.md) for general help

---

## 📁 Project Structure

```
newsletter/
├── Documentation Files
│   ├── README.md                      # Full documentation
│   ├── QUICKSTART.md                  # Quick start guide
│   ├── CUSTOMIZATION.md               # Customization guide
│   ├── DEPLOYMENT.md                  # Deployment guide
│   ├── PROJECT_SUMMARY.md             # Project overview
│   └── DOCUMENTATION_INDEX.md         # This file
│
├── Configuration
│   ├── _quarto.yml                    # Site configuration
│   └── styles.css                     # OAF branding styles
│
├── Templates & Includes
│   ├── NEWSLETTER_TEMPLATE.qmd        # Newsletter template
│   ├── _layouts/
│   │   └── newsletter.qmd             # Newsletter layout
│   └── _includes/
│       ├── newsletter-header.html     # Newsletter header
│       └── newsletter-footer.html     # Newsletter footer
│
├── Content
│   ├── index.qmd                      # Homepage
│   ├── about.qmd                      # About page
│   └── posts/
│       └── monthly/
│           ├── 2025-12/               # December 2025 issue
│           ├── 2026-01/               # January 2026 issue
│           └── index.qmd              # Newsletter archive
│
├── Assets
│   ├── images/
│   │   └── logo.svg                   # OAF logo
│   └── profile.jpg                    # Profile image
│
└── Generated
    └── _site/                         # Built website (generated)
```

---

## 🎨 OAF Branding Colors

- **Primary Green**: #2b7f68
- **Accent Gold**: #e8b757
- **Light Green**: #e8f4f0
- **Text Primary**: #111111
- **Text Secondary**: #333333
- **Text Muted**: #666666
- **Background**: #f7f7f7

---

## 🚀 Quick Commands

```bash
# Render the site
quarto render

# Preview locally
quarto preview

# Create a new newsletter
# 1. Create folder: posts/monthly/YYYY-MM/
# 2. Create file: index.qmd
# 3. Copy content from NEWSLETTER_TEMPLATE.qmd
# 4. Run: quarto render
```

---

## 📞 Support

For help with:
- **Quarto**: https://quarto.org/docs/
- **GitHub Pages**: https://docs.github.com/en/pages
- **Netlify**: https://docs.netlify.com/
- **Vercel**: https://vercel.com/docs

---

## ✅ Checklist for First Newsletter

- [ ] Read QUICKSTART.md
- [ ] Create folder: `posts/monthly/2026-02/`
- [ ] Create file: `index.qmd`
- [ ] Copy template from NEWSLETTER_TEMPLATE.qmd
- [ ] Update title and date
- [ ] Add your content
- [ ] Run `quarto render`
- [ ] Preview in browser
- [ ] Deploy using DEPLOYMENT.md

---

## 📝 Version Information

- **Quarto**: 1.6.40+
- **Project Type**: Quarto Website
- **Theme**: Cosmo with OAF Branding
- **Format**: HTML + PDF

---

**Start with [QUICKSTART.md](QUICKSTART.md) to create your first newsletter!**
