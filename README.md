# Whittleville Website

A mobile-first, responsive static website for Whittleville craftsmanship services, designed for GitHub Pages hosting.

## Features

- Mobile-first responsive design
- Custom CSS (no framework dependencies)
- Smooth mobile navigation menu
- Portfolio showcase
- Services detail pages
- Contact form
- Clean, accessible HTML structure

## Required Images

To complete the website, add the following images to the `images/` directory:

### Home Page
- `outdoor-furniture.jpg` - Services section image (recommended size: 1200x800px)
- `joey-atwell.jpg` - About section image (recommended size: 800x1000px)

### Portfolio Page
- `portfolio-1.jpg` through `portfolio-6.jpg` - Portfolio project images (recommended size: 800x600px each)

### Image Guidelines
- Use high-quality images (at least 1200px wide for hero/main images)
- Optimize images for web (aim for under 500KB each)
- Use JPG format for photos
- Consider using a service like [TinyJPG](https://tinyjpg.com/) to compress images

## Local Development

1. Clone or download this repository
2. Add your images to the `images/` directory
3. Open `index.html` in a web browser
4. Or use a local server:
   ```bash
   # Using Node.js
   npx serve
   ```

## Deploying to GitHub Pages

1. Create a new repository on GitHub
2. Push your code to the repository:
   ```bash
   cd whittleville-website
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git push -u origin main
   ```

3. Enable GitHub Pages:
   - Go to your repository settings
   - Navigate to "Pages" in the sidebar
   - Under "Source", select "main" branch
   - Click "Save"
   - Your site will be available at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

## Customization

### Colors
Edit CSS variables in `css/styles.css` at `:root`:
```css
--olive-green: #4a4f2c;
--tan-gold: #d4a574;
--rust-orange: #b8593f;
--cream: #f5f0e8;
```

### Content
- Edit text directly in the HTML files
- Replace placeholder text with your actual content
- Update contact information in `contact.html`

### Typography
The site uses "Courier Prime" for headings (loaded from Google Fonts) and system fonts for body text.

## Form Submission & Spam Protection

### Built-in Spam Protection

The contact form includes a **honeypot field** to catch basic spam bots:
- Hidden field that humans won't see but bots will fill out
- JavaScript validation automatically rejects submissions with honeypot filled
- No false positives for legitimate users
- Zero configuration required

### Making the Form Functional

The contact form currently uses JavaScript to prevent default submission and shows an alert. To make it functional:

#### Option 1: Formspree (Recommended)

1. Sign up for free at [formspree.io](https://formspree.io)
2. Create a new form and get your unique endpoint URL
3. Update `contact.html` line 48:
   ```html
   <!-- Change this: -->
   <form action="#" method="POST" id="contactForm">

   <!-- To this: -->
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" id="contactForm">
   ```
4. Formspree Free tier: 50 submissions/month
5. Formspree Gold ($10/mo): Adds reCAPTCHA for advanced spam protection

#### Option 2: Netlify Forms

If hosting on Netlify instead of GitHub Pages:
- Add `netlify` attribute to the form tag
- Netlify automatically handles submissions with built-in spam filtering
- Deploy to Netlify

#### Option 3: Custom Backend

- Set up your own server endpoint
- Update the form action URL
- Implement your own spam protection

### Additional Spam Protection

If spam becomes an issue, consider adding:
- **reCAPTCHA v3** - Invisible, scores users in background
- **Rate limiting** - Prevent rapid-fire submissions
- **Email validation** - Verify email format and domain
- **Form service spam filtering** - Upgrade to Formspree Gold or use Netlify Forms

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Structure

```
whittleville-website/
├── css/
│   └── styles.css          # All styles
├── js/
│   └── main.js             # Mobile menu & form handling
├── images/                 # Your images go here
├── index.html              # Home page
├── portfolio.html          # Portfolio page
├── services.html           # Services page
├── about.html              # About page
├── contact.html            # Contact page
└── README.md               # This file
```

## License

This is a custom website template. Feel free to modify and use as needed.
