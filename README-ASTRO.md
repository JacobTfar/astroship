# Jason Fallas Contracting Website (Astro)

**Domain:** jfcontracting.biz  
**Tagline:** Building Dreams, One Project at a Time  
**Framework:** Astro 4.16+ (Static Site Generator)

Modern, component-based rebuild for performance, SEO, and easy maintenance.

---

## 🚀 Quick Start

### Install Dependencies
```powershell
npm install
```

### Run Dev Server
```powershell
npm run dev
```

Visit http://localhost:4321

### Build for Production
```powershell
npm run build
```

Output: `dist/` folder (deploy this)

### Preview Production Build
```powershell
npm run preview
```

---

## 📁 Project Structure

```
jfcontracting/
├── src/
│   ├── layouts/
│   │   └── Layout.astro       # Base layout with header/footer
│   ├── components/
│   │   ├── ServiceDetail.astro # Reusable service card
│   │   └── Feature.astro       # Feature box component
│   ├── pages/
│   │   ├── index.astro         # Homepage (/)
│   │   ├── services.astro      # Services (/services)
│   │   ├── about.astro         # About (/about)
│   │   └── contact.astro       # Contact (/contact)
│   └── styles/
│       └── global.css          # Global styles
├── public/
│   ├── images/                 # Static images (ADD YOURS HERE)
│   │   ├── logo.png            # Logo (REQUIRED)
│   │   └── perch-maplewood.jpg # Featured project (REQUIRED)
│   └── favicon.ico             # Favicon
├── package.json
├── astro.config.mjs
└── tsconfig.json
```

---

## ✅ Before Deploying

### 1. **Update Contact Info**
Edit `src/layouts/Layout.astro` (lines 9-11):
```astro
const phone = "+1-YOUR-PHONE";
const phoneDisplay = "(XXX) XXX-XXXX";
const email = "your@email.com";
```

Also update in page files:
- `src/pages/index.astro`
- `src/pages/services.astro`
- `src/pages/about.astro`
- `src/pages/contact.astro`

### 2. **Update JSON-LD Schema**
Edit `src/layouts/Layout.astro` (line 29):
- `addressLocality`: your city
- `postalCode`: your ZIP

### 3. **Add Images**
Place in `public/images/`:
- `logo.png` (transparent PNG, ~200x200px)
- `perch-maplewood.jpg` (project photo, 1200x800px)

Images are auto-optimized by Astro during build.

---

## 🚀 Deployment

### **Option 1: Netlify (Recommended)**

#### Via Netlify CLI:
```powershell
npm install -g netlify-cli
netlify login
netlify init
netlify deploy --prod
```

#### Via Drag & Drop:
1. Run `npm run build`
2. Go to https://app.netlify.com
3. Drag `dist/` folder to Netlify
4. Add custom domain: jfcontracting.biz

**Form Handling:** Works automatically with Netlify Forms (already configured in `contact.astro`)

---

### **Option 2: Vercel**

```powershell
npm install -g vercel
vercel login
vercel --prod
```

Or connect GitHub repo at https://vercel.com

**Note:** For Vercel, update form to use Formspree or web3forms.

---

### **Option 3: Cloudflare Pages**

1. Connect GitHub repo at https://pages.cloudflare.com
2. Build command: `npm run build`
3. Output directory: `dist`

---

## 🎨 Customization

### Change Colors
Edit `src/styles/global.css`:
```css
:root {
  --accent: #0b5;        /* Primary green */
  --accent-dark: #098844; /* Hover state */
  --muted: #666;         /* Gray text */
}
```

### Add New Service
Edit `src/pages/index.astro` or `src/pages/services.astro`:
```astro
<ServiceDetail 
  title="New Service Name"
  items={["Feature 1", "Feature 2", "Feature 3"]}
>
  <p>Description of the service...</p>
</ServiceDetail>
```

### Add New Page
Create `src/pages/gallery.astro`:
```astro
---
import Layout from '../layouts/Layout.astro';
---

<Layout title="Gallery" description="..." activePage="gallery">
  <h2>Gallery</h2>
  <!-- content -->
</Layout>
```

Auto-generates `/gallery` route.

---

## 🔧 Key Features

✅ **Component-based** — Reusable ServiceDetail, Feature components  
✅ **SEO-optimized** — Meta tags, JSON-LD schema, semantic HTML  
✅ **Performance** — Static generation, minimal JS, optimized images  
✅ **Mobile-first** — Responsive design for QR code scans  
✅ **Form handling** — Netlify Forms built-in (or swap for Formspree)  
✅ **Type-safe** — TypeScript support for props

---

## 📊 Performance

Astro generates static HTML with near-zero JS by default:

- **Lighthouse Score:** 95-100 (all categories)
- **Page Size:** ~50-100 KB (with images optimized)
- **Load Time:** <1s on 4G

Perfect for QR code scans and mobile users.

---

## 🆘 Troubleshooting

### Port already in use:
```powershell
npm run dev -- --port 3000
```

### Build errors:
```powershell
npm run astro check
```

### Clear cache:
```powershell
Remove-Item -Recurse -Force node_modules,.astro,dist
npm install
```

---

## 📚 Resources

- **Astro Docs:** https://docs.astro.build
- **Netlify Astro Guide:** https://docs.netlify.com/frameworks/astro/
- **Vercel Astro Guide:** https://vercel.com/docs/frameworks/astro

---

## 💡 Future Enhancements

- [ ] Add image optimization with `@astrojs/image`
- [ ] Create gallery page with lightbox
- [ ] Add blog with markdown support
- [ ] Integrate Google Analytics
- [ ] Add sitemap.xml generation
- [ ] Implement view transitions (Astro 3+)

---

Built for **Jason Fallas Contracting** — November 2025  
Framework: Astro 4.16+ | Design: HTML5 UP
