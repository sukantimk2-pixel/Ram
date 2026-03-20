[README.md](https://github.com/user-attachments/files/26148071/README.md)
# 🇮🇳 Smart Exam & Document Photo Hub

**Free · No Login · All Indian Exams**  
Resize photos and signatures for UPSC, SSC, RRB, IBPS, JEE, NEET, state PSCs and government documents. PDF tools included.

---

## 📁 Project Structure

```
exam-hub/
├── index.html              ← Main tool page (homepage)
├── sitemap.xml             ← SEO sitemap
├── robots.txt              ← Search engine crawl rules
├── css/
│   └── style.css           ← All styles (mobile-first)
├── js/
│   └── engine.js           ← Image editing + PDF engine
├── data/
│   └── exams.json          ← Master database (26 central + 30 states)
└── pages/
    ├── about.html
    ├── contact.html
    ├── privacy.html
    ├── terms.html
    ├── disclaimer.html
    └── license.html
```

---

## 🚀 Deployment

### Option 1: GitHub Pages (Free)
1. Create a GitHub repository (e.g. `exam-photo-hub`)
2. Upload all files maintaining the folder structure
3. Go to Settings → Pages → Source: `main` branch, `/root`
4. Your site will be live at `https://yourusername.github.io/exam-photo-hub/`

### Option 2: Netlify (Free, Custom Domain)
1. Drag & drop the entire `exam-hub/` folder to [netlify.com/drop](https://netlify.com/drop)
2. Get instant deployment with a netlify URL
3. Add a custom domain in Netlify settings

### Option 3: Vercel (Free)
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the `exam-hub/` directory
3. Follow the prompts

### Option 4: Any Static Hosting
Upload all files to any web host that supports static HTML files. No server-side code required.

---

## 💰 Google AdSense Setup

1. Sign up at [adsense.google.com](https://adsense.google.com)
2. Get your Publisher ID (format: `ca-pub-XXXXXXXXXXXXXXXX`)
3. In `index.html` and all page files, uncomment and update the AdSense script:
   ```html
   <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX" crossorigin="anonymous"></script>
   ```
4. Replace the `<div class="ad-slot ...">` placeholders with actual `<ins class="adsbygoogle">` tags
5. Ad slots are pre-positioned at: header (728×90), sidebar (300×250 + 300×600), footer (728×90)

---

## 🔧 Customization

### Update Domain
Search and replace `https://examphoto.in` with your actual domain in:
- All `<link rel="canonical">` tags
- All `<meta property="og:url">` tags
- `sitemap.xml`

### Add More Exams
Edit `data/exams.json` to add exams:
```json
{
  "id": "unique_id",
  "name": "Exam Name",
  "photo": { "w": 200, "h": 230, "kb": 300, "bg": "white", "fmt": "jpg" },
  "signature": { "w": 200, "h": 67, "kb": 50, "bg": "white", "fmt": "jpg" }
}
```

### Contact Form Backend
The contact form currently shows a success message client-side.  
For real email delivery, integrate with:
- [Formspree](https://formspree.io) (free tier: 50 submissions/month)
- [EmailJS](https://emailjs.com) (free tier: 200 emails/month)
- Your own backend API

---

## 🛡️ Features
- ✅ 100% browser-side processing (no server uploads)
- ✅ Mobile-first responsive design
- ✅ Indian tricolor theme (Saffron + Navy + Green)
- ✅ Background removal (flood-fill algorithm)
- ✅ Auto compress to KB limit
- ✅ PDF: OCR, compress, split, rotate, merge
- ✅ Image → PDF, PDF → Image
- ✅ Google AdSense ready (ad slots pre-placed)
- ✅ SEO optimized (meta tags, sitemap, robots.txt, schema.org)
- ✅ All legal pages included

---

## 📜 License
Original code © 2026 — All rights reserved.  
External libraries: jsPDF (MIT), PDF.js (Apache 2.0), Google Fonts (OFL).  
Free for personal use. Commercial copying prohibited.

See [pages/license.html](pages/license.html) for full details.
