# Local Development Guide

This guide explains how to set up and run this website locally for development and testing purposes.

## Overview

This is a static HTML/CSS/JavaScript website that can be run locally using any web server. No build process or dependencies are required.

## Prerequisites

You need a local web server to properly test the website. This is necessary because:
- Browsers apply CORS restrictions when opening HTML files directly
- Some features may not work correctly with the `file://` protocol
- You want to test the website as it would appear when deployed

## Setup Instructions

### Option 1: Using Python (Recommended for Linux/Mac)

Python comes pre-installed on most Linux distributions and macOS systems.

#### On Linux/Mac:

1. **Navigate to the project directory:**
   ```bash
   cd /path/to/HasyimAP.github.io
   ```

2. **Start the server:**
   
   For Python 3 (most common):
   ```bash
   python3 -m http.server 8000
   ```
   
   Or for Python 2:
   ```bash
   python -m SimpleHTTPServer 8000
   ```

3. **Open your browser and visit:**
   ```
   http://localhost:8000
   ```

4. **To stop the server:**
   Press `Ctrl + C` in the terminal

### Option 2: Using Python on Windows

1. **Open Command Prompt or PowerShell**

2. **Navigate to the project directory:**
   ```cmd
   cd C:\path\to\HasyimAP.github.io
   ```

3. **Check if Python is installed:**
   ```cmd
   python --version
   ```
   
   If not installed, download it from [python.org](https://www.python.org/downloads/)

4. **Start the server:**
   ```cmd
   python -m http.server 8000
   ```

5. **Open your browser and visit:**
   ```
   http://localhost:8000
   ```

6. **To stop the server:**
   Press `Ctrl + C` in the command prompt

### Option 3: Using Node.js (Cross-platform)

If you have Node.js installed, you can use a simple HTTP server package.

1. **Install http-server globally (one-time setup):**
   ```bash
   npm install -g http-server
   ```

2. **Navigate to the project directory:**
   ```bash
   cd /path/to/HasyimAP.github.io
   ```

3. **Start the server:**
   ```bash
   http-server -p 8000
   ```

4. **Open your browser and visit:**
   ```
   http://localhost:8000
   ```

5. **To stop the server:**
   Press `Ctrl + C` in the terminal

### Option 4: Using Live Server (VS Code Extension)

If you use Visual Studio Code:

1. **Install the "Live Server" extension:**
   - Open VS Code
   - Go to Extensions (Ctrl+Shift+X or Cmd+Shift+X)
   - Search for "Live Server"
   - Install it

2. **Open the project folder in VS Code:**
   ```bash
   code /path/to/HasyimAP.github.io
   ```

3. **Start Live Server:**
   - Right-click on `index.html`
   - Select "Open with Live Server"
   - Or click "Go Live" in the status bar

4. **The website will automatically open in your default browser**

5. **Live Server features:**
   - Auto-reload on file changes
   - Usually runs on port 5500

### Option 5: Using PHP (If installed)

If you have PHP installed:

```bash
cd /path/to/HasyimAP.github.io
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

### Option 6: Using Ruby (If installed)

If you have Ruby installed:

```bash
cd /path/to/HasyimAP.github.io
ruby -run -ehttpd . -p8000
```

Then visit `http://localhost:8000` in your browser.

## Making Changes

1. **Edit the files:**
   - Use any text editor or IDE
   - Main files:
     - `index.html` - Homepage
     - `whoami.html` - About page
     - `college stuff.html` - College materials page
     - `css/style.css` - Homepage styles
     - `css/whoami style.css` - About page styles
     - `css/college style.css` - College page styles

2. **Test your changes:**
   - Save the file
   - Refresh your browser (F5 or Cmd+R)
   - For Live Server, changes auto-reload

3. **Check across different browsers:**
   - Chrome/Edge
   - Firefox
   - Safari

4. **Test responsive design:**
   - Use browser DevTools (F12)
   - Toggle device toolbar
   - Test different screen sizes

## Project Structure

```
HasyimAP.github.io/
├── index.html              # Homepage
├── whoami.html            # About page
├── college stuff.html     # College materials page
├── css/
│   ├── style.css          # Homepage styles
│   ├── whoami style.css   # About page styles
│   └── college style.css  # College page styles
├── images/
│   ├── background.jpeg    # Background wallpaper
│   ├── profile.jpeg       # Profile picture
│   ├── icon-*.png/jpg     # Social media icons
│   └── course-*.jpg/png   # Course material images
├── robots.txt             # Search engine directives
├── sitemap.xml           # Site structure for search engines
└── DEVELOPMENT.md        # This file
```

## Common Issues and Solutions

### Issue: "Address already in use" error

**Solution:** The port is already being used by another application.
- Try a different port: `python3 -m http.server 8080`
- Or find and stop the process using that port

### Issue: Changes not showing up

**Solution:**
- Hard refresh the browser: `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)
- Clear browser cache
- Ensure you saved the file

### Issue: Images not loading

**Solution:**
- Check image paths are correct
- Ensure images exist in the `images/` folder
- Check for typos in filenames (case-sensitive on Linux/Mac)

### Issue: CSS not applying

**Solution:**
- Check the CSS file path in the HTML
- Ensure CSS file is saved
- Clear browser cache
- Check browser console (F12) for errors

## Deployment

This website is hosted on GitHub Pages. To deploy changes:

1. **Commit your changes:**
   ```bash
   git add .
   git commit -m "Your commit message"
   ```

2. **Push to GitHub:**
   ```bash
   git push origin main
   ```

3. **GitHub Pages will automatically deploy the changes**
   - Usually takes 1-2 minutes
   - Visit your site at: https://hasyimap.github.io

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [MDN Web Docs](https://developer.mozilla.org/)
- [HTML5 Reference](https://www.w3.org/TR/html52/)
- [CSS Reference](https://www.w3.org/Style/CSS/)

## Getting Help

If you encounter issues:
1. Check the browser console (F12) for error messages
2. Verify all file paths are correct
3. Ensure all required files are present
4. Try a different browser
5. Check that your local server is running

---

**Happy Coding! 🚀**
