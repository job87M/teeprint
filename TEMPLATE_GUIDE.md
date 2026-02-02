# Adding Your Custom Template Images

## Quick Guide

Your website now has a **Graphic Template** dropdown in the design form. Users can select from pre-made designs that display on the t-shirt preview along with their text.

## How to Add Your Template Images

### Option 1: Using Image URLs (Recommended for GitHub Pages)

1. **Upload your transparent PNG files** to your GitHub repository in an `images` folder:
   ```
   /images/skull-design.png
   /images/mountain-scene.png
   /images/logo.png
   ```

2. **Update the `templateDesigns` array** in `index.html` (around line 503):

   ```javascript
   const templateDesigns = [
     { 
       id: 'none', 
       name: 'No Template', 
       url: '' 
     },
     { 
       id: 'skull', 
       name: 'Skull Design', 
       url: './images/skull-design.png'  // Your image path
     },
     { 
       id: 'mountain', 
       name: 'Mountain Scene', 
       url: './images/mountain-scene.png'
     },
     { 
       id: 'logo', 
       name: 'Company Logo', 
       url: './images/logo.png'
     },
     // Add more templates here...
   ];
   ```

### Option 2: Using External URLs

If your images are hosted elsewhere (like Imgur, Cloudinary, or your own CDN):

```javascript
const templateDesigns = [
  { 
    id: 'none', 
    name: 'No Template', 
    url: '' 
  },
  { 
    id: 'design1', 
    name: 'Cool Design', 
    url: 'https://your-domain.com/designs/cool-design.png'
  },
  { 
    id: 'design2', 
    name: 'Awesome Logo', 
    url: 'https://i.imgur.com/yourimage.png'
  },
];
```

### Option 3: Using Base64 Embedded Images (For Small Files)

For very small PNG files, you can embed them directly:

1. Convert your PNG to base64: https://www.base64-image.de/
2. Add to the array:

```javascript
{ 
  id: 'small-icon', 
  name: 'Small Icon', 
  url: 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgA...'
}
```

## Image Requirements

✅ **Best Practices:**
- **Format**: PNG with transparent background
- **Size**: 500-1000px width (for good quality)
- **File Size**: Keep under 500KB for fast loading
- **Color**: White or light colors work best on dark shirts, dark colors on light shirts

⚠️ **Important Notes:**
- Make sure images have **transparent backgrounds** (not white)
- Test on both light and dark shirt colors
- Optimize images before uploading (use TinyPNG.com or similar)

## Current Placeholders

The website currently has **placeholder SVG graphics** as examples:
- Skull Design
- Mountain Scene
- Floral Pattern
- Geometric Shapes
- Coffee Cup
- Wave Pattern
- Star Burst

**Replace these with your actual design images!**

## File Structure for GitHub Pages

```
your-repo/
├── index.html
├── README.md
└── images/
    ├── design1.png
    ├── design2.png
    ├── logo.png
    └── skull.png
```

## Testing Your Templates

1. Open `index.html` in your browser
2. Click the **Graphic Template** dropdown
3. Select each template to verify it displays correctly
4. Test on different shirt colors
5. Adjust text positioning if needed

## Customizing Template Display

### Adjust Image Size

Find this CSS (around line 578):

```css
.design-image {
  max-width: 80%;        /* Make larger/smaller */
  max-height: 250px;     /* Adjust max height */
  object-fit: contain;
}
```

### Change Layout (Image Above/Below Text)

The current layout shows: **Image → Text → Subtitle**

To change the order, modify the preview section (around line 823):

```jsx
<div className="design-content">
  {/* Image first (current) */}
  {selectedTemplate !== 'none' && (
    <img src={...} className="design-image" />
  )}
  
  {/* Then text */}
  <div className="design-text">...</div>
  <div className="design-subtext">...</div>
</div>
```

## Need Help?

Common issues:
- **Image not showing**: Check file path is correct
- **Image too large**: Resize to max 1000px width
- **Poor quality**: Use higher resolution PNG
- **Wrong colors**: Ensure transparent background

---

**Pro Tip**: Create a matching gallery item for each template so users can see examples!