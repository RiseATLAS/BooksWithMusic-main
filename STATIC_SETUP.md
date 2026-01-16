# Static HTML Setup (No Build Required)

This project now runs as pure static HTML/CSS/JavaScript without any build tools or compilation.

## Running Locally

### Option 1: Simple HTTP Server (Recommended)
```bash
# If you have Node.js installed:
npm start
# Opens at http://localhost:8080

# Or use Python:
python3 -m http.server 8080
# Opens at http://localhost:8080

# Or use PHP:
php -S localhost:8080
```

### Option 2: Open Directly in Browser
⚠️ **Note:** Some browsers block ES6 modules when opening `file://` URLs directly.

If you see CORS errors, use one of the HTTP server options above.

## File Structure
```
BooksWithMusic-main/
├── index.html          # Main library page
├── reader.html         # Book reader page
├── styles.css          # All styles
├── service-worker.js   # Offline support
└── js/                 # All JavaScript modules
    ├── main.js
    ├── auth/
    ├── config/
    ├── core/
    ├── storage/
    └── ui/
```

## Deployment to GitHub Pages

1. **Enable GitHub Pages:**
   - Go to your repo Settings → Pages
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Save

2. **Your site will be live at:**
   `https://yourusername.github.io/BooksWithMusic/`

3. **No build step required!** GitHub Pages serves static files directly.

## What Changed from Vite

- ✅ Removed Vite build process
- ✅ All files now in root directory (not `public/`)
- ✅ Uses relative paths (`./styles.css` instead of `/styles.css`)
- ✅ ES6 modules work directly in modern browsers
- ✅ JSZip loaded from CDN (no npm install needed for browser)
- ✅ Works with any static file server

## Browser Requirements

- Modern browser with ES6 module support:
  - Chrome 61+
  - Firefox 60+
  - Safari 11+
  - Edge 79+

## No Installation Required

The app uses:
- Pure JavaScript (ES6 modules)
- JSZip from CDN for EPUB parsing
- Firebase SDK from CDN (optional, for cloud features)

No `npm install` or build step needed to run!
