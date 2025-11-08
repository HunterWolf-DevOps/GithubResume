# ⚡ Quick Start Guide

Get your live resume online in **5 minutes**!

## 🎯 What You'll Get

A professional, futuristic resume website with:
- ✨ Stunning animations and effects
- 📱 Mobile-responsive design
- 🚀 Fast loading speed
- 🎨 Modern cyberpunk aesthetic
- 🔗 Shareable link

## 📋 Prerequisites

- GitHub account (free) - [Sign up here](https://github.com/join)
- Your resume information ready
- 5 minutes of your time

## 🚀 3-Step Deployment

### Step 1: Get the Code (1 minute)

**Option A: Download ZIP**
1. Click the green "Code" button on GitHub
2. Select "Download ZIP"
3. Extract the files to a folder

**Option B: Clone with Git**
```bash
git clone https://github.com/YOUR-USERNAME/live-resume.git
cd live-resume
```

### Step 2: Customize (2 minutes)

Open `index.html` and update:

1. **Your Name** (Line ~40):
```html
<h1 class="glitch" data-text="YOUR NAME">YOUR NAME</h1>
```

2. **Your Title** (Line ~42):
```html
<p class="hero-subtitle">Your Professional Title</p>
```

3. **Contact Info** (Lines ~250-270):
```html
<p>your.email@example.com</p>
```

4. **LinkedIn URL** (Line ~50):
```html
<a href="https://linkedin.com/in/YOUR-PROFILE">
```

### Step 3: Deploy to GitHub Pages (2 minutes)

1. **Create new repository** on GitHub
   - Name it: `your-name-resume`
   - Make it **Public**

2. **Upload files**:
   ```bash
   git init
   git add .
   git commit -m "My live resume"
   git remote add origin https://github.com/YOUR-USERNAME/your-name-resume.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Source: main branch
   - Click Save

4. **Done!** Your site is live at:
   ```
   https://YOUR-USERNAME.github.io/your-name-resume/
   ```

## 🎨 Quick Customization Tips

### Change Colors

Edit `styles.css` (Lines 1-8):
```css
:root {
    --primary-color: #00f3ff;    /* Change this! */
    --secondary-color: #ff00ff;  /* And this! */
}
```

### Add Your Photo

1. Add your photo to the project folder
2. In `index.html`, add after line 45:
```html
<div class="profile-photo">
    <img src="your-photo.jpg" alt="Your Name">
</div>
```

3. In `styles.css`, add:
```css
.profile-photo img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    border: 3px solid var(--primary-color);
    box-shadow: 0 0 30px rgba(0, 243, 255, 0.5);
}
```

### Update Experience

Find the experience section in `index.html` (around line 120) and modify:
```html
<div class="timeline-item">
    <div class="timeline-marker"></div>
    <div class="timeline-content">
        <span class="timeline-date">2024 - Present</span>
        <h3>Your Job Title</h3>
        <h4>Company Name | Location</h4>
        <ul>
            <li>Your achievement 1</li>
            <li>Your achievement 2</li>
        </ul>
    </div>
</div>
```

### Update Skills

Find the skills section (around line 200):
```html
<div class="skill-category">
    <h3><i class="fas fa-code"></i> Your Skill Category</h3>
    <div class="skill-tags">
        <span class="skill-tag">Skill 1</span>
        <span class="skill-tag">Skill 2</span>
    </div>
</div>
```

## 📱 Test Your Site

### Locally
```bash
# Open in browser
open index.html

# Or use a local server
python -m http.server 8000
# Visit: http://localhost:8000
```

### Online
Visit: `https://YOUR-USERNAME.github.io/your-name-resume/`

## 🔄 Making Updates

After making changes:
```bash
git add .
git commit -m "Updated resume"
git push origin main
```

Site updates automatically in 1-2 minutes!

## 🎯 Next Steps

### Enhance Your Resume

1. **Add Projects Section**
   - Showcase your work
   - Include GitHub links
   - Add project images

2. **Add Certifications**
   - List your credentials
   - Include badge images
   - Link to verification

3. **Add Blog/Articles**
   - Share your knowledge
   - Link to Medium/Dev.to
   - Showcase thought leadership

4. **Add Testimonials**
   - Client feedback
   - Colleague recommendations
   - LinkedIn endorsements

### Share Your Resume

- 📧 Email signature
- 💼 LinkedIn profile
- 🐦 Twitter bio
- 📱 QR code (use [QR Code Generator](https://www.qr-code-generator.com/))

### Track Visitors

Add Google Analytics:
1. Create account at [analytics.google.com](https://analytics.google.com)
2. Get tracking ID
3. Add code to `index.html` before `</head>`

## 🆘 Common Issues

### Site shows 404
- Wait 2-5 minutes after enabling Pages
- Check file is named `index.html` (lowercase)
- Ensure repository is public

### Styles not loading
- Clear browser cache (Ctrl+Shift+R)
- Check file paths are correct
- Verify `styles.css` is in same folder

### Mobile menu not working
- Check `script.js` is loaded
- Open browser console (F12) for errors
- Ensure JavaScript is enabled

## 💡 Pro Tips

1. **Use a custom domain** ($10-15/year)
   - More professional
   - Easier to remember
   - Better for SEO

2. **Keep it updated**
   - Add new experiences
   - Update skills
   - Refresh projects

3. **Get feedback**
   - Share with friends
   - Ask for suggestions
   - Iterate and improve

4. **Monitor performance**
   - Use [PageSpeed Insights](https://pagespeed.web.dev/)
   - Optimize images
   - Minimize code

## 📚 Resources

- [GitHub Pages Docs](https://docs.github.com/pages)
- [HTML Tutorial](https://www.w3schools.com/html/)
- [CSS Tutorial](https://www.w3schools.com/css/)
- [JavaScript Tutorial](https://www.w3schools.com/js/)

## 🎉 You're Done!

Congratulations! You now have a professional live resume.

**Share it with the world! 🌍**

---

Need help? Open an issue on GitHub or contact via LinkedIn:
🔗 [linkedin.com/in/blackhawk](https://www.linkedin.com/in/blackhawk/)
