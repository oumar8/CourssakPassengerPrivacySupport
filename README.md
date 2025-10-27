# Courssak Privacy Policy Pages

This repository contains the privacy policy pages for both the Courssak Passenger and Driver apps.

## Pages

- **Passenger App Privacy Policy**: `index.html`
- **Driver App Privacy Policy**: `driver.html`

## How to Deploy to GitHub Pages

### Method 1: Using GitHub Settings (Recommended)

1. **Push your code to GitHub**:
   ```bash
   git add .
   git commit -m "Add driver privacy policy page"
   git push origin main
   ```

2. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Click on **Settings**
   - Scroll down to **Pages** section (in the left sidebar under "Code and automation")
   - Under **Source**, select **Deploy from a branch**
   - Under **Branch**, select `main` (or `master`) and `/ (root)`
   - Click **Save**

3. **Access your site**:
   - After a few minutes, your site will be live at:
   - `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/`
   - Passenger page: `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/`
   - Driver page: `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/driver.html`

### Method 2: Using GitHub Actions (Advanced)

If you want more control, you can use GitHub Actions:

1. Create `.github/workflows/deploy.yml`:
   ```yaml
   name: Deploy to GitHub Pages

   on:
     push:
       branches: [ main ]

   jobs:
     deploy:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v2
         - name: Deploy to GitHub Pages
           uses: peaceiris/actions-gh-pages@v3
           with:
             github_token: ${{ secrets.GITHUB_TOKEN }}
             publish_dir: ./
   ```

2. Enable GitHub Pages from the `gh-pages` branch

## Local Development

To test locally, simply open `index.html` or `driver.html` in your web browser, or use a local server:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (if you have http-server installed)
npx http-server
```

Then visit `http://localhost:8000` in your browser.

## Features

- ✅ Responsive design for mobile and desktop
- ✅ Navigation between Passenger and Driver pages
- ✅ Clean, modern UI following Apple design guidelines
- ✅ Accessible and SEO-friendly
- ✅ No dependencies - pure HTML/CSS

## Updating Content

To update the privacy policies:
1. Edit `index.html` for passenger app changes
2. Edit `driver.html` for driver app changes
3. Update the "Last Updated" date in both files
4. Commit and push to GitHub

## Custom Domain (Optional)

To use a custom domain:
1. Add a `CNAME` file with your domain name
2. Configure DNS settings at your domain provider
3. Add your custom domain in GitHub Pages settings

## Support

For questions or support, contact: goal.direct9@gmail.com

