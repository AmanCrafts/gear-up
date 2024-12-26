# 🌟 Welcome to Our Amazing Project! 🌟

## 🎯 Contributor Guidelines and Project Structure

Hello, awesome contributor! 🎉 We're super excited to have you join our community of creators. This guide will help you understand our project structure and contribution process. Let's make something incredible together! 💫

## 🚀 Quick Start Guide

### 1. Setting Up Your Development Environment 🛠️

```bash
# Clone the repository
git clone https://github.com/<your-username>/<repo-name>.git

# Navigate to project directory
cd <repo-name>

# Set up upstream remote
git remote add upstream https://github.com/<original-owner>/<repo-name>.git

# Create and switch to your feature branch
git checkout -b feature/your-amazing-feature
```

### 2. Before You Start Coding 📝

- ✅ Pull latest changes from upstream
- ✅ Create a new branch for your feature
- ✅ Read through our coding standards below
- ✅ Plan your changes before you start

## 📂 Project Structure

```
YourProject/
├── 📄 index.html                 # Main entry point
├── 📂 css/                       # All CSS files
│   ├── styles.css               # Homepage styles
│   ├── header.css              # Global header styles
│   ├── footer.css              # Global footer styles
│   ├── about.css               # About page styles
│   └── contact.css             # Contact page styles
├── 📂 js/                        # JavaScript files
│   ├── main.js                 # Main JavaScript file
│   ├── about.js                # About page scripts
│   └── contact.js              # Contact page scripts
├── 📂 assets/                    # Media files
│   ├── 📂 images/               # Image files (.jpg or .png only and recommended-file-size: 500KB maximum!)
│   │   ├── hero_banner.png
│   │   └── about_team.jpg
│   └── 📂 videos/               # Video files (.mp4 and max-file-size: 102400 KB ie. 100MB)
│       └── intro_video.mp4
└── 📂 pages/                     # HTML pages
    ├── about.html
    └── contact.html
```

## 📏 Naming Conventions and Standards

### 🖼️ Images
- ✨ Format: `.jpg` and `.png` ONLY
- 📦 Size: Optimize all images (max 500KB recommended)
- 🏷️ Naming Pattern: `<section>_<description>.jpg`
  - ✅ Good: `hero_banner.jpg`, `team_photo.jpg`
  - ❌ Bad: `IMG001.jpg`, `hero banner.jpg`

### 📁 Folders
- 🔤 Use only lowercase letters
- 🚫 No numbers or special characters
- ✨ Must be descriptive
  - ✅ Good: `images`, `styles`, `scripts`
  - ❌ Bad: `img1`, `style2`, `misc_files`

### 📄 Files
- 🔤 Use lowercase with underscores
- 📝 Be descriptive but concise
  - ✅ Good: `about_page.css`, `contact_form.js`
  - ❌ Bad: `page1.css`, `script.js`


## 🔗 Path Linking Guidelines

### 📍 Using Relative Paths

Always use relative paths to link images, pages, and other resources. This ensures our project remains portable and works across different environments.

### ✅ Correct Way (Using Relative Paths)

From `index.html` to different resources:
```html
<!-- Linking images -->
<img src="./assets/images/logo.jpg" alt="Logo">
<img src="./assets/images/hero/banner.jpg" alt="Banner">

<!-- Linking CSS -->
<link rel="stylesheet" href="./css/styles.css">
<link rel="stylesheet" href="./css/about.css">

<!-- Linking JavaScript -->
<script src="./js/main.js"></script>

<!-- Linking pages -->
<a href="./pages/about.html">About Us</a>
```

From `pages/about.html` to different resources:
```html
<!-- Linking images -->
<img src="../assets/images/logo.jpg" alt="Logo">
<img src="../assets/images/about/team.jpg" alt="Team">

<!-- Linking CSS -->
<link rel="stylesheet" href="../css/styles.css">
<link rel="stylesheet" href="../css/about.css">

<!-- Linking JavaScript -->
<script src="../js/about.js"></script>

<!-- Linking back to home -->
<a href="../index.html">Home</a>
```

### ❌ Incorrect Way (Using Absolute Paths)

Don't use these types of paths:
```html
<!-- ❌ Absolute system paths -->
<img src="/Users/username/Desktop/project/images/logo.jpg">
<img src="C:/Projects/website/images/logo.jpg">

<!-- ❌ Absolute root paths -->
<img src="/images/logo.jpg">
<link href="/css/styles.css">

<!-- ❌ Full URLs to local files -->
<img src="https://github.com/username/repo/images/logo.jpg">
```

### 🗺️ Path Navigation Guide

- `./` means current directory
- `../` means up one directory
- `../../` means up two directories

### 📁 Examples Based on File Location

Let's say you're linking resources from different files:

```plaintext
YourProject/
├── index.html
├── css/
│   └── styles.css
├── assets/
│   └── images/
│       └── logo.jpg
└── pages/
    └── about/
        └── team.html
```

From `index.html` to `logo.jpg`:
```html
✅ <img src="./assets/images/logo.jpg">
❌ <img src="/Users/me/project/assets/images/logo.jpg">
```

From `pages/about/team.html` to `logo.jpg`:
```html
✅ <img src="../../assets/images/logo.jpg">
❌ <img src="/assets/images/logo.jpg">
```

### 💡 Tips for Path Linking

1. **Use CLI to Verify Paths**
   ```bash
   # From project root, verify file exists
   ls ./assets/images/logo.jpg
   
   # Check relative path from a specific directory
   cd pages/about && ls ../../assets/images/logo.jpg
   ```

2. **Test Local Navigation**
   - Always test your links locally before committing
   - Use Live Server in VS Code to catch path issues
   - Verify paths work when project is moved to different locations

3. **Path Troubleshooting**
   - If image doesn't load, right-click and "Open image in new tab" to debug path
   - Check browser console for 404 errors
   - Verify file extensions match exactly (case-sensitive)

[Rest of the previous content remains the same]

## 🎨 CSS Guidelines

### Structure
```css
/* Example of CSS organization */
/* 1. Global Styles */
/* 2. Layout & Grid */
/* 3. Components */
/* 4. Page-specific styles */
/* 5. Keyframes */
/* 6. media queries */
```

## 💻 JavaScript Guidelines

- 🎯 Use meaningful variable names
- 📝 Comment your code
- ✨ Follow DRY (Don't Repeat Yourself) principles

## 🔄 Contribution Workflow

1. 🌿 Create a new branch:
```bash
git checkout -b feature/your-feature-name
```

2. 💾 Make your changes and commit:
```bash
git add .
git commit -m "✨ Add: Brief description of your changes"
```

3. 🔄 Keep your branch updated:
```bash
git fetch upstream
git rebase upstream/main
```

4. 🚀 Push your changes:
```bash
git push origin feature/your-feature-name
```

## ✅ Pull Request Checklist

Before submitting your PR, ensure:
- [ ] Code follows our naming conventions
- [ ] Images are optimized and properly named
- [ ] No unnecessary files are included
- [ ] Code is properly commented
- [ ] All links are working
- [ ] No console errors

## 🤝 Code Review Process

1. 👀 Submit your PR
2. 🔍 Wait for code review
3. 📝 Address any feedback
4. ✨ Get approved and merged!

Remember: Every contribution matters! 🌟 Whether it's fixing a typo or adding a feature, you're helping make this project better! 

Happy Coding! 🚀