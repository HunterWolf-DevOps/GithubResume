# 🚀 Deployment Guide

## GitHub Pages Deployment (Recommended)

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name it: `live-resume` or `your-name-resume`
5. Make it **Public** (required for free GitHub Pages)
6. Click "Create repository"

### Step 2: Upload Your Files

**Option A: Using Git Command Line**

```bash
# Initialize git in your project folder
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: Live resume website"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR-USERNAME/live-resume.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Option B: Using GitHub Desktop**

1. Download and install [GitHub Desktop](https://desktop.github.com/)
2. Click "Add" → "Add Existing Repository"
3. Select your project folder
4. Click "Publish repository"
5. Choose your repository name and make it public
6. Click "Publish Repository"

**Option C: Upload via GitHub Website**

1. Go to your repository on GitHub
2. Click "uploading an existing file"
3. Drag and drop all your files
4. Click "Commit changes"

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" tab
3. Scroll down to "Pages" in the left sidebar
4. Under "Source":
   - Select branch: **main**
   - Select folder: **/ (root)**
5. Click "Save"
6. Wait 1-2 minutes for deployment

### Step 4: Access Your Live Site

Your site will be available at:
```
https://YOUR-USERNAME.github.io/live-resume/
```

Example: `https://ramakrishnan-s.github.io/live-resume/`

---

## Custom Domain Setup (Optional)

### Step 1: Purchase a Domain

Buy a domain from:
- [Namecheap](https://www.namecheap.com)
- [Google Domains](https://domains.google)
- [GoDaddy](https://www.godaddy.com)

### Step 2: Configure DNS

Add these DNS records at your domain provider:

```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153

Type: CNAME
Name: www
Value: YOUR-USERNAME.github.io
```

### Step 3: Configure GitHub Pages

1. Go to repository Settings → Pages
2. Under "Custom domain", enter your domain
3. Click "Save"
4. Wait for DNS check (can take up to 24 hours)
5. Enable "Enforce HTTPS"

---

## Alternative Deployment Options

### Netlify (Free)

1. **Sign up** at [Netlify](https://www.netlify.com)
2. Click "Add new site" → "Import an existing project"
3. Connect your GitHub account
4. Select your repository
5. Click "Deploy site"
6. Your site is live at: `random-name.netlify.app`
7. Optional: Add custom domain in Site settings

**Advantages:**
- Automatic deployments on git push
- Free SSL certificate
- Form handling
- Serverless functions

### Vercel (Free)

1. **Sign up** at [Vercel](https://vercel.com)
2. Click "New Project"
3. Import your GitHub repository
4. Click "Deploy"
5. Your site is live at: `project-name.vercel.app`

**Advantages:**
- Excellent performance
- Automatic deployments
- Preview deployments for PRs
- Edge network

### Cloudflare Pages (Free)

1. **Sign up** at [Cloudflare Pages](https://pages.cloudflare.com)
2. Click "Create a project"
3. Connect your GitHub account
4. Select your repository
5. Click "Begin setup" → "Save and Deploy"

**Advantages:**
- Global CDN
- Unlimited bandwidth
- DDoS protection
- Fast performance

---

## Updating Your Live Site

### Method 1: Git Command Line

```bash
# Make your changes to files
# Then:

git add .
git commit -m "Update resume content"
git push origin main
```

Your site will automatically update in 1-2 minutes!

### Method 2: GitHub Website

1. Go to your repository
2. Click on the file you want to edit
3. Click the pencil icon (Edit)
4. Make your changes
5. Click "Commit changes"

### Method 3: GitHub Desktop

1. Make changes to your files
2. Open GitHub Desktop
3. Review changes
4. Add commit message
5. Click "Commit to main"
6. Click "Push origin"

---

## Troubleshooting

### Site Not Loading

**Check:**
1. Repository is public
2. GitHub Pages is enabled in Settings
3. Branch is set to "main"
4. Wait 2-5 minutes after enabling

**Solution:**
```bash
# Force rebuild by making a small change
git commit --allow-empty -m "Trigger rebuild"
git push origin main
```

### 404 Error

**Check:**
1. File is named `index.html` (lowercase)
2. File is in root directory
3. Repository name matches URL

### Styles Not Loading

**Check:**
1. File paths are correct (case-sensitive)
2. CSS file is named `styles.css`
3. Clear browser cache (Ctrl+Shift+R)

### Custom Domain Not Working

**Check:**
1. DNS records are correct
2. Wait 24-48 hours for DNS propagation
3. CNAME file exists in repository
4. "Enforce HTTPS" is enabled

---

## Performance Optimization

### Enable Caching

Add this to your repository root as `.htaccess`:

```apache
<IfModule mod_expires.c>
  ExpiresActive On
  ExpiresByType text/css "access plus 1 year"
  ExpiresByType application/javascript "access plus 1 year"
  ExpiresByType image/png "access plus 1 year"
  ExpiresByType image/jpg "access plus 1 year"
</IfModule>
```

### Minify Files (Optional)

Use online tools:
- [CSS Minifier](https://cssminifier.com/)
- [JavaScript Minifier](https://javascript-minifier.com/)

### Image Optimization

- Use WebP format for images
- Compress images with [TinyPNG](https://tinypng.com/)
- Use appropriate image sizes

---

## Security Best Practices

1. **Never commit sensitive data**
   - API keys
   - Passwords
   - Personal information

2. **Use HTTPS**
   - Always enable "Enforce HTTPS" in GitHub Pages

3. **Keep dependencies updated**
   - Update Font Awesome CDN link regularly

4. **Validate user input**
   - If you add forms, validate on both client and server

---

## Monitoring & Analytics

### Add Google Analytics

Add before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Monitor Uptime

Use free services:
- [UptimeRobot](https://uptimerobot.com/)
- [StatusCake](https://www.statuscake.com/)

---

## Need Help?

- **GitHub Pages Docs**: https://docs.github.com/pages
- **GitHub Community**: https://github.community/
- **Stack Overflow**: Tag your questions with `github-pages`

---

**Happy Deploying! 🚀**
