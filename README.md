# Portfolio Theme

A high-performance, mobile-first Hugo template for personal portfolios and blogs, based on [Hugo Profile](https://github.com/gurusabarish/hugo-profile). This theme is perfect for developers, designers, and professionals looking to showcase their work, experience, and projects.

![GitHub forks](https://img.shields.io/github/forks/anky209e/portfolio?style=plastic)
![GitHub stars](https://img.shields.io/github/stars/anky209e/portfolio?style=plastic)
![Netlify Status](https://api.netlify.com/api/v1/badges/0a76b59f-67be-47da-bd3b-c8c26214e967/deploy-status)
![License](https://img.shields.io/github/license/anky209e/portfolio)

## 🚀 Demo

[Live Demo](https://anky209e.netlify.app) - See the theme in action with a real portfolio site.

## ✨ Features

- **🎨 Responsive Design**: Mobile-first approach that looks great on all devices
- **🌙 Dark Mode**: Built-in theme toggle with customizable color schemes
- **⚡ High Performance**: Optimized for fast loading and Core Web Vitals
- **📝 Blog Support**: Integrated blog with RSS feeds and JSON output
- **🏆 Portfolio Sections**: About, Experience, Education, Projects, Achievements
- **🔍 Search Functionality**: Built-in search for content discovery
- **📊 Analytics Ready**: Support for Google Analytics and other tracking
- **🖼️ Gallery**: Photo gallery with image viewer
- **📱 Social Integration**: Easy social media linking and sharing
- **🧩 Modular Components**: Easily enable/disable sections via configuration
- **🔧 SEO Optimized**: Meta tags, structured data, and sitemap generation
- **📧 Contact Forms**: Formspree integration or custom contact handling

## 🛠️ Tech Stack

- **Static Site Generator**: Hugo (v0.68.0+)
- **CSS Framework**: Bootstrap 5
- **Icons**: Font Awesome 6
- **Image Viewer**: Viewer.js
- **Deployment**: Netlify ready (with Docker support)

## 📦 Installation

1. Clone this repository:
```bash
git clone https://github.com/anky209e/portfolio.git
cd portfolio
```

2. Run the development server:
```bash
hugo server
```

3. Open `http://localhost:1313` in your browser

## ⚙️ Configuration

The theme is highly customizable through the `hugo.yaml` file. Key configuration sections include:

### Basic Setup
```yaml
params:
  title: "Your Name"
  description: "Your professional description"
  favicon: "/fav.png"
```

### Navigation
```yaml
params:
  navbar:
    brandName: "Your Name"
    disableSearch: false
    menus:
      disableAbout: false
      disableExperience: false
      # ... other sections
```

### Hero Section
```yaml
params:
  hero:
    enable: true
    intro: "Hi, my name is"
    title: "Your Name"
    subtitle: "Your professional tagline"
    content: "Brief description about yourself"
    image: /images/me.png
```

## 📁 Project Structure

```
portfolio/
├── layouts/                 # Hugo templates
│   ├── _default/           # Default layouts
│   ├── partials/           # Reusable components
│   └── shortcodes/         # Custom shortcodes
├── static/                 # Static assets
│   ├── css/               # Stylesheets
│   ├── js/                # JavaScript files
│   └── images/            # Images and media
├── exampleSite/           # Demo site configuration
│   ├── content/           # Site content
│   ├── static/            # Site-specific static files
│   └── hugo.yaml          # Configuration file
└── theme.toml            # Theme metadata
```

## 🎨 Customization

### Colors
Customize colors in your configuration:

```yaml
params:
  color:
    textColor: "#343a40"
    primaryColor: "#007bff"
    backgroundColor: "#eaedf0"
    darkmode:
      textColor: "#e4e6eb"
      backgroundColor: "#18191a"
```

### Fonts
Adjust typography settings:

```yaml
params:
  font:
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.5
    textAlign: left
```

### Sections
Enable/disable sections as needed:

```yaml
params:
  navbar:
    menus:
      disableAbout: false      # About section
      disableProjects: true     # Projects section
      disableBlog: false        # Blog section
```

## 📝 Content Management

### Adding Blog Posts
Create markdown files in `content/blogs/`:

```yaml
---
title: "Your Blog Post Title"
date: 2024-01-01
tags: ["tag1", "tag2"]
featuredImage: "/images/blog-post.jpg"
---
Your blog content here...
```

### Adding Projects
Configure projects in `hugo.yaml`:

```yaml
params:
  projects:
    items:
      - title: "Project Name"
        content: "Project description"
        image: "/images/projects/project.png"
        badges: ["React", "Node.js", "MongoDB"]
        links:
          - icon: fab fa-github
            url: https://github.com/username/repo
```

## 🚀 Deployment

### Netlify
1. Connect your repository to Netlify
2. Set build command: `cd exampleSite && hugo --gc --minify --themesDir ../..`
3. Set publish directory: `exampleSite/public`
4. Deploy!

### GitHub Pages
1. Configure GitHub Actions with this workflow:

```yaml
name: Deploy
on:
  push:
    branches: [ main ]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
      - name: Build
        run: cd exampleSite && hugo --gc --minify --themesDir ../..
      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./exampleSite/public
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This theme is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Based on [Hugo Profile](https://github.com/gurusabarish/hugo-profile) by Gurusabarish
- Built with [Hugo](https://gohugo.io/) static site generator
- Styled with [Bootstrap 5](https://getbootstrap.com/)
- Icons by [Font Awesome](https://fontawesome.com/)

## 📞 Support

If you have any questions or need help with the theme, please:
- Open an issue on GitHub
- Check the [demo site](https://anky209e.netlify.app) for examples
- Review the example site configuration in `exampleSite/hugo.yaml`

