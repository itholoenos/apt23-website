# Cycling Company Website - Setup Guide

This is a Jekyll-based website configured for GitHub Pages with custom domain support.

## Initial Setup

### 1. Update Configuration

Edit `_config.yml` and update these values with your actual information:
```yaml
title: Cycling Company  # Your company name
email: contact@example.com  # Your contact email
url: "https://example.com"  # Your custom domain
```

### 2. Configure Custom Domain

#### Option A: Using a Subdomain (e.g., www.example.com)
1. Update the `CNAME` file with your domain:
   ```
   www.example.com
   ```
2. In your domain registrar, add a `CNAME` record pointing to `yourgithubusername.github.io`

#### Option B: Using an Apex Domain (e.g., example.com)
1. Update the `CNAME` file with your domain:
   ```
   example.com
   ```
2. In your domain registrar, add these DNS records:
   - `A` records pointing to GitHub Pages IP addresses:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - `AAAA` records (IPv6):
     - 2606:50c0:8000::153
     - 2606:50c0:8001::153
     - 2606:50c0:8002::153
     - 2606:50c0:8003::153

### 3. Update Social Links
Edit `_config.yml` and add your social media usernames:
```yaml
twitter_username: your_twitter_handle
github_username: your_github_username
```

## Local Development

### Build and Serve Locally
```bash
bundle exec jekyll serve
```
Visit `http://localhost:4000` in your browser.

### Build for Production
```bash
bundle exec jekyll build
```

## File Structure

- `_posts/` - Blog post content (Markdown files)
- `_layouts/` - Page templates
- `_includes/` - Reusable page components
- `assets/` - CSS, JavaScript, images
- `_config.yml` - Site configuration
- `about.markdown` - About page template

## Publishing to GitHub Pages

1. Commit your changes:
   ```bash
   git add .
   git commit -m "Initial Jekyll site setup"
   git push origin main
   ```

2. Enable GitHub Pages:
   - Go to your repository settings
   - Navigate to "Pages" section
   - Select "Deploy from a branch" (if not already selected)
   - Choose the `main` branch as source
   - Save

3. GitHub will automatically build and deploy your site within a few minutes.

4. Check deployment status in the "Pages" section of repository settings.

## Theme

The site uses the **Minima** theme by default. To customize, see `_config.yml`.

## Next Steps

1. Customize the homepage (`index.markdown`)
2. Update the about page (`about.markdown`)
3. Add product/service pages to `_layouts/`
4. Create blog posts in `_posts/`
5. Add images to `assets/images/`

## Resources

- [Jekyll Documentation](https://jekyllrb.com/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Minima Theme Documentation](https://github.com/jekyll/minima)
