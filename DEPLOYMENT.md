# Deployment Guide - Training Brochure PWA

## Quick Start - Make Your Brochure Accessible via Link

### Option 1: Free Hosting Services (Recommended)

#### GitHub Pages (Free)
1. Create a GitHub account at https://github.com
2. Create a new repository
3. Upload all files (brochure.html, manifest.json, service-worker.js)
4. Go to Settings → Pages
5. Select main branch and save
6. Your brochure will be available at: `https://yourusername.github.io/repository-name/brochure.html`

#### Netlify (Free)
1. Go to https://www.netlify.com
2. Sign up for free account
3. Drag and drop your folder or connect to GitHub
4. Your brochure will be live instantly with a custom URL
5. You can customize the domain name

#### Vercel (Free)
1. Go to https://vercel.com
2. Sign up for free account
3. Import your project or drag and drop
4. Deploy instantly - get a shareable link

#### Firebase Hosting (Free)
1. Go to https://firebase.google.com
2. Create a project
3. Install Firebase CLI: `npm install -g firebase-tools`
4. Run: `firebase init hosting`
5. Deploy: `firebase deploy`

### Option 2: Traditional Web Hosting
Upload all files to your web hosting provider via FTP:
- brochure.html
- manifest.json
- service-worker.js

### Option 3: Local Network Sharing
1. Use a local server like Python's HTTP server:
   ```bash
   python -m http.server 8000
   ```
2. Access from same network: `http://your-ip:8000/brochure.html`

## Features After Deployment

Once deployed, your brochure will have:

✅ **Shareable Link** - Send the URL to anyone
✅ **Mobile App** - Installable on phones (PWA)
✅ **Desktop App** - Installable on computers
✅ **Offline Access** - Works without internet
✅ **Fast Loading** - Cached for quick access
✅ **App-like Experience** - Native app feel

## Testing Locally

1. Use a local server (don't open HTML file directly):
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Node.js
   npx http-server
   
   # PHP
   php -S localhost:8000
   ```

2. Open in browser: `http://localhost:8000/brochure.html`

3. Test PWA features:
   - Open DevTools → Application → Service Workers
   - Check "Add to Home Screen" functionality
   - Test offline mode

## Mobile Installation

### Android (Chrome)
1. Open the brochure link
2. Tap menu (3 dots) → "Add to Home Screen"
3. Or tap "Install App" button if shown

### iPhone (Safari)
1. Open the brochure link
2. Tap Share button → "Add to Home Screen"
3. Or tap "Install App" button if shown

### Desktop (Chrome/Edge)
1. Open the brochure link
2. Look for install icon in address bar
3. Or click "Install App" button

## Customization

### Update Contact Information
- Edit the contact section directly in the browser
- Changes are saved to browser storage

### Change Colors/Branding
- Edit CSS variables in the `<style>` section
- Update theme-color in manifest.json

### Add Your Logo
- Replace icon data URIs in manifest.json with your logo URLs

## Troubleshooting

### PWA Not Installing?
- Ensure you're using HTTPS (or localhost)
- Check that manifest.json is accessible
- Verify service-worker.js is registered

### Service Worker Not Working?
- Clear browser cache
- Check browser console for errors
- Ensure service-worker.js is in root directory

### Share Link Not Working?
- Make sure the file is hosted (not file://)
- Check that the URL is accessible publicly

## Support

For issues or questions, check:
- Browser console for errors
- Network tab for failed requests
- Application tab for service worker status


