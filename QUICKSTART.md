# JF Contracting - Astro Site Quick Reference

## 🚀 Essential Commands

```powershell
npm install          # Install dependencies (first time only)
npm run dev          # Start dev server → http://localhost:4321
npm run build        # Build for production → dist/ folder
npm run preview      # Preview production build locally
```

## 📝 Before Going Live

1. **Update contact info** in `src/layouts/Layout.astro` (lines 9-11)
2. **Add images** to `public/images/`:
   - `logo.png`
   - `perch-maplewood.jpg`
3. **Test locally**: `npm run dev` and check all pages
4. **Build**: `npm run build` (creates `dist/` folder)

## 🌐 Deploy to Netlify

### Quick Deploy

```powershell
npm run build
```

Then drag `dist/` folder to <https://app.netlify.com>


### Or use Netlify CLI

```powershell
npm install -g netlify-cli
netlify login
netlify init
netlify deploy --prod --dir=dist
```

Form submissions will appear in Netlify dashboard automatically.

## 🎨 Common Edits

### Change phone/email globally

Edit `src/layouts/Layout.astro` lines 9-11

### Add a new service

Edit `src/pages/services.astro`, add:

```astro
<ServiceDetail 
  title="Service Name"
  items={["Feature 1", "Feature 2"]}
>
  <p>Description...</p>
</ServiceDetail>
```

### Change colors

Edit `src/styles/global.css` `:root` variables

## 📦 Project Structure

```text
src/
├── layouts/Layout.astro    # Header/footer/nav
├── components/             # Reusable components
├── pages/                  # Auto-generates routes
└── styles/global.css       # Global styles

public/
└── images/                 # Static images (add yours here)
```

## 📚 Full Docs

See `README-ASTRO.md` for complete documentation.

---

**Current Status:** ✅ Build successful, ready to deploy  
**Framework:** Astro 4.16.1  
**Old HTML files:** Backed up in `_old-html/` folder
