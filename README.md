# Sun Exposure - Marketing Website

A lightweight, modern marketing website for the Sun Exposure iOS app, designed for deployment on GitHub Pages.

## Features

- **Responsive Design**: Optimized for all devices (desktop, tablet, mobile)
- **Modern UI**: Clean, professional design with smooth animations
- **Fast Loading**: Minimal dependencies, pure HTML/CSS
- **SEO Friendly**: Semantic HTML and meta tags
- **Accessible**: WCAG compliant with proper heading structure

## Pages

- **Home** (`index.html`): Main marketing page with features, benefits, and download CTA
- **Privacy Policy** (`privacy-policy.html`): Comprehensive privacy policy
- **Terms of Use** (`terms-of-use.html`): Legal terms and conditions

## Deployment to GitHub Pages

### Option 1: Deploy from main branch

1. Push this repository to GitHub
2. Go to your repository Settings
3. Navigate to Pages (under Code and automation)
4. Under "Source", select "Deploy from a branch"
5. Select branch: `main` and folder: `/ (root)`
6. Click Save
7. Your site will be available at `https://[username].github.io/sunexposure-web/`

### Option 2: Deploy from gh-pages branch

1. Create a new branch called `gh-pages`:
   ```bash
   git checkout -b gh-pages
   git push origin gh-pages
   ```
2. Go to your repository Settings
3. Navigate to Pages
4. Select branch: `gh-pages` and folder: `/ (root)`
5. Click Save

### Custom Domain (Optional)

To use a custom domain like `sunexposure.app`:

1. Create a file named `CNAME` in the root directory with your domain:
   ```
   sunexposure.app
   ```
2. Configure your domain's DNS settings to point to GitHub Pages:
   - Add an A record pointing to GitHub's IP addresses
   - Or add a CNAME record pointing to `[username].github.io`
3. Enable HTTPS in GitHub Pages settings

## File Structure

```
sunexposure-web/
├── index.html           # Main homepage
├── privacy-policy.html  # Privacy policy page
├── terms-of-use.html    # Terms of use page
├── styles.css           # All CSS styles
└── README.md           # This file
```

## Customization

### Colors

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #FF9500;
    --secondary-color: #FFB84D;
    --dark-color: #1C1C1E;
    --light-color: #F5F5F7;
    --text-dark: #1D1D1F;
    --text-light: #6E6E73;
}
```

### Content

- Update app description in `index.html`
- Modify privacy policy in `privacy-policy.html`
- Adjust terms in `terms-of-use.html`
- Replace placeholder screenshots by updating the `.screenshot-placeholder` section

### Adding Real Screenshots

To add actual app screenshots, replace the placeholder mockup:

1. Export screenshots from your iPhone/iPad
2. Save them in an `images/` folder
3. Update the `.phone-screen` div in `index.html`:

```html
<div class="phone-screen">
    <img src="images/screenshot-1.png" alt="Sun Exposure App Screenshot">
</div>
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- No external dependencies
- Minimal CSS (~3KB gzipped)
- Fast initial load (<1s on 3G)
- Optimized for Core Web Vitals

## License

Copyright © 2025 Sun Exposure. All rights reserved.
