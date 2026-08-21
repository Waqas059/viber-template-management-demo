# How to Share on GitHub - Step by Step Guide

## For Non-Technical Users

### Easiest Method: GitHub Web Interface

1. **Create GitHub Account**
   - Go to https://github.com
   - Click "Sign up"
   - Complete registration

2. **Create New Repository**
   - Click "+" icon (top right)
   - Select "New repository"
   - Name it: `viber-template-management-demo`
   - Description: "Interactive mockup of Viber template management for CPaaS"
   - Select "Public" (so anyone can access)
   - Check "Add a README file"
   - Click "Create repository"

3. **Upload Files**
   - Click "Add file" → "Upload files"
   - Drag & drop these files:
     - `viber-template-management-demo.html`
     - `README.md`
     - `DEMO_FEATURES_SUMMARY.md`
   - Click "Commit changes"

4. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Under "Branch", select `main`
   - Click Save
   - Your site is now live at: `https://yourusername.github.io/viber-template-management-demo/`

5. **Share Links**

   **Direct View (GitHub):**
   ```
   https://github.com/yourusername/viber-template-management-demo
   ```
   Click the HTML file → Click "Raw" button to open in browser

   **Live Demo (GitHub Pages):**
   ```
   https://yourusername.github.io/viber-template-management-demo/viber-template-management-demo.html
   ```

   **Share in README:**
   Add this to your README:
   ```markdown
   ## Live Demo
   
   [Click here to view the interactive demo](https://yourusername.github.io/viber-template-management-demo/viber-template-management-demo.html)
   ```

---

## For Developers (Command Line)

### Step 1: Initialize Git Repository

```bash
# Navigate to your project folder
cd path/to/viber-template-management-demo

# Initialize git
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: Viber template management demo"
```

### Step 2: Create GitHub Repository

1. Go to https://github.com/new
2. Name: `viber-template-management-demo`
3. Description: "Interactive mockup of Viber template management"
4. Select "Public"
5. Click "Create repository"

### Step 3: Push to GitHub

```bash
# Add remote repository
git remote add origin https://github.com/yourusername/viber-template-management-demo.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

### Step 4: Enable GitHub Pages

```bash
# GitHub Pages is enabled via Settings, but you can also use:
# Settings → Pages → Branch: main → Save
```

### Step 5: Get Your Live Link

Your demo is now live at:
```
https://yourusername.github.io/viber-template-management-demo/viber-template-management-demo.html
```

---

## Different Ways to Share

### 1. Share GitHub Repository Link
Perfect for: Code review, contribution
```
https://github.com/yourusername/viber-template-management-demo
```

### 2. Share GitHub Pages Link (BEST)
Perfect for: Live demo, stakeholders, anyone without GitHub
```
https://yourusername.github.io/viber-template-management-demo/viber-template-management-demo.html
```

### 3. Share Raw HTML Link
Perfect for: Direct file download
```
https://raw.githubusercontent.com/yourusername/viber-template-management-demo/main/viber-template-management-demo.html
```
Right-click → Save as HTML file

### 4. Generate Release/Download
Perfect for: Versioned releases

```bash
git tag -a v1.0 -m "Version 1.0"
git push origin v1.0
```

Then go to GitHub → Releases → Create Release from tag

### 5. Embed in Documentation
Perfect for: Internal wikis, documentation sites

```html
<iframe 
  src="https://yourusername.github.io/viber-template-management-demo/viber-template-management-demo.html"
  width="100%"
  height="800"
  frameborder="0"
></iframe>
```

### 6. Share via Gist (Quick Share)
Perfect for: Quick one-file sharing, no setup

1. Go to https://gist.github.com
2. Paste HTML code
3. Name it: `viber-template-management-demo.html`
4. Click "Create public gist"
5. Share the link: `https://gist.github.com/yourusername/...`

---

## How Others View It

