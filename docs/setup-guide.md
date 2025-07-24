# 🚀 Website Setup Guide

> **How to run and deploy your Docsify personal website**

This guide will help you set up, run locally, and deploy your personal website built with Docsify.

---

## 📋 Prerequisites

### **Required Software**
- **Node.js** (version 14 or higher)
- **npm** (comes with Node.js)
- **Git** (for version control and deployment)

### **Check Your Installation**
```bash
# Check Node.js version
node --version

# Check npm version  
npm --version

# Check Git version
git --version
```

---

## ⚡ Quick Start (Local Development)

### **1. Install Docsify CLI**
```bash
npm install -g docsify-cli
```

### **2. Navigate to Your Project**
```bash
cd Personal_Website
```

### **3. Serve the Website Locally**
```bash
docsify serve docs
```

### **4. Open in Browser**
Your website will be available at: **http://localhost:3000**

**That's it!** Your personal website is now running locally. 🎉

---

## 🌐 Deployment Options

### **Option 1: GitHub Pages (Recommended)**

**Step 1**: Create a GitHub repository
```bash
# Initialize Git (if not already done)
git init

# Add all files
git add .

# Commit changes
git commit -m "Initial commit - Personal website"

# Add GitHub remote (replace with your repository URL)
git remote add origin https://github.com/dannychantszfong/personal-website.git

# Push to GitHub
git push -u origin main
```

**Step 2**: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll to **Pages** section
4. Set source to **Deploy from a branch**
5. Select branch: **main**
6. Select folder: **/ (root)** or **/docs**
7. Click **Save**

**Your website will be live at**: `https://dannychantszfong.github.io/personal-website/`

### **Option 2: Netlify**

**Step 1**: Build for deployment
```bash
# No build step needed - Docsify serves static files directly
```

**Step 2**: Deploy to Netlify
1. Go to [netlify.com](https://www.netlify.com)
2. Sign up/Sign in
3. Click **"Add new site"** → **"Deploy manually"**
4. Drag and drop your entire `docs` folder
5. Your site will be live immediately with a random URL
6. You can customize the URL in site settings

### **Option 3: Vercel**

**Step 1**: Install Vercel CLI
```bash
npm install -g vercel
```

**Step 2**: Deploy
```bash
# Navigate to docs folder
cd docs

# Deploy with Vercel
vercel

# Follow the prompts
```

### **Option 4: Surge.sh (Simple & Fast)**

**Step 1**: Install Surge
```bash
npm install -g surge
```

**Step 2**: Deploy
```bash
# Navigate to docs folder
cd docs

# Deploy to Surge
surge

# Choose domain or use generated one
```

---

## 📁 File Structure Explanation

```
Personal_Website/
├── docs/                    # Docsify website root
│   ├── index.html          # Docsify configuration
│   ├── README.md           # Homepage content  
│   ├── _coverpage.md       # Landing page
│   ├── _sidebar.md         # Navigation menu
│   ├── _navbar.md          # Top navigation
│   ├── cv.md              # Professional CV page
│   ├── projects.md        # Portfolio page
│   ├── skills.md          # Skills & expertise
│   ├── contact.md         # Contact information
│   ├── certifications.md  # Professional credentials
│   ├── interests.md       # Personal interests
│   └── setup-guide.md     # This file
├── cv.html                # Original CV file (not linked)
├── cv.md                  # CV source content
├── read_word.py           # Python utility script
└── requirements.txt       # Python dependencies
```

---

## 🛠️ Customization Guide

### **Update Content**
- **Homepage**: Edit `docs/README.md`
- **About/Profile**: Edit `docs/_coverpage.md`
- **Navigation**: Edit `docs/_sidebar.md`
- **CV Content**: Edit `docs/cv.md`
- **Projects**: Edit `docs/projects.md`

### **Styling Changes**
Edit the `<style>` section in `docs/index.html`:

```css
/* Custom theme colors */
:root {
  --theme-color: #0066cc;        /* Main theme color */
  --text-color-dark: #333;       /* Text color */
  --border-color: #e6e6e6;       /* Border color */
}
```

### **Add New Pages**
1. Create new `.md` file in `docs/` folder
2. Add link to `_sidebar.md` navigation
3. Content will be automatically available

### **SEO Optimization**
Update meta tags in `docs/index.html`:
```html
<meta name="description" content="Your custom description">
<meta name="keywords" content="your,custom,keywords">
<meta property="og:title" content="Your Custom Title">
```

---

## 🔧 Advanced Configuration

### **Enable Google Analytics**
Uncomment and update the analytics section in `docs/index.html`:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR_GA_ID');
</script>
```

### **Add Custom Domain (GitHub Pages)**
1. Create `CNAME` file in `docs/` folder
2. Add your domain: `www.yourname.com`
3. Configure DNS with your domain provider

### **Enable HTTPS**
- **GitHub Pages**: Automatic HTTPS
- **Netlify**: Automatic HTTPS + custom domains
- **Vercel**: Automatic HTTPS + custom domains

---

## 🐛 Troubleshooting

### **Common Issues**

**Issue**: "docsify: command not found"
**Solution**: 
```bash
npm install -g docsify-cli
# or
npx docsify serve docs
```

**Issue**: Pages not updating
**Solution**: 
- Hard refresh browser (Ctrl+F5)
- Clear browser cache
- Check file names and paths

**Issue**: Sidebar not showing
**Solution**: 
- Ensure `loadSidebar: true` in `index.html`
- Check `_sidebar.md` exists and has correct content

**Issue**: Coverpage not displaying
**Solution**:
- Ensure `coverpage: true` in `index.html`  
- Check `_coverpage.md` exists

### **Development Tips**
- Use browser developer tools to debug styling
- Check browser console for JavaScript errors
- Docsify hot-reloads automatically during development
- Test on different screen sizes for responsiveness

---

## 📈 Performance Optimization

### **Loading Speed**
- Docsify loads content dynamically (already optimized)
- Images should be compressed and properly sized
- Minimize custom CSS and JavaScript

### **SEO Best Practices**
- Use descriptive page titles and meta descriptions
- Add structured data markup
- Ensure all links work correctly
- Submit sitemap to search engines

---

## 🆙 Updates & Maintenance

### **Regular Updates**
```bash
# Pull latest changes (if collaborating)
git pull origin main

# Make your updates
# Edit .md files as needed

# Commit and push changes
git add .
git commit -m "Update content"
git push origin main
```

### **Content Workflow**
1. **Edit locally** and test with `docsify serve docs`
2. **Review changes** in browser
3. **Commit and push** to GitHub
4. **Automatic deployment** (GitHub Pages/Netlify/etc.)

---

## 🚀 You're All Set!

Your professional personal website is ready to impress visitors and potential employers. The website includes:

✅ **Professional Design** - Clean, modern appearance  
✅ **Mobile Responsive** - Works on all devices  
✅ **SEO Optimized** - Google-friendly structure  
✅ **Easy to Maintain** - Simple Markdown editing  
✅ **Fast Loading** - Optimized performance  
✅ **Professional Features** - CV, portfolio, contact info  

### **Next Steps**
1. **Deploy your website** using one of the options above
2. **Share your URL** on LinkedIn, GitHub profile, email signature
3. **Keep content updated** as you gain new skills and complete projects
4. **Monitor analytics** (if enabled) to track visitors

**Need help?** Check the Docsify documentation or reach out!

---

**🎉 Congratulations on your new professional website!** 

Your online presence is now ready to showcase your skills and help advance your career in data science and software development. 