# 📋 Files You Need to Add

Before deploying, add these files to make your portfolio complete:

## 🖼️ Priority 1: Images (Critical for Visual Appeal)

### Your Profile Picture
```
📁 assets/img/
   └── profile_pic.jpg          ← Add your professional headshot
                                   Recommended: 400x400px, < 200KB
```

**Where to get it:**
- LinkedIn profile photo
- Professional headshot
- Crop and resize to square format

---

### Project Thumbnails
```
📁 assets/img/
   ├── kurvedwind_thumb.jpg     ← KurvedWind project image
   ├── kirigami_thumb.jpg       ← Kirigami project image
   ├── xfem_thumb.jpg           ← XFEM project image
   └── thin_shells_thumb.jpg    ← Thin shells project image
                                   Recommended: 600x400px each
```

**Ideas for project images:**
- Screenshots of simulation results
- Graphs showing performance improvements
- Methodology diagrams
- Photos of experimental setups
- Code snippets (as images)
- Before/after comparisons

**Tip:** If you don't have images yet, use:
- Placeholder service: [placeholder.com](https://placeholder.com/)
- Free stock photos: [unsplash.com](https://unsplash.com/) (search "engineering", "simulation", "data")
- Create simple diagrams with [draw.io](https://draw.io)

---

## 📄 Priority 2: Your CV

```
📁 assets/pdf/
   └── CV_DeCunto_Luis.pdf      ← Your current CV
```

**Action:** Copy your CV PDF to this folder
- This will enable the CV download link
- Keep filename: `CV_DeCunto_Luis.pdf` (or update _pages/cv.md)

---

## 🎨 Optional: Additional Project Images

For each project, you can add detailed images:

```
📁 assets/img/
   # KurvedWind images
   ├── kurvedwind_simulation.jpg
   ├── kurvedwind_results.jpg
   ├── kurvedwind_ml_comparison.jpg

   # Kirigami images
   ├── kirigami_pattern.jpg
   ├── kirigami_deformation.jpg
   ├── kirigami_results.jpg

   # XFEM images
   ├── xfem_mesh.jpg
   ├── xfem_crack_propagation.jpg
   ├── xfem_pressure_field.jpg

   # Thin shells images
   ├── thin_shells_stress.jpg
   ├── thin_shells_curvature.jpg
   └── thin_shells_geometry.jpg
```

**How to use:** Uncomment the image sections in each project .md file

---

## 📊 Optional: Additional Content

### Publications (if you have any)
```
📁 _bibliography/
   └── papers.bib               ← BibTeX file with your publications
```

### News/Announcements
```
📁 _news/
   ├── announcement_1.md
   └── announcement_2.md
```

### Additional Blog Posts
```
📁 _posts/
   ├── 2024-01-15-from-engineering-to-ml.md  ← Already created
   ├── 2024-02-01-your-next-post.md          ← Add more as you write
   └── 2024-03-01-another-post.md
```

---

## ✅ Quick Checklist Before Deployment

- [ ] **Profile picture added** (profile_pic.jpg)
- [ ] **At least 2-3 project thumbnails** (can add placeholders temporarily)
- [ ] **CV PDF uploaded** (CV_DeCunto_Luis.pdf)
- [ ] **Reviewed all content** in _pages/about.md
- [ ] **Updated _config.yml** with correct contact info
- [ ] **Tested locally** with `bundle exec jekyll serve`

---

## 🎯 Minimum Viable Portfolio

**You can deploy with just these:**
1. ✅ Profile picture (profile_pic.jpg)
2. ✅ CV PDF (CV_DeCunto_Luis.pdf)
3. ✅ 1-2 project thumbnails

**Everything else can be added later!** The beauty of GitHub Pages is that you can update anytime by:
```bash
git add .
git commit -m "Added new images"
git push
```

---

## 📸 Creating Project Images - Quick Guide

### Option 1: Screenshots of Your Work
- Open your simulation software
- Take high-quality screenshots (use Snipping Tool on Windows)
- Crop to remove unnecessary UI
- Resize to 600x400 or 800x600

### Option 2: Create Simple Graphics
1. Go to [Canva](https://canva.com) (free)
2. Create 600x400 canvas
3. Add your project title + key visual
4. Use professional colors (blues, grays)
5. Export as JPG

### Option 3: Use Matplotlib/Python
```python
import matplotlib.pyplot as plt
import numpy as np

# Create a simple visualization
fig, ax = plt.subplots(figsize=(8, 6))
# ... your plotting code ...
plt.savefig('project_thumb.jpg', dpi=150, bbox_inches='tight')
```

### Option 4: Temporary Placeholders
Use [placeholder.com](https://placeholder.com/):
- `https://via.placeholder.com/600x400?text=KurvedWind+Project`
- Just update image URLs in project files

---

## 🚀 What Happens if You Don't Add Images?

**Good news:** The site will still work!
- Profile section will show placeholder
- Projects will display without thumbnails
- Everything else functions normally

**But:** Adding images makes your portfolio **much more visually appealing** and professional.

---

## 💡 Pro Tip

**Start minimal, iterate quickly:**
1. Deploy with just profile pic + CV
2. Add project images over the next week
3. Write blog posts monthly
4. Update as you complete new projects

Don't let perfectionism prevent you from launching!

---

## 📞 Need Help Creating Images?

If you need help:
1. Send me your simulation screenshots
2. I can help create professional thumbnails
3. Or use the placeholder approach initially

**Remember:** Content > Images > Perfection

Launch first, polish later! 🚀
