# Deployment Guide - OAF Ethiopia Newsletter

## Overview

Your OAF Ethiopia Newsletter is a static website that can be deployed to any hosting service. This guide covers the most popular deployment options.

## Pre-Deployment Checklist

Before deploying, ensure:

- [ ] All newsletters are created and tested
- [ ] Site renders without errors: `quarto render`
- [ ] Homepage looks correct
- [ ] Newsletter archive displays properly
- [ ] All links work correctly
- [ ] Branding colors are correct
- [ ] Logo is in place

## Deployment Options

### Option 1: GitHub Pages (Recommended)

GitHub Pages is free and integrates well with Quarto.

#### Setup:

1. **Create a GitHub repository**
   - Go to [github.com/new](https://github.com/new)
   - Name it `newsletter` or similar
   - Make it public

2. **Initialize git in your project**
   ```bash
   cd c:\Users\Lenovo\Desktop\newsletter
   git init
   git add .
   git commit -m "Initial commit: OAF Ethiopia Newsletter"
   ```

3. **Add remote and push**
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/newsletter.git
   git branch -M main
   git push -u origin main
   ```

4. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Select "Deploy from a branch"
   - Choose `main` branch and `/root` folder
   - Click Save

5. **Your site will be live at**
   ```
   https://YOUR_USERNAME.github.io/newsletter/
   ```

#### Automatic Updates:

To automatically rebuild when you push changes, create `.github/workflows/publish.yml`:

```yaml
name: Publish

on:
  push:
    branches: main

jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Set up Quarto
        uses: quarto-dev/quarto-actions/setup@v2
      
      - name: Render site
        run: quarto render
      
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./_site
```

### Option 2: Netlify

Netlify offers free hosting with automatic deployments.

#### Setup:

1. **Push to GitHub** (follow Option 1 steps 1-3)

2. **Connect to Netlify**
   - Go to [netlify.com](https://netlify.com)
   - Click "New site from Git"
   - Select GitHub and authorize
   - Choose your repository

3. **Configure build settings**
   - Build command: `quarto render`
   - Publish directory: `_site`
   - Click Deploy

4. **Your site will be live at**
   ```
   https://YOUR_SITE_NAME.netlify.app
   ```

### Option 3: Vercel

Vercel is optimized for static sites and offers excellent performance.

#### Setup:

1. **Push to GitHub** (follow Option 1 steps 1-3)

2. **Import to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository

3. **Configure**
   - Framework: Other
   - Build command: `quarto render`
   - Output directory: `_site`
   - Click Deploy

4. **Your site will be live at**
   ```
   https://YOUR_PROJECT.vercel.app
   ```

### Option 4: Manual Deployment

For other hosting services:

1. **Build locally**
   ```bash
   quarto render
   ```

2. **Upload `_site` folder**
   - Connect via FTP/SFTP
   - Use hosting provider's file manager
   - Upload all files from `_site/` to your web root

3. **Your site will be live at**
   ```
   https://yourdomain.com
   ```

## Custom Domain

### For GitHub Pages:

1. **Update DNS records** at your domain registrar:
   ```
   CNAME: YOUR_USERNAME.github.io
   ```

2. **Add domain to GitHub**
   - Go to repository Settings > Pages
   - Enter your custom domain
   - Click Save

### For Netlify:

1. **Update DNS records** at your domain registrar:
   ```
   CNAME: YOUR_SITE_NAME.netlify.app
   ```

2. **Add domain to Netlify**
   - Go to Site settings > Domain management
   - Click "Add custom domain"
   - Follow the prompts

### For Vercel:

1. **Add domain to Vercel**
   - Go to Project settings > Domains
   - Enter your domain
   - Follow DNS setup instructions

## SSL Certificate

Most hosting services provide free SSL certificates:
- **GitHub Pages**: Automatic
- **Netlify**: Automatic
- **Vercel**: Automatic
- **Other**: Check with your provider

## Monitoring

### Check deployment status:

**GitHub Pages:**
- Go to repository > Actions
- View workflow runs

**Netlify:**
- Go to Deploys tab
- View deployment history

**Vercel:**
- Go to Deployments tab
- View deployment status

## Troubleshooting

### Site not updating after push

1. **Check build status**
   - GitHub: Actions tab
   - Netlify: Deploys tab
   - Vercel: Deployments tab

2. **Check build logs** for errors

3. **Rebuild manually**
   - GitHub: Re-run workflow
   - Netlify: Trigger deploy
   - Vercel: Redeploy

### 404 errors

1. **Check file paths** in links
2. **Verify `_site/` folder** has all files
3. **Check publish directory** setting

### Styling not applied

1. **Clear browser cache** (Ctrl+Shift+Delete)
2. **Check CSS file** in `_site/styles.css`
3. **Verify CSS path** in HTML files

## Performance Optimization

### Before deployment:

1. **Optimize images**
   - Compress PNG/JPG files
   - Use appropriate sizes

2. **Minimize CSS**
   - Remove unused styles
   - Combine files

3. **Test performance**
   - Use [PageSpeed Insights](https://pagespeed.web.dev/)
   - Check load times

## Backup

### Regular backups:

1. **Backup locally**
   ```bash
   git clone https://github.com/YOUR_USERNAME/newsletter.git backup
   ```

2. **Backup to cloud**
   - Use GitHub as backup
   - Consider additional cloud storage

## Maintenance

### Regular tasks:

1. **Update newsletters** monthly
2. **Check links** quarterly
3. **Update dependencies** as needed
4. **Monitor analytics** (if enabled)

## Analytics (Optional)

### Add Google Analytics:

1. **Get tracking ID** from Google Analytics

2. **Add to `_quarto.yml`**:
   ```yaml
   website:
     google-analytics: "G-XXXXXXXXXX"
   ```

3. **Rebuild and deploy**

## Support

For deployment issues:
- Check hosting provider's documentation
- Review Quarto deployment guide: https://quarto.org/docs/publishing/
- Check GitHub Actions documentation

---

**Your newsletter is ready to deploy!** Choose your preferred hosting option and follow the setup steps above.
