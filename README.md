# vibescripts2 - Webflow Scripts

This project was created with [create-webflow-scripts](https://www.npmjs.com/package/create-webflow-scripts).

## 🚀 Your Project Setup

- **GitHub Username:** julianmemberstack
- **Repository:** vibescripts2
- **Webflow Domain:** vibescripts2.webflow.io

- **GitHub Pages URL:** https://julianmemberstack.github.io/vibescripts2

## 📋 Webflow Embed Code

Copy this code to your Webflow Site Settings → Custom Code → Head:

```html
<script>
(function() {
  const isDev = location.hostname.includes('.webflow.io');
  const baseUrl = isDev 
    ? 'http://localhost:3000/src' 
    : 'https://julianmemberstack.github.io/vibescripts2';
  
  // Scripts that load on EVERY page
  window.globalScripts = ['alert'];  // Add your global scripts here
  
  // Load the router
  const script = document.createElement('script');
  script.src = baseUrl + '/router.js';
  document.head.appendChild(script);
})();
</script>
```

## 🛠 Development

### Start Development Server
```bash
npm run dev
```

### Create New Script
```bash
npm run new-script my-script-name
```

### Build for Production
```bash
npm run build
```

## 📁 Project Structure

```
vibescripts2/
├── src/
│   ├── router.js          # Script router (don't modify)
│   └── scripts/           # Your scripts go here
│       └── alert.js       # Example script
├── dist/                  # Production build (auto-generated)
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Pages deployment
└── package.json
```

## 🚢 Deploy to GitHub Pages

1. **Initialize Git:**
   ```bash
   git init
   git add .
   git commit -m "Initial setup"
   ```

2. **Create GitHub Repository:**
   - Go to https://github.com/new
   - Name it: **vibescripts2**
   - Don't initialize with README
   - Create repository

3. **Push to GitHub:**
   ```bash
   git remote add origin https://github.com/julianmemberstack/vibescripts2.git
   git push -u origin main
   ```

4. **Enable GitHub Pages:**
   - Go to https://github.com/julianmemberstack/vibescripts2/settings/pages
   - Under "Source", select **GitHub Actions**
   - Save

5. **Deploy:**
   Every push to main will auto-deploy!

## 📝 Adding Scripts

### Global Script (loads on every page)
1. Create: `src/scripts/my-script.js`
2. Update embed code: `window.globalScripts = ['my-script'];`
3. Publish Webflow

### Page-Specific Script
1. Create: `src/scripts/contact-form.js`
2. In page settings add:
   ```html
   <script>window.pageScript = 'contact-form';</script>
   ```
3. Publish Webflow

## 🆘 Troubleshooting

- **Scripts not loading?** Check browser console (F12)
- **Dev server running?** Should see "VITE ready" in terminal
- **Published Webflow?** Required after adding embed code
- **Hard refresh:** Cmd+Shift+R (Mac) or Ctrl+F5 (Windows)

## 📚 Learn More

- [Full Documentation](https://github.com/julianmemberstack/webflow-vibe-scripts)
- [Report Issues](https://github.com/julianmemberstack/webflow-vibe-scripts/issues)
