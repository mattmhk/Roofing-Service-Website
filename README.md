# Belfast Roofing Services Website

A modern, responsive website for roofing services in Belfast, Northern Ireland. Built as a static site optimized for Render's free tier hosting.

## Features

- 🏠 Professional, modern design
- 📱 Fully responsive (mobile, tablet, desktop)
- 🖼️ Image gallery showcasing work
- 📝 Contact/quote form
- ⚡ Fast loading and optimized
- 🚀 Ready for Render deployment

## Project Structure

```
├── index.html      # Main HTML file
├── styles.css      # All styling
├── script.js       # JavaScript functionality
├── render.yaml     # Render deployment configuration
└── README.md       # This file
```

## Deployment to Render

### Option 1: Using Render Dashboard (Recommended)

1. **Create a Render Account**
   - Go to [render.com](https://render.com) and sign up for a free account

2. **Create a New Static Site**
   - Click "New +" → "Static Site"
   - Connect your Git repository (GitHub, GitLab, or Bitbucket)
   - Or upload the files directly

3. **Configure the Site**
   - **Name**: belfast-roofing-website (or your preferred name)
   - **Build Command**: Leave empty (no build needed)
   - **Publish Directory**: Leave empty (root directory)
   - Click "Create Static Site"

4. **Your site will be live!**
   - Render will provide a URL like: `https://belfast-roofing-website.onrender.com`

### Option 2: Using Render CLI

```bash
# Install Render CLI (if not already installed)
npm install -g render-cli

# Login to Render
render login

# Deploy from the project directory
render deploy
```

### Option 3: Using render.yaml

The `render.yaml` file is included for automatic configuration. When you connect your repository to Render, it will automatically detect and use this configuration.

## Customization

### Images

The website currently uses placeholder images from Unsplash. To add your own images:

1. Replace the image URLs in `index.html`:
   - Hero section background image
   - Gallery images (6 images)
   - About section image

2. **Option A**: Host images externally (recommended for Render free tier)
   - Upload to a free service like Imgur, Cloudinary, or similar
   - Replace URLs in the HTML

3. **Option B**: Use a CDN or image hosting service

### Contact Form Setup

**Currently:** The form uses a mailto fallback (opens user's email client). This works but isn't ideal.

**Recommended:** Set up Formspree (free tier - 50 submissions/month) to receive form submissions directly to your email:

1. **Sign up for Formspree** (free):
   - Go to [formspree.io](https://formspree.io)
   - Click "Sign Up" and create a free account
   - Verify your email address

2. **Create a new form**:
   - Click "New Form" in your dashboard
   - Give it a name (e.g., "Belfast Roofing Quotes")
   - Copy your form ID (looks like: `xrgkqyzw` or `mknvjqpd`)

3. **Update the website**:
   - Open `script.js`
   - Find the line: `const FORMSPREE_ID = 'YOUR_FORMSPREE_ID';`
   - Replace `YOUR_FORMSPREE_ID` with your actual Formspree form ID
   - Save the file

4. **Configure email notifications**:
   - In Formspree dashboard, go to Settings → Email Notifications
   - Add your email address where you want to receive submissions
   - Save settings

**That's it!** Now when someone fills out the form, you'll receive an email with all their details.

**Alternative options:**
- **EmailJS** (free tier): [emailjs.com](https://www.emailjs.com)
- **Getform** (free tier): [getform.io](https://getform.io)
- **Web3Forms** (free): [web3forms.com](https://web3forms.com)

### Contact Information

Update the contact information in `index.html`:
- Phone number
- Email address
- Business hours
- Physical address (if applicable)

### Colors and Branding

Customize colors in `styles.css` by modifying the CSS variables at the top:

```css
:root {
    --primary-color: #c41e3a;      /* Main brand color */
    --primary-dark: #9a1629;       /* Darker shade */
    --secondary-color: #2c3e50;    /* Secondary color */
    /* ... */
}
```

## Local Development

To view the website locally:

1. Simply open `index.html` in your web browser
2. Or use a local server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Notes

- This is a static website, so no server-side processing is required
- No database or disk storage needed - perfect for Render's free tier
- All images are loaded from external sources (Unsplash) to avoid storage requirements
- The form can be enhanced with third-party services as mentioned above

## License

This project is open source and available for use.

## Support

For questions or issues, please contact the development team.
