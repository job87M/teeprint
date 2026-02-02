# Inked Studio - T-Shirt Design & Print Website

A beautiful, custom t-shirt design and preview website built with React. Features an editorial/print-shop aesthetic inspired by vintage screen printing meets contemporary web design.

## Features

- 🎨 **Live Design Preview** - See your design updates in real-time
- 🌈 **Color Customization** - Choose from curated shirt and text colors
- ✍️ **Typography Options** - Select from distinctive font styles
- 🖼️ **Design Gallery** - Browse and customize featured designs
- 📱 **Responsive Design** - Works beautifully on all devices
- 🎭 **Distinctive Aesthetic** - Warm colors, tactile feel, animated details

## Quick Start

Simply open `index.html` in your browser to start designing!

## Deploy to GitHub Pages

### Option 1: Using GitHub Web Interface

1. Create a new repository on GitHub
2. Upload `index.html` to your repository
3. Go to **Settings** → **Pages**
4. Under "Source", select **main branch** and **/ (root)**
5. Click Save
6. Your site will be live at `https://yourusername.github.io/repository-name`

### Option 2: Using Git Command Line

```bash
# Navigate to your project directory
cd /path/to/your/project

# Initialize git (if not already done)
git init

# Add the file
git add index.html README.md

# Commit
git commit -m "Initial commit - Inked Studio t-shirt designer"

# Add your GitHub repository as remote
git remote add origin https://github.com/yourusername/repository-name.git

# Push to GitHub
git branch -M main
git push -u origin main

# Enable GitHub Pages
# Go to repository Settings → Pages → Select main branch → Save
```

### Option 3: Quick Deploy Script

```bash
#!/bin/bash
# save this as deploy.sh and run: bash deploy.sh

REPO_NAME="tshirt-designer"  # Change this to your repo name
GITHUB_USERNAME="yourusername"  # Change this to your username

git init
git add .
git commit -m "Deploy Inked Studio"
git branch -M main
git remote add origin https://github.com/$GITHUB_USERNAME/$REPO_NAME.git
git push -u origin main

echo "🚀 Pushed to GitHub!"
echo "Now enable GitHub Pages in repository settings:"
echo "https://github.com/$GITHUB_USERNAME/$REPO_NAME/settings/pages"
```

## Customization

### Colors
Edit the CSS variables in the `<style>` section to match your brand:

```css
:root {
  --ink-black: #1a1a1a;
  --paper-cream: #faf8f3;
  --rust-orange: #d4682f;
  --forest-green: #2d5541;
  --clay-brown: #8b6f5c;
  --soft-blue: #7ba3b8;
  --highlight: #ffd97d;
}
```

### Fonts
The site uses Google Fonts. Current fonts are:
- **Bebas Neue** - Display headings
- **Crimson Text** - Elegant serif for subtitles
- **Work Sans** - Clean sans-serif for body text

To change fonts, update the Google Fonts link and CSS font-family properties.

### Adding More Gallery Items
Find the `exampleDesigns` array in the JavaScript and add new designs:

```javascript
const exampleDesigns = [
  { 
    text: 'YOUR TEXT', 
    sub: 'Your subtitle', 
    color: '#hexcolor', 
    textColor: '#hexcolor' 
  },
  // Add more...
];
```

## Browser Support

Works in all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Mobile browsers

## Tech Stack

- **React 18** - UI framework (CDN version)
- **HTML5** - Structure
- **CSS3** - Styling with animations
- **Vanilla JavaScript** - Interactivity

## File Structure

```
.
├── index.html          # Complete single-file application
└── README.md          # Documentation (this file)
```

## Features Roadmap

- [ ] Export design as PNG/SVG
- [ ] More design templates
- [ ] Custom image upload
- [ ] Multiple design positions (front/back)
- [ ] Size and quantity selection
- [ ] Shopping cart integration
- [ ] Print-ready file generation

## License

Free to use and modify for personal and commercial projects.

## Support

For questions or issues, please open an issue on GitHub or contact hello@inkedstudio.example

---

**Made with ❤️ for creators everywhere**