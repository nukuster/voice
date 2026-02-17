# Voice & Ukulele Teaching Website

A clean, professional website for Eddie Adams Voice - voice and ukulele lessons in the SF Bay Area.

## Features

- ✅ Fully responsive (mobile, tablet, desktop)
- ✅ Clean, modern design with mint green accent color
- ✅ Fast-loading static site (no dependencies)
- ✅ SEO-optimized
- ✅ Contact form integration ready
- ✅ Easy to maintain and update

## Pages

1. **Home** - Hero section, services overview, what makes you different
2. **About** - Your story and background
3. **Services** - Detailed service descriptions with pricing
4. **Approach** - Your teaching philosophy and methodology
5. **Contact** - Contact form and booking information

## Setup Instructions

### 1. Set Up Contact Form

The contact form uses Formspree (free tier allows 50 submissions/month).

1. Go to [formspree.io](https://formspree.io)
2. Sign up for a free account
3. Create a new form
4. Copy your form endpoint (looks like: `https://formspree.io/f/YOUR_FORM_ID`)
5. In `contact.html`, replace `YOUR_FORM_ID` on line 38:
   ```html
   <form action="https://formspree.io/f/YOUR_ACTUAL_FORM_ID" method="POST" class="contact-form">
   ```

**Alternative:** If you want to use Netlify Forms instead:
1. Change the form tag to:
   ```html
   <form name="contact" method="POST" data-netlify="true" class="contact-form">
   ```
2. Add a hidden input:
   ```html
   <input type="hidden" name="form-name" value="contact">
   ```

### 2. Add Your Photos (Optional)

Create an `images` folder and add:
- `headshot.jpg` - Your professional photo
- `teaching.jpg` - Photo of you teaching (if available)

Then update the About page to include your photo by adding this to `about.html` in the about-intro section:

```html
<div class="about-photo">
    <img src="images/headshot.jpg" alt="Eddie Adams">
</div>
```

### 3. Deploy to GitHub Pages

#### Option A: Using an existing repo (nukuster.github.io)

1. Copy all files to your local git repository
2. Commit and push:
   ```bash
   git add .
   git commit -m "Add voice teaching website"
   git push origin main
   ```
3. Your site will be live at `https://nukuster.github.io`

#### Option B: Using a custom subdomain

1. Create a new repository called `voice` (or any name you want)
2. Push your files to that repo
3. Go to Settings > Pages
4. Select your branch (usually `main`)
5. Your site will be at `https://nukuster.github.io/voice`

#### Option C: Custom domain

If you want a custom domain (like `eddieteaches.com`):
1. Buy a domain from Namecheap, Google Domains, etc.
2. In your GitHub repo, go to Settings > Pages
3. Enter your custom domain
4. Update your domain's DNS settings (instructions will be provided by GitHub)

### 4. Customize Content

All content is in plain HTML - easy to edit:

#### Update pricing:
Edit `services.html` - search for the pricing sections

#### Change colors:
Edit `css/styles.css` - change the CSS variables at the top:
```css
:root {
    --color-primary: #9CCC65;  /* Change this to your preferred accent color */
    /* ... */
}
```

#### Add/remove pages:
Just duplicate any `.html` file and update the navigation in all pages

## File Structure

```
vocal-teaching-site/
├── index.html          # Homepage
├── about.html          # About page
├── services.html       # Services & pricing
├── approach.html       # Teaching philosophy
├── contact.html        # Contact form
├── css/
│   └── styles.css      # All styles
├── js/
│   └── main.js         # Mobile nav & interactions
├── images/             # Your photos (create this)
└── README.md           # This file
```

## Maintenance

### To update prices:
1. Open `services.html`
2. Find the pricing sections
3. Update the numbers
4. Commit and push

### To add a blog:
1. Create a `blog` folder
2. Create `blog/index.html` with a list of posts
3. Add individual post pages
4. Add "Blog" to the navigation

### To change copy/text:
Just edit the HTML files directly - all text is right there in the markup.

## Browser Support

Works in all modern browsers:
- Chrome, Firefox, Safari, Edge (latest versions)
- Mobile Safari, Chrome Mobile
- IE11 (with minor degradation)

## Performance

- No external dependencies (except fonts from system)
- Minimal CSS/JS
- Fast load times (<1 second on good connection)
- Optimized for Core Web Vitals

## SEO

- Semantic HTML
- Meta descriptions on all pages
- Proper heading hierarchy
- Alt text ready (add when you upload images)
- Mobile-friendly (Google ranking factor)

## Need Help?

If you need to make changes and get stuck:
1. HTML files = content and structure
2. CSS file = colors, fonts, layout
3. JS file = mobile menu (rarely needs changes)

## License

All rights reserved - Eddie Adams 2025

---

## Quick Start Checklist

- [ ] Set up Formspree account and update contact form
- [ ] Add your photos to `/images` folder
- [ ] Update any content you want to change
- [ ] Push to GitHub
- [ ] Enable GitHub Pages in repo settings
- [ ] Test the contact form
- [ ] Share your site!

Your site will be live at: `https://nukuster.github.io`
