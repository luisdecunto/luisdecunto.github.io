# Luis De Cunto - Personal Portfolio Website

Welcome to the repository for my personal website and portfolio! This site showcases my work in **mechanical engineering**, **computational modeling**, and **machine learning**.

🌐 **Live Site:** [luisdecunto.github.io](https://luisdecunto.github.io)

## About

I'm a Mechanical Engineer with a Master's degree from Aarhus University, specializing in:
- Finite Element Modeling (FEM) and Computational Fluid Dynamics (CFD)
- Machine Learning and Surrogate Modeling
- Mathematical Modeling and Numerical Methods
- Scientific Computing (Python, MATLAB)

This portfolio highlights my research projects, engineering work, and technical blog posts.

## Technology Stack

This website is built with:
- **[Jekyll](https://jekyllrb.com/)** - Static site generator
- **[al-folio](https://github.com/alshedivat/al-folio)** - Beautiful academic theme
- **GitHub Pages** - Free hosting
- **Markdown** - Content writing

## Features

- 📱 **Responsive design** - Works beautifully on mobile and desktop
- 🌓 **Dark/light mode** - Toggle based on user preference
- 📊 **Project showcase** - Detailed case studies with images
- 📝 **Blog** - Technical articles on ML, simulations, and engineering
- 🔍 **Search** - Full-text search across the site
- 🎨 **Modern UI** - Clean, professional design

## Local Development Setup

### Prerequisites

1. **Install Ruby** (version 2.7 or higher)
   - Windows: [RubyInstaller](https://rubyinstaller.org/)
   - macOS: `brew install ruby`
   - Linux: `sudo apt-get install ruby-full`

2. **Install Bundler**
   ```bash
   gem install bundler
   ```

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/luisdecunto/luisdecunto.github.io.git
   cd luisdecunto.github.io
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Run local server**
   ```bash
   bundle exec jekyll serve
   ```

4. **View the site**
   - Open your browser to `http://localhost:4000`
   - The site will auto-reload when you make changes

### Common Issues

**Issue: `bundle install` fails**
- Solution: Update bundler with `gem update bundler`
- On Windows, you may need: `gem install eventmachine --platform ruby`

**Issue: Jekyll won't start**
- Solution: Try `bundle exec jekyll serve --trace` to see detailed errors

**Issue: Port 4000 already in use**
- Solution: Use a different port: `bundle exec jekyll serve --port 4001`

## Deployment to GitHub Pages

### First-Time Setup

1. **Create GitHub repository**
   - Repository name MUST be: `yourusername.github.io`
   - For me: `luisdecunto.github.io`

2. **Push your code**
   ```bash
   git add .
   git commit -m "Initial commit: Portfolio website"
   git remote add origin https://github.com/luisdecunto/luisdecunto.github.io.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Click Save

4. **Wait for deployment** (2-5 minutes)
   - Check status in Actions tab
   - Visit `https://luisdecunto.github.io`

### Updating the Site

Every time you push changes to the `main` branch, GitHub Pages automatically rebuilds and deploys:

```bash
git add .
git commit -m "Updated project descriptions"
git push
```

Wait 1-2 minutes, then refresh your site to see changes!

## Content Management

### Adding a New Project

1. Create a new file in `_projects/` folder:
   ```bash
   _projects/5_my_new_project.md
   ```

2. Add front matter and content:
   ```markdown
   ---
   layout: page
   title: My New Project
   description: Short description of the project
   img: assets/img/project_thumbnail.jpg
   importance: 5
   category: Machine Learning
   ---

   ## Project content here...
   ```

3. Add project image to `assets/img/`

4. Commit and push!

### Writing a New Blog Post

1. Create a new file in `_posts/` folder:
   ```bash
   _posts/2024-01-20-my-blog-post.md
   ```

2. Add front matter:
   ```markdown
   ---
   layout: post
   title: "My Blog Post Title"
   date: 2024-01-20
   description: Brief description for preview
   tags: machine-learning python engineering
   ---

   ## Your content here...
   ```

3. Commit and push!

### Adding Your Profile Picture

1. Add your photo to `assets/img/profile_pic.jpg`
2. Recommended size: 400x400 pixels
3. Format: JPG or PNG

### Customizing Site Settings

Edit `_config.yml` to update:
- Name and contact info
- Social media links
- Site description
- Theme colors
- Analytics settings

## Site Structure

```
luisdecunto.github.io/
├── _config.yml              # Main configuration
├── _pages/                  # Static pages (About, Projects, Blog)
│   ├── about.md
│   ├── projects.md
│   └── blog.md
├── _projects/               # Project case studies
│   ├── 1_kurvedwind.md
│   ├── 2_kirigami.md
│   ├── 3_xfem_hydraulic_fracturing.md
│   └── 4_thin_shells_thesis.md
├── _posts/                  # Blog posts
│   └── 2024-01-15-from-engineering-to-ml.md
├── assets/
│   ├── img/                 # Images for projects and blog
│   ├── json/                # JSON data files
│   └── pdf/                 # PDFs (CV, papers)
├── blog/                    # Blog setup files
├── Gemfile                  # Ruby dependencies
├── index.html               # Homepage
└── README.md                # This file
```

## Adding Custom Domain (Optional)

If you want to use your own domain (e.g., `luisdecunto.com`):

1. **Buy a domain** from Namecheap, Google Domains, or Cloudflare

2. **Configure DNS** (at your domain registrar):
   - Add 4 A records pointing to GitHub Pages:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - Add CNAME record: `www` → `luisdecunto.github.io`

3. **Update GitHub Pages settings**:
   - Go to Settings → Pages
   - Custom domain: Enter `luisdecunto.com`
   - Check "Enforce HTTPS"

4. **Update _config.yml**:
   ```yaml
   url: https://luisdecunto.com
   ```

5. **Wait for DNS propagation** (can take up to 24 hours)

## Maintenance Tips

### Keep Dependencies Updated

```bash
bundle update
```

### Check for Broken Links

Use [html-proofer](https://github.com/gjtorikian/html-proofer):
```bash
gem install html-proofer
bundle exec jekyll build
htmlproofer ./_site
```

### Optimize Images

Before adding images, compress them:
- Use [TinyPNG](https://tinypng.com/) or [Squoosh](https://squoosh.app/)
- Keep images under 500KB for fast loading

## Resources & Credits

- **Theme:** [al-folio](https://github.com/alshedivat/al-folio) by Maruan Al-Shedivat
- **Icons:** [Font Awesome](https://fontawesome.com/)
- **Hosting:** [GitHub Pages](https://pages.github.com/)
- **Jekyll Documentation:** [jekyllrb.com/docs](https://jekyllrb.com/docs/)

## Contact

- **Email:** luisdcnt@gmail.com
- **LinkedIn:** [linkedin.com/in/luisdecunto](https://linkedin.com/in/luisdecunto)
- **GitHub:** [github.com/luisdecunto](https://github.com/luisdecunto)

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

Feel free to use this repository as a template for your own portfolio!

---

**Last Updated:** January 2024
