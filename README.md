# Interactive Demos Gallery

A clean, professional demo gallery hosted on GitHub Pages. Add interactive demos and showcase them in one beautiful landing page.

## 📂 Project Structure

```
.
├── index.html          # Main landing page (gallery)
├── demos.json          # List of all demos
├── demos/              # Individual demo HTML files
│   ├── chart-demo.html
│   ├── form-demo.html
│   └── animation-demo.html
└── README.md
```

## 🚀 Setup on GitHub Pages

### Option 1: Using GitHub Pages with your GitHub account

1. **Create a new repository** on GitHub named `username.github.io` (replace `username` with your GitHub username)
2. **Push this code** to the repository:
   ```bash
   git remote add origin https://github.com/username/username.github.io.git
   git branch -M main
   git push -u origin main
   ```
3. Your gallery will be live at: `https://username.github.io`

### Option 2: Using a different repo name

1. **Create any repository** on GitHub
2. **Go to Settings > Pages > Source** and select "main" branch
3. **Push this code** to your repository
4. Your gallery will be live at: `https://username.github.io/repo-name`

## 📝 Adding New Demos

### Step 1: Create your HTML demo
Create a new file in the `demos/` folder. Example: `demos/my-feature.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Feature Demo</title>
    <style>
        /* Your CSS here */
    </style>
</head>
<body>
    <h1>My Interactive Demo</h1>
    <!-- Your content here -->
    <a href="../">← Back to Demos</a>
</body>
</html>
```

**Pro tip**: Always include `<a href="../">← Back to Demos</a>` so users can return to the gallery.

### Step 2: Add it to demos.json

Open `demos.json` and add your demo to the array:

```json
{
  "title": "Your Demo Title",
  "description": "A short description of what this demo shows",
  "url": "demos/my-feature.html",
  "tags": ["Tag1", "Tag2"]
}
```

**Fields explained**:
- `title`: Name shown on the card
- `description`: Brief explanation (1-2 sentences)
- `url`: Path to your HTML file
- `tags`: Array of category tags (optional but recommended)

### Step 3: Commit and push

```bash
git add demos.json demos/my-feature.html
git commit -m "Add my feature demo"
git push
```

Your demo appears on the gallery within seconds!

## 🎨 Customizing the Gallery

### Change the header
Edit `index.html`:
```html
<h1>Your Company Name - Demos</h1>
<p>Your tagline here</p>
```

### Change colors
Edit the gradient in `index.html` CSS:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

Replace with your brand colors (hex codes or rgb).

### Change the grid layout
Modify in `index.html`:
```css
grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
/* Change 300px to adjust card width, adjust 1fr for different layouts */
```

## 📱 Mobile & Responsive

The gallery is fully responsive and works on all devices. Test by opening `index.html` in a browser and resizing the window.

## 🔧 Local Testing

Before pushing to GitHub:

1. Open `index.html` in your browser locally
2. The gallery should load and show all demos from `demos.json`
3. Click each demo to verify it works
4. Check on mobile by opening browser dev tools (F12) → toggle device toolbar

## ⚡ Tips

- **Keep demos lightweight**: Large files slow down loading
- **Test the back link**: Each demo should link back to `../` 
- **Use descriptive tags**: Help visitors find what they're looking for
- **Keep descriptions short**: 1-2 sentences max
- **Use meaningful titles**: Make it clear what each demo does

## 🐛 Troubleshooting

**"Error loading demos"** → Make sure `demos.json` is in the root directory (same folder as `index.html`)

**Demos not showing** → Check that the `url` path in `demos.json` matches your actual file path

**Back link broken** → Make sure each demo has `<a href="../">← Back to Demos</a>`

---

Happy demoing! 🎉
