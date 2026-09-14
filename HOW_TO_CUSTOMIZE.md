# How to Customize Your Personal Website

This guide will help you customize your personal website based on the al-folio theme.

## 📋 Quick Start Checklist

Follow these steps in order:

### 1. Basic Information (_config.yml)

Open `_config.yml` and modify these sections (search for "CHANGE THIS"):

```yaml
# Your name
first_name: Your_First_Name
last_name: Your_Last_Name

# Your email
email: your.email@example.com

# Your GitHub Pages URL
url: https://your-github-username.github.io
```

### 2. Social Media Links (_config.yml)

Scroll down to the "Social integration" section and fill in your accounts:

```yaml
github_username: your-github-username
linkedin_username: your-linkedin-username
scholar_userid: your-google-scholar-id
x_username: your-twitter-username
```

Leave empty the ones you don't use.

### 3. Profile Photo

**Location:** `assets/img/`

**Steps:**
1. Put your photo in the `assets/img/` folder
2. Rename it to something simple like `prof_pic.jpg`
3. Update `_pages/about.md`:
   ```yaml
   profile:
     image: prof_pic.jpg  # Use your filename here
   ```

### 4. Homepage Content (_pages/about.md)

**Location:** `_pages/about.md`

**What to change:**
- Replace the placeholder text with your own introduction
- Update your title/position in the `more_info` section
- Write your bio in the main content area (between the `---` markers and the button)
- Optionally: Add more details in the expandable section

**Example:**
```markdown
---
layout: about
title: About
permalink: /
subtitle: 

profile:
  align: right
  image: prof_pic.jpg
  image_circular: true
  more_info: >
    <p style="font-size: 16px; font-family: Roboto, sans-serif;">PhD Student @ University Name</p>
    <p style="font-size: 16px; font-family: Roboto, sans-serif;">email [at] university [dot] edu</p>

news: true
selected_papers: true
social: true
---

I am a PhD student at [University Name](https://example.com), working on artificial intelligence and machine learning.

My research focuses on...
```

## 📁 File Structure Overview

```
my-personal-website/
├── _config.yml              # Main configuration (name, email, social links)
├── _pages/                  # Website pages
│   ├── about.md            # Homepage (your main introduction)
│   ├── cv.md               # CV page
│   └── publications.md     # Publications page
├── _news/                   # News items (add .md files here)
├── _projects/               # Project pages (add .md files here)
├── _bibliography/           # Your publications
│   └── papers.bib          # BibTeX file for publications
├── assets/
│   └── img/                # PUT YOUR PHOTOS HERE
└── _data/
    └── talks.yml           # Your talks/presentations
```

## 📝 Adding Content

### Add News Items

Create a new file in `_news/` folder, e.g., `announcement_1.md`:

```markdown
---
layout: post
date: 2024-09-13
inline: true
---

Your news announcement here. You got accepted to a conference! 🎉
```

### Add Projects

Create a new file in `_projects/` folder, e.g., `project_1.md`:

```markdown
---
layout: page
title: Project Name
description: Brief description of your project
img: assets/img/project_thumbnail.jpg
importance: 1
category: work
---

Detailed description of your project.

You can add images:
{% include figure.liquid path="assets/img/project_detail.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
```

### Add Publications

Edit `_bibliography/papers.bib` and add your papers in BibTeX format:

```bibtex
@article{yourname2024,
  title={Your Paper Title},
  author={Your Name and Coauthor Name},
  journal={Conference/Journal Name},
  year={2024},
  selected={true}  // This will feature it on your homepage
}
```

### Add Talks

Edit `_data/talks.yml`:

```yaml
- title: Talk Title
  event: Conference Name
  date: 2024-09-13
  location: City, Country
  url: https://link-to-slides.com
```

## 🎨 Customization Tips

### Change Profile Image Shape

In `_pages/about.md`:
```yaml
image_circular: false  # Square image
image_circular: true   # Circular image
```

### Disable Sections

In `_pages/about.md`:
```yaml
news: false              # Hide news section
talks: false             # Hide talks section
selected_papers: false   # Hide selected papers
social: false            # Hide social icons
```

### Change Color Theme

The theme has built-in light/dark mode. Users can toggle it with the button on the website.

## 🚀 Publishing to GitHub

### Step 1: Create GitHub Repository

1. Go to GitHub and create a new repository
2. Name it: `your-username.github.io` (replace with your actual GitHub username)
3. Make it public

### Step 2: Upload Your Website

In the `my-personal-website` folder, run these commands:

```bash
git init
git add .
git commit -m "Initial commit: My personal website"
git branch -M main
git remote add origin https://github.com/your-username/your-username.github.io.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" → "Pages"
3. Under "Source", select "Deploy from a branch"
4. Select branch: `main`, folder: `/ (root)`
5. Click "Save"

Wait 2-5 minutes, then visit: `https://your-username.github.io`

## 🔧 Local Testing (Optional)

To preview your website locally before publishing:

### Install Dependencies

```bash
# Install Ruby (if not installed)
# On Windows: Download from https://rubyinstaller.org/

# Install Jekyll
gem install jekyll bundler

# Install project dependencies
bundle install
```

### Run Local Server

```bash
bundle exec jekyll serve
```

Then open your browser and go to: `http://localhost:4000`

## ❗ Common Issues

### Issue: Profile image not showing
- **Solution:** Make sure the image file is in `assets/img/` and the filename in `about.md` matches exactly (including file extension)

### Issue: Social icons not appearing
- **Solution:** Check that you filled in the username in `_config.yml` correctly (no spaces, no @ symbol)

### Issue: Publications not showing
- **Solution:** Make sure your BibTeX file (`_bibliography/papers.bib`) is properly formatted

### Issue: Website not updating on GitHub
- **Solution:** 
  1. Check the "Actions" tab in your GitHub repository for build errors
  2. Wait 5-10 minutes after pushing changes
  3. Try force refresh in your browser (Ctrl+F5)

## 📚 Additional Resources

- [al-folio documentation](https://github.com/alshedivat/al-folio)
- [Jekyll documentation](https://jekyllrb.com/docs/)
- [GitHub Pages documentation](https://docs.github.com/en/pages)
- [Markdown guide](https://www.markdownguide.org/)

## 💡 Tips

1. **Start simple:** Get the basic information working first, then add more content
2. **Test locally:** If possible, test your website locally before pushing to GitHub
3. **Regular commits:** Commit your changes frequently with descriptive messages
4. **Check examples:** Look at other al-folio websites for inspiration
5. **Keep backups:** Keep a copy of your original content before making major changes

---

Good luck with your website! 🎉