### Scenario 1: You Share GitHub Pages Link
```
User clicks link → Opens live demo in browser → Can interact with all features
```

### Scenario 2: You Share Repository Link
```
User visits GitHub → Sees code → Can fork/clone → Can download HTML → Open locally
```

### Scenario 3: You Share Raw HTML Link
```
User right-clicks "Save as" → Saves to computer → Opens locally in browser
```

### Scenario 4: You Share as Release
```
User goes to Releases → Downloads .zip → Extracts → Opens HTML → Works offline
```

### Scenario 5: You Embed in Docs
```
Embedded on your site/wiki → Opens in iframe → Can interact without leaving page
```

---

## Example: Complete GitHub Repo Structure

```
viber-template-management-demo/
├── viber-template-management-demo.html    # Main demo (standalone, fully functional)
├── README.md                               # How to use & share
├── DEMO_FEATURES_SUMMARY.md               # Detailed feature list
├── LICENSE                                 # MIT License (optional)
└── .gitignore                              # (optional)
```

.gitignore content (optional):
```
.DS_Store
*.log
node_modules/
```

---

## GitHub README Template

Add this to your GitHub README.md:

```markdown
# Viber Template Management - Interactive Demo

An interactive HTML mockup of a Viber template management interface for CPaaS platforms.

## Features

- Template list with search and filters
- Create new templates with validation
- View template details including Viber API Template ID
- Viber ID account management
- Live message preview with compliance checking

## Quick Start

### View Live Demo
[Click here to open the interactive demo](https://yourusername.github.io/viber-template-management-demo/viber-template-management-demo.html)

### Download & Open Locally
1. Download `viber-template-management-demo.html`
2. Double-click to open in browser (or right-click → Open with → Browser)
3. No installation required!

### Clone Repository
```bash
git clone https://github.com/yourusername/viber-template-management-demo.git
cd viber-template-management-demo
```

## Sample Data

12 pre-loaded templates with different statuses:
- 6 Approved (green)
- 2 Pending (amber)
- 3 Declined (red)

Languages: English, French, Arabic
Categories: OTP, Transactional

## Viber API Integration

This demo showcases:
- Template ID (UUID format)
- Status lifecycle (Pending → Approved/Declined)
- OTP template validation
- Variable detection ({{placeholder}} syntax)
- Viber ID management

## Technology

- Pure HTML5, CSS3, JavaScript
- No frameworks or build tools
- Standalone file (works offline after first load)

## License

MIT License - Free to use and modify

---

For detailed features, see [DEMO_FEATURES_SUMMARY.md](DEMO_FEATURES_SUMMARY.md)
```

---

## Troubleshooting

### "GitHub Pages not working"
- Wait 5-10 minutes after enabling
- Check Settings → Pages shows green checkmark
- URL format must be: `https://yourusername.github.io/repository-name/file.html`

### "Want to update the demo"
```bash
git add .
git commit -m "Update: Added new feature"
git push origin main
# GitHub Pages auto-updates within minutes
```

### "Want to delete and start over"
1. Go to repository Settings
2. Scroll down to "Danger Zone"
3. Click "Delete this repository"
4. Type repository name to confirm

---

## Quick Command Reference

```bash
# Initial setup
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/repo-name.git
git branch -M main
git push -u origin main

# Future updates
git add .
git commit -m "Update message"
git push origin main

# Create release version
git tag -a v1.0 -m "Version 1.0 release"
git push origin v1.0
```

---

## Best Practices

1. **Always include README.md** - Explains what people are looking at
2. **Keep HTML standalone** - No dependencies, works anywhere
3. **Use GitHub Pages** - Best for sharing with non-technical users
4. **Add descriptive commit messages** - Helps track changes
5. **Create releases** - For versioned iterations

---

Need help? Check:
- GitHub Docs: https://docs.github.com
- GitHub Pages Guide: https://pages.github.com
- This demo's README.md file
