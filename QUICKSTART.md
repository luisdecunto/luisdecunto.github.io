# Quick Start Guide - Portfolio Website

## 🚀 Get Your Portfolio Live in 15 Minutes!

Follow these steps to deploy your portfolio website to GitHub Pages.

### Step 1: Install Ruby (5 minutes)

**Windows:**
1. Download [RubyInstaller](https://rubyinstaller.org/downloads/)
2. Install Ruby+Devkit (version 3.2.x recommended)
3. In the final step, run `ridk install` and select option 3

**macOS:**
```bash
brew install ruby
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt-get install ruby-full build-essential
```

**Verify installation:**
```bash
ruby -v
# Should show: ruby 3.x.x
```

### Step 2: Install Bundler

```bash
gem install bundler
```

### Step 3: Install Jekyll Dependencies

Navigate to your portfolio folder and install:

```bash
cd C:\Users\luisd\Documents\Projects\luisdecunto.github.io
bundle install
```

**Note:** This might take 5-10 minutes the first time.

### Step 4: Test Locally (Optional but Recommended)

```bash
bundle exec jekyll serve
```

Then open your browser to: `http://localhost:4000`

**You should see your portfolio!** 🎉

Press `Ctrl+C` to stop the server.

### Step 5: Create GitHub Repository

1. Go to [github.com](https://github.com)
2. Click "New repository" (green button)
3. **Important:** Name it exactly: `luisdecunto.github.io`
4. Keep it **Public**
5. **Do NOT** initialize with README (we already have one)
6. Click "Create repository"

### Step 6: Push Your Code to GitHub

```bash
cd C:\Users\luisd\Documents\Projects\luisdecunto.github.io

# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: My portfolio website"

# Connect to GitHub (replace with YOUR repository URL)
git remote add origin https://github.com/luisdecunto/luisdecunto.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Authenticate with GitHub:**
- If prompted, use your GitHub username and a [Personal Access Token](https://github.com/settings/tokens) (not password)

### Step 7: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (gear icon)
3. Scroll down to **Pages** (left sidebar)
4. Under "Source":
   - Branch: **main**
   - Folder: **/ (root)**
5. Click **Save**

### Step 8: Wait for Deployment

1. Go to the **Actions** tab in your repository
2. You'll see a workflow running (orange dot)
3. Wait until it turns green (checkmark) - usually 2-5 minutes

### Step 9: Visit Your Live Site! 🎉

Open your browser and go to:
```
https://luisdecunto.github.io
```

**Congratulations!** Your portfolio is now live on the internet!

---

## 📝 Making Changes

Every time you want to update your site:

```bash
# Make your edits to files
# Then:

git add .
git commit -m "Describe your changes here"
git push
```

GitHub will automatically rebuild and deploy in 1-2 minutes!

---

## 🎨 Customization Checklist

### Immediate To-Dos:

- [ ] **Add your profile picture**
  - Save as: `assets/img/profile_pic.jpg`
  - Recommended size: 400x400 pixels

- [ ] **Update _config.yml**
  - Check all personal information
  - Update social media links
  - Verify email address

- [ ] **Add project images**
  - For each project, add a thumbnail in `assets/img/`
  - Name format: `project_name_thumb.jpg`

- [ ] **Write more blog posts**
  - Create files in `_posts/` folder
  - Format: `YYYY-MM-DD-post-title.md`

- [ ] **Add your CV**
  - Save as: `assets/pdf/CV_DeCunto_Luis.pdf`
  - Link from About page

### Optional Enhancements:

- [ ] Add Google Analytics
- [ ] Enable site search
- [ ] Add publication list
- [ ] Create a custom 404 page
- [ ] Set up custom domain

---

## 🆘 Troubleshooting

### Site not loading?
1. Check Actions tab for build errors
2. Verify repository name is exactly `luisdecunto.github.io`
3. Wait 5 minutes and try again (DNS propagation)

### Changes not showing up?
1. Did you `git push`?
2. Check Actions tab - build successful?
3. Hard refresh browser (Ctrl+F5)
4. Clear browser cache

### Local server won't start?
```bash
# Try this:
bundle update
bundle exec jekyll serve --trace
```

### Need help?
- Check the [README.md](README.md) for detailed documentation
- Jekyll docs: [jekyllrb.com/docs](https://jekyllrb.com/docs/)
- al-folio theme: [github.com/alshedivat/al-folio](https://github.com/alshedivat/al-folio)

---

## 🎓 Next Steps

1. **Populate with content**
   - Add more projects from your CV
   - Write blog posts about your journey
   - Add images and visualizations

2. **Share your portfolio**
   - Add link to your LinkedIn profile
   - Include in your email signature
   - Share with potential employers

3. **Keep it updated**
   - Add projects as you complete them
   - Write regular blog posts (aim for 1/month)
   - Update skills and experience

4. **Monitor traffic** (optional)
   - Add Google Analytics
   - See which projects get the most views
   - Understand your audience

---

**Ready to make your portfolio shine?** Start customizing! 🚀
