# GitHub Pages Deployment Checklist

Follow these steps to deploy your cycling company website on GitHub Pages:

## Step 1: Prepare Your Content (✓ Already Done)
- [x] Jekyll site initialized
- [x] `_config.yml` updated with basic cycling company info
- [x] Homepage and About page customized
- [x] Sample blog post created
- [ ] Replace placeholder information with your actual details
- [ ] Add your company logo/images to `assets/images/`

## Step 2: Update Configuration

Before deploying, update `_config.yml` with:

```yaml
title: "Your Cycling Company Name"
email: "your-email@company.com"
description: "Your company description"
url: "https://yourdomain.com"  # Replace with your custom domain
```

Also update `CNAME` file:
```
yourdomain.com
```

## Step 3: Commit Your Changes

```bash
cd /workspaces/apt23-website
git add .
git commit -m "Initial cycling company website setup"
git push origin main
```

## Step 4: Enable GitHub Pages

1. Go to your GitHub repository: `https://github.com/itholoenos/apt23-website`
2. Click **Settings** → **Pages**
3. Under "Build and deployment":
   - Select **Deploy from a branch**
   - Choose **main** branch
   - Select **root** folder
4. Click **Save**

GitHub will now automatically build and deploy your site!

## Step 5: Configure Custom Domain (After GitHub Pages is Live)

1. Confirm GitHub Pages is working at `https://itholoenos.github.io/apt23-website`
2. Go to your domain registrar
3. Update DNS records to point to GitHub Pages:
   - **For subdomain (www.example.com)**: Create CNAME record pointing to `itholoenos.github.io`
   - **For apex domain (example.com)**: Create A records pointing to GitHub's IPs (see SETUP_GUIDE.md)
4. GitHub will automatically verify the domain (may take 24-48 hours)
5. Enable HTTPS: Go back to GitHub Pages settings and check "Enforce HTTPS"

## Step 6: Verify Deployment

- Check deployment status in **Settings** → **Pages**
- Visit your domain in a browser
- Verify the site loads correctly with your content

## Troubleshooting

**Site not building?**
- Check the "Actions" tab for build errors
- Verify your branch is set correctly in Pages settings
- Ensure `Gemfile` is present

**Custom domain not connecting?**
- Verify CNAME file has correct domain
- Wait 24-48 hours for DNS propagation
- Check DNS records with: `nslookup yourdomain.com`

**HTTPS not available?**
- GitHub Pages HTTPS might take a few mins to provision
- Refresh GitHub Pages settings page after DNS updates

## Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Pages custom domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Jekyll Documentation](https://jekyllrb.com/docs/)

---

**Next Steps:**
1. Customize the content with your company information
2. Add images to `assets/`
3. Create additional pages for products/services
4. Publish the site following this checklist
