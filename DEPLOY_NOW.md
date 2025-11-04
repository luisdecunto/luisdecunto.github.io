# 🚀 Deploy Your Portfolio in 10 Commands

Copy and paste these commands one by one to deploy your portfolio to GitHub Pages.

## Prerequisites Check

Make sure you have:
- [ ] GitHub account created
- [ ] Git installed on your computer
- [ ] Added at minimum: profile picture (profile_pic.jpg)

---

## Step 1: Open Terminal/Command Prompt

```bash
# Navigate to your portfolio folder
cd C:\Users\luisd\Documents\Projects\luisdecunto.github.io
```

---

## Step 2: Add Your Files

**Before deploying, add these files:**

1. **Profile picture:**
   - Copy your photo to: `assets/img/profile_pic.jpg`

2. **CV (optional but recommended):**
   - Copy your CV to: `assets/pdf/CV_DeCunto_Luis.pdf`

3. **Project images (optional):**
   - Add thumbnails to `assets/img/` folder

---

## Step 3: Create GitHub Repository

Go to GitHub.com and:
1. Click "+" → "New repository"
2. Name: `luisdecunto.github.io` (exactly this!)
3. Public repository
4. Do NOT initialize with README
5. Click "Create repository"

---

## Step 4: Deploy Commands

**Copy and paste these commands one at a time:**

```bash
# 1. Check current location
pwd

# 2. Check git status
git status

# 3. Add all files
git add .

# 4. Create first commit
git commit -m "Initial commit: Portfolio website with projects and blog"

# 5. Add your GitHub repository as remote
git remote add origin https://github.com/luisdecunto/luisdecunto.github.io.git

# 6. Verify remote was added
git remote -v

# 7. Push to GitHub (you'll be asked for credentials)
git push -u origin main
```

---

## Step 5: GitHub Authentication

When prompted for credentials:

**Username:** `luisdecunto`

**Password:** You need a **Personal Access Token** (not your GitHub password)

### Creating a Personal Access Token:

1. Go to: [github.com/settings/tokens](https://github.com/settings/tokens)
2. Click "Generate new token" → "Generate new token (classic)"
3. Give it a name: "Portfolio deployment"
4. Select scopes: ✅ `repo` (full control)
5. Click "Generate token"
6. **COPY THE TOKEN** (you'll only see it once!)
7. Use this token as your password when pushing

**Save this token somewhere safe!**

---

## Step 6: Enable GitHub Pages

1. Go to your repository: `github.com/luisdecunto/luisdecunto.github.io`
2. Click "Settings" (top menu)
3. Click "Pages" (left sidebar)
4. Under "Source":
   - Branch: **main**
   - Folder: **/ (root)**
5. Click "Save"
6. Wait 2-5 minutes for deployment

---

## Step 7: Check Deployment Status

1. Go to "Actions" tab in your repository
2. You'll see a workflow running (orange dot)
3. Wait until it turns green (checkmark)
4. This means deployment succeeded!

---

## Step 8: Visit Your Live Site! 🎉

Open your browser and go to:
```
https://luisdecunto.github.io
```

**Congratulations! Your portfolio is live!** 🎊

---

## Troubleshooting

### Push Failed - Authentication Error
**Solution:** Use Personal Access Token instead of password
- Create token at: [github.com/settings/tokens](https://github.com/settings/tokens)

### Site Not Loading - 404 Error
**Check:**
- Repository name is exactly: `luisdecunto.github.io`
- GitHub Pages is enabled in Settings → Pages
- Wait 5-10 minutes (DNS propagation)

### Build Failed in Actions
**Check:**
- Look at error message in Actions tab
- Usually a typo in .md files
- Fix the error, commit, push again

### Images Not Showing
**Check:**
- File paths are correct: `assets/img/filename.jpg`
- Images are actually in the folder
- File names match exactly (case-sensitive!)

---

## Making Updates Later

Every time you want to update your site:

```bash
# 1. Make your changes to files

# 2. Stage changes
git add .

# 3. Commit with descriptive message
git commit -m "Added new project images"

# 4. Push to GitHub
git push

# 5. Wait 1-2 minutes, refresh your site!
```

---

## Next Steps After Deployment

1. **Share your portfolio:**
   - Update LinkedIn profile
   - Add to email signature
   - Share on social media

2. **Add missing content:**
   - More project images
   - Additional blog posts
   - Publications (if any)

3. **Monitor and improve:**
   - Get feedback from friends/colleagues
   - Add Google Analytics (optional)
   - Write regular blog posts

4. **Customize further:**
   - Adjust colors in `_config.yml`
   - Add more projects as you complete them
   - Create interactive demos

---

## Quick Reference Commands

```bash
# Check status
git status

# Add all changes
git add .

# Commit changes
git commit -m "Your message here"

# Push to GitHub (updates live site)
git push

# View remote URL
git remote -v

# Test locally before pushing
bundle exec jekyll serve
# Then visit: http://localhost:4000
```

---

## Important Notes

⚠️ **Don't edit files directly on GitHub**
- Always edit locally, then push
- This prevents conflicts and errors

⚠️ **Keep your token safe**
- Treat it like a password
- Don't share it publicly
- Don't commit it to your repository

⚠️ **Site updates take 1-2 minutes**
- Changes aren't instant
- Wait for Actions to complete
- Hard refresh browser (Ctrl+F5)

---

## Success Checklist

After deployment:
- [ ] Site loads at `https://luisdecunto.github.io`
- [ ] About page shows your info
- [ ] Projects page displays all 4 projects
- [ ] Blog shows sample post
- [ ] Profile picture displays (if added)
- [ ] Navigation works correctly
- [ ] Site looks good on mobile (test on phone)

---

## You're All Set! 🎉

Your portfolio is now live and accessible to:
- Potential employers
- Recruiters
- Collaborators
- Anyone searching for your work

**What's next?**
1. Share your portfolio link everywhere
2. Add content regularly (blog posts, projects)
3. Keep learning and building (your ML roadmap!)
4. Update your portfolio as you grow

---

**Need help?** Check:
- [README.md](README.md) - Full documentation
- [QUICKSTART.md](QUICKSTART.md) - Step-by-step guide
- [TODO_ADD_THESE_FILES.md](TODO_ADD_THESE_FILES.md) - Content checklist

**Ready to deploy?** Let's do this! 💪
