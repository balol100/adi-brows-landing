# CLAUDE.md - AI Assistant Guide for adi-brows-landing

## Project Overview

This is a **static landing page** for "Adi Buganim" - a professional eyebrow designer/stylist business based in Israel. The website serves as a simple marketing page to attract clients and provide contact information.

**Business Name:** Adi Buganim (עדי בוגנים)
**Service:** Professional Eyebrow Design (עיצוב גבות מקצועי)
**Contact:** 050-2129735

## Repository Structure

```
adi-brows-landing/
├── index.html      # Main landing page (single-page site)
├── README.md       # Project readme
└── CLAUDE.md       # This file - AI assistant guide
```

## Tech Stack

- **Pure HTML5/CSS3** - No build tools, frameworks, or JavaScript dependencies
- **Single-file architecture** - All styles embedded in `<style>` tags within `index.html`
- **Static hosting ready** - Can be deployed to any static hosting service (GitHub Pages, Netlify, etc.)

## Key Technical Details

### Language & Direction
- **Primary language:** Hebrew (he)
- **Text direction:** Right-to-left (RTL) - set via `dir="rtl"` on `<html>` element
- Phone numbers use `direction: ltr` to display correctly

### Design System
- **Primary brand color:** Gold/Goldenrod (`#d4af37`)
- **Secondary color:** Dark brown (`#2c1810`)
- **Background:** Light beige gradients (`#f5f0e8`, `#fdf8f3`)
- **Typography:** 'Segoe UI' system font stack; 'Brush Script MT' for logo
- **Border radius:** 20px for cards, 50px for buttons

### Page Sections (in order)
1. **Hero** - Logo with animated eyebrow graphics, business name, phone CTA
2. **Services** - Three service cards (design, coloring, structure improvement)
3. **About** - Brief bio of the professional
4. **CTA** - Call-to-action with phone and WhatsApp buttons
5. **Footer** - Business info and copyright

### Contact Integration
- **Phone:** Click-to-call via `tel:+972502129735`
- **WhatsApp:** Direct message link via `wa.me` with pre-filled Hebrew text

## Development Guidelines

### Making Changes

1. **Edit `index.html` directly** - No build process required
2. **Test locally** - Open the file in a browser
3. **Preserve RTL layout** - Ensure any new content works with right-to-left direction
4. **Maintain brand colors** - Use the established gold/brown palette

### CSS Organization

All styles are in a single `<style>` block (lines 7-330). Sections are organized by:
- Reset/base styles
- Hero section (`.hero`, `.logo-container`, `.eyebrows`)
- Typography (`h1`, `.subtitle`, `.section-title`)
- Buttons (`.phone-number`, `.cta-button`, `.whatsapp-button`)
- Service cards (`.service-card`)
- Section backgrounds (`.services`, `.about`, `.cta-section`)
- Responsive styles (`@media (max-width: 768px)`)

### Responsive Design

- Mobile breakpoint: 768px
- Adjustments include: font sizes, button sizes, eyebrow graphic dimensions
- Contact buttons stack vertically on mobile

## Common Tasks

### Update Phone Number
Replace all instances of `050-2129735` and `+972502129735`:
- Line 344: Hero phone link
- Line 384: CTA phone link
- Line 385: WhatsApp link (number in URL)
- Line 391: Footer text

### Update WhatsApp Message
Edit the URL-encoded Hebrew text in line 385:
```
https://wa.me/972502129735?text=YOUR_ENCODED_MESSAGE
```

### Add New Service
Add a new `.service-card` div inside `.services-grid` following the existing pattern:
```html
<div class="service-card">
    <div class="service-icon">EMOJI</div>
    <h3>Service Name</h3>
    <p>Service description</p>
</div>
```

### Change Brand Colors
Search and replace these values:
- Gold: `#d4af37`
- Light gold: `#f4d03f`
- Dark brown: `#2c1810`
- Beige backgrounds: `#f5f0e8`, `#fdf8f3`

## Deployment

This is a static site. To deploy:
1. Push to a GitHub repository
2. Enable GitHub Pages in repository settings, or
3. Deploy to any static hosting (Netlify, Vercel, Cloudflare Pages)

No environment variables or build configuration needed.

## Testing Checklist

- [ ] Phone links work (`tel:` protocol)
- [ ] WhatsApp link opens with correct message
- [ ] Site displays correctly in RTL
- [ ] Animations work smoothly
- [ ] Mobile responsive layout looks good
- [ ] All Hebrew text renders properly

## Notes for AI Assistants

- This is a production business website - changes affect a real business
- Always preserve Hebrew content and RTL layout
- Keep the design elegant and professional
- Phone number is real - do not change without explicit request
- WhatsApp message should remain in Hebrew unless requested otherwise
