# 🌾 КАНТЕМИР-АГРО — Digital Presence Package
## Deployment & Setup Guide

---

## FILES IN THIS PACKAGE

```
kantemir-agro/
├── index.html                    ← Main website (all 4 languages)
├── sitemap.xml                   ← SEO sitemap
├── robots.txt                    ← Search engine instructions
├── assets/
│   ├── css/main.css              ← Stylesheet
│   └── js/main.js                ← All content + language engine
├── GOOGLE_BUSINESS_PROFILE_GUIDE.md  ← Task 2: GBP optimization
├── EMAIL_SIGNATURE.html          ← Task 3: Email signature
└── EMAIL_AUTORESPONDER.md        ← Task 4: Auto-responder templates
```

---

## TASK 1: DEPLOY WEBSITE TO GITHUB PAGES

### Step 1: Create GitHub repository
1. Go to github.com → New repository
2. Name: `kantemir-agro.kz` (or `kantemir-agro`)
3. Public, no template
4. Create repository

### Step 2: Upload files
```bash
git init
git add .
git commit -m "Initial site launch"
git remote add origin https://github.com/YOUR_USERNAME/kantemir-agro.kz.git
git push -u origin main
```

### Step 3: Enable GitHub Pages
- Repository → Settings → Pages
- Source: Deploy from branch → main → / (root)
- Save → site will be live at `https://YOUR_USERNAME.github.io/kantemir-agro.kz/`

### Step 4: Connect custom domain (kantemir-agro.kz)
1. In GitHub Pages settings → Custom domain → enter: `kantemir-agro.kz`
2. At your domain registrar, add DNS records:
   ```
   A     @    185.199.108.153
   A     @    185.199.109.153
   A     @    185.199.110.153
   A     @    185.199.111.153
   CNAME www  YOUR_USERNAME.github.io
   ```
3. Check "Enforce HTTPS" (wait 24h for DNS propagation)

---

## TASK 2: GOOGLE BUSINESS PROFILE

See: `GOOGLE_BUSINESS_PROFILE_GUIDE.md`

1. Go to business.google.com
2. Search for your business or click "Add your business"
3. Follow the guide — paste all content from the guide file

---

## TASK 3: EMAIL SETUP

### Option A: Zoho Mail (FREE for up to 5 users)
1. Go to zoho.com/mail → Free plan
2. Add domain: kantemir-agro.kz
3. Verify domain via DNS TXT record
4. Create: info@, export@, director@
5. Import signature from EMAIL_SIGNATURE.html

### Option B: Google Workspace (~$6/month)
1. workspace.google.com
2. Add domain, verify, create users

### Setting up the HTML signature:
- Open EMAIL_SIGNATURE.html in a browser
- Select all → Copy
- Paste into Gmail/Outlook signature editor

---

## TASK 4: AUTO-RESPONDER

See: `EMAIL_AUTORESPONDER.md`

Set up on export@kantemir-agro.kz using your email provider's settings.

---

## WHAT TO DO NEXT (Priority Order)

- [ ] 1. Deploy website to GitHub Pages
- [ ] 2. Fill in real phone number in index.html
- [ ] 3. Set up Google Business Profile
- [ ] 4. Create email accounts
- [ ] 5. Set up auto-responder on export@
- [ ] 6. Add email signatures to all accounts
- [ ] 7. Upload real photos to Google Business Profile
- [ ] 8. Ask 3-5 business partners for Google reviews
- [ ] 9. Submit sitemap to Google Search Console

---

## WEBSITE FEATURES

✅ **4 languages** — Russian, English, Chinese (Simplified), Kazakh  
✅ **Auto language detection** — browser language auto-selects  
✅ **Flag switcher** in header  
✅ **Mobile responsive** — works on WeChat in-app browser  
✅ **6 product cards** with full specs  
✅ **Export section** with logistics, payment, documentation  
✅ **Contact form** (requires backend or Formspree — see below)  
✅ **SEO** — Schema.org, Open Graph, hreflang, sitemap  
✅ **Fast** — static HTML, no tracking, no cookies  

### Contact Form Setup (Formspree — Free):
1. Go to formspree.io → Create account
2. New form → Get form endpoint URL
3. In index.html, find the `<form id="inquiry-form">` tag
4. Add: `action="https://formspree.io/f/YOUR_FORM_ID"` `method="POST"`
5. Emails will be sent to your address automatically

---

## CUSTOMIZATION

### Add your real phone number:
Search in index.html for `[INSERT ACTUAL PHONE]` → replace with actual number
Also add `<a href="tel:+7XXXXXXXXXX">+7 (XXX) XXX-XX-XX</a>`

### Replace placeholder Unsplash images with real photos:
In `assets/js/main.js`, search for `images.unsplash.com` entries in the PRODUCTS array.
Replace URLs with your actual product photo URLs.

### Update Google Maps embed:
In index.html, find the `<iframe>` with maps.google.com.
Replace with the actual embed code from Google Maps for your exact address.

---

*Package prepared for ТОО «КАНТЕМИР-АГРО» (BIN 041240002101)*  
*kantemir-agro.kz | export@kantemir-agro.kz*
