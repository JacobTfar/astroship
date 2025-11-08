# Assets Checklist for jfcontracting.biz

## Required Images

### Logo

- **Filename:** `images/logo.png`
- **Specs:** PNG with transparent background, ~200x200px
- **Alt text:** "JF Contracting logo"
- **Where used:** Header on all pages

### Project Photos (3 required)

#### 1. Kitchen Remodel

- **Filename:** `images/kitchen-before-after.jpg`
- **Specs:** JPEG, 1200x800px, 60-75% quality
- **Alt text:** "Kitchen remodel before and after, Madison NJ"
- **Suggested content:** Side-by-side or before/after of a kitchen renovation
- **Where used:** Homepage projects section

#### 2. Exterior Renovation

- **Filename:** `images/exterior.jpg`
- **Specs:** JPEG, 1200x800px, 60-75% quality
- **Alt text:** "Home exterior renovation in Mendham NJ"
- **Suggested content:** Exterior siding, trim, or full home renovation
- **Where used:** Homepage projects section

#### 3. Commercial Project

- **Filename:** `images/salad-house.jpg`
- **Specs:** JPEG, 1200x800px, 60-75% quality
- **Alt text:** "Commercial renovation at Salad House, Newark"
- **Suggested content:** Interior or exterior of Salad House or other commercial client
- **Where used:** Homepage projects section

### Favicon

- **Filename:** `favicon.ico`
- **Specs:** 32x32px ICO format (or PNG named favicon.png)
- **Tool:** <https://favicon.io/favicon-converter/>
- **Where used:** Browser tab icon (all pages)

---

## Image Optimization Tips

1. **Resize before upload:**
   - Desktop: Use Photoshop, GIMP, or Preview (Mac)
   - Online: <https://squoosh.app> or <https://tinypng.com>

2. **File size targets:**
   - Logo: < 50 KB
   - Project photos: < 200 KB each
   - Favicon: < 10 KB

3. **Format recommendations:**
   - Logo: PNG (transparency)
   - Photos: JPEG (smaller file size) or WebP (best compression)

4. **Naming conventions:**
   - Use lowercase
   - Use hyphens, not spaces
   - Be descriptive (good SEO)

---

## Optional Additional Images

### Future Gallery Page

- Create `images/gallery/` folder
- Add more project photos with naming pattern:

  - `kitchen-madison-1.jpg`
  - `bathroom-maplewood-2.jpg`
  - `exterior-mendham-3.jpg`
  - `commercial-salad-house-4.jpg`

### Team/About Photo

- **Filename:** `images/team.jpg`
- **Where to use:** Add to About page
- **Alt text:** "JF Contracting team"

---

## Text Content to Customize

### Required Updates (see README.md)

- [ ] Phone number (all pages)
- [ ] Email address (all pages)
- [ ] Business address (index.html JSON-LD)
- [ ] Operating hours (contact.html)

### Optional Enhancements

- [ ] Add real client testimonials with permission
- [ ] Add specific town names for completed projects
- [ ] Add years of experience to About page
- [ ] Add license/certification numbers if required by NJ

---

## SEO Meta Tags (Already Included)

Each page has:

- Title tag (unique per page)
- Meta description (unique per page)
- Alt text on all images
- JSON-LD LocalBusiness schema (homepage)

**Keywords naturally included:**

- home renovation Madison NJ
- Maplewood contractor
- Mendham remodeling
- Morris County contractor
- Essex County home improvement

---

## Form Configuration

### Current Setup: Netlify Forms

- Form in `contact.html` uses Netlify Forms
- Will work automatically when deployed to Netlify
- Spam protection via honeypot field

### Alternative: Formspree

If not using Netlify:

1. Sign up at <https://formspree.io>
2. Get form endpoint (e.g., `https://formspree.io/f/abc123xyz`)
3. Replace form tag in `contact.html`:
   
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   

---

## DNS Settings (For Custom Domain)

### Netlify DNS Settings

Point your domain `jfcontracting.biz` to Netlify:

**At your domain registrar (GoDaddy, Namecheap, etc.):**

- `A` record: `@` → `75.2.60.5`
- `CNAME` record: `www` → `YOUR-SITE.netlify.app`

Wait 24-48 hours for DNS propagation.

### Alternative: Cloudflare (Free CDN + SSL)

1. Sign up at Cloudflare
2. Add site: jfcontracting.biz
3. Update nameservers at registrar (Cloudflare will provide)
4. Point DNS to your hosting

---

## Testing Checklist

Before going live:

- [ ] All images load correctly
- [ ] Logo displays in header
- [ ] Favicon appears in browser tab
- [ ] Phone links work on mobile (tap to call)
- [ ] Email links open mail client
- [ ] Contact form submits successfully
- [ ] All navigation links work
- [ ] Footer links work
- [ ] Site looks good on mobile (test on phone)
- [ ] Site looks good on desktop
- [ ] Page load time under 3 seconds

---

## Quick Deployment Command (if using Netlify CLI)

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login
netlify login

# Deploy from jfcontracting folder
cd jfcontracting
netlify deploy --prod
```

---

## Support Resources

- **Image optimization:** <https://squoosh.app>
- **Favicon generator:** <https://favicon.io>
- **Netlify docs:** <https://docs.netlify.com>
- **Formspree docs:** <https://help.formspree.io>
- **Google Business Profile:** <https://www.google.com/business>

---

Last updated: November 2025
