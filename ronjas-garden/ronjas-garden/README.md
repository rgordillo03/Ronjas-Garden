# 🌿 Ronja's Garden

A motivational digital garden — a personal website that shows a random photo and an inspiring quote every time she visits.

---

## 🚀 SETUP GUIDE (Step by Step)

### STEP 1 — Set Up Cloudinary (Free Photo Hosting)

1. Go to [cloudinary.com](https://cloudinary.com/) and create a **free account**
2. After signing up, go to your **Dashboard** — copy your **Cloud Name** (it looks like `dxyz1abc2`)
3. **Enable Resource List API:**
   - Go to **Settings** → **Security**
   - Scroll to **"Restricted media types"** section
   - Make sure **"Resource list"** is checked/enabled
   - Save changes
4. **Upload your photos:**
   - Go to **Media Library** (top menu)
   - Click **Upload** → drag & drop all your photos
   - After uploading, **select all photos** → click **"Manage Tags"** → add the tag: `ronjas-garden`
   - That's it! The website will automatically find and display them

> 💡 **Tip:** You can add more photos anytime — just upload and tag them `ronjas-garden`. They'll appear on the site automatically, no redeployment needed!

---

### STEP 2 — Deploy to Vercel (Free Hosting)

1. Go to [vercel.com](https://vercel.com/) and sign up (use GitHub, or email)
2. Install the Vercel CLI or use the web dashboard
3. **Option A — Deploy via GitHub (Recommended):**
   - Push this project to a GitHub repository
   - In Vercel dashboard, click **"Add New Project"** → Import your repo
   - Before deploying, add **Environment Variables:**
     - `VITE_CLOUDINARY_CLOUD_NAME` = your cloud name from Step 1
     - `VITE_CLOUDINARY_TAG` = `ronjas-garden`
   - Click **Deploy**

4. **Option B — Deploy via drag & drop:**
   - First, build the project locally:
     ```bash
     npm install
     ```
   - Create a `.env` file in the root folder:
     ```
     VITE_CLOUDINARY_CLOUD_NAME=your_cloud_name
     VITE_CLOUDINARY_TAG=ronjas-garden
     ```
   - Build:
     ```bash
     npm run build
     ```
   - Go to [vercel.com/new](https://vercel.com/new) → drag the `dist` folder

---

### STEP 3 — Connect Your Custom Domain

1. Buy a domain (e.g., `ronjas-garden.com`) from:
   - [Namecheap](https://namecheap.com) (~€9/year)
   - [Porkbun](https://porkbun.com) (~€8/year)
   - [Google Domains](https://domains.google) / Squarespace Domains
2. In your **Vercel project** → **Settings** → **Domains**
3. Add your domain name (e.g., `ronjas-garden.com`)
4. Vercel will show you DNS records to add — go to your domain registrar and add them
5. Wait 5-10 minutes → your site is live on your custom domain! 🎉

---

### STEP 4 — Program the NFC Tag

1. Buy NFC stickers (NTAG215 or NTAG216) — available on Amazon for ~€5-8 for a pack
2. Download **"NFC Tools"** app (free, available on iOS and Android)
3. Open the app → **Write** → **Add a record** → **URL**
4. Enter your domain: `https://ronjas-garden.com`
5. Hold your phone against the NFC sticker → **Write**
6. Stick the NFC tag inside a greeting card
7. She taps the card → the garden opens 🌿💛

---

## ✏️ HOW TO EDIT QUOTES

Open `src/quotes.js` — the file is organized by category with clear sections.

**To add a quote:**
```js
{ text: "Your quote here", author: "Author Name", category: "mindfulness" },
```

**Categories:** `yoga`, `mindfulness`, `ayurveda`, `psychology`, `motivation`, `growth`, `love`, `personal`

**Personal quotes** (from you) are at the bottom — search for `"Your Love"` to find them. Edit these to make them truly yours!

After editing, just push to GitHub and Vercel will auto-redeploy.

---

## 📸 HOW TO ADD MORE PHOTOS

1. Log into [cloudinary.com](https://cloudinary.com)
2. Go to **Media Library**
3. Upload new photos
4. Tag them with `ronjas-garden`
5. Done — they'll appear on the site automatically!

---

## 🛠️ DEVELOPMENT (Optional)

Run locally:
```bash
npm install
npm run dev
```

The site will be available at `http://localhost:5173`

---

## 📁 PROJECT STRUCTURE

```
ronjas-garden/
├── index.html          ← Entry point
├── package.json        ← Dependencies
├── vite.config.js      ← Build config
├── .env.example        ← Environment variables template
├── src/
│   ├── main.jsx        ← React entry
│   ├── App.jsx         ← Main app (screens, Cloudinary, logic)
│   ├── quotes.js       ← ✏️ ALL QUOTES HERE — easy to edit!
│   └── index.css       ← Global styles & animations
```

---

Made with love 💛
