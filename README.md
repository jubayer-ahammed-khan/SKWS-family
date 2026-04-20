# SKWS Family — সেবা ডিরেক্টরি

A simple community shop directory for SKWS Family members.

---

## 🚀 Setup in 3 Steps

### Step 1 — Create Your Google Sheet

Create a new Google Sheet with these **exact column headers** in Row 1:

| name | category | owner | area | address | phone | whatsapp | photo | description | facebook | maplink |
|------|----------|-------|------|---------|-------|----------|-------|-------------|----------|---------|

**Column details:**
- `name` — Shop or institution name (e.g. রহমান মুদিখানা, আল-নূর মাদরাসা, হোম টিউটর)
- `category` — Must be exactly one of: `food`, `clothing`, `health`, `electronics`, `education`, `other`
- `owner` — Owner or person's full name (e.g. মোঃ আব্দুর রহমান)
- `area` — Short area (e.g. সিদ্ধিরগঞ্জ, নারায়ণগঞ্জ)
- `address` — Full address
- `phone` — Phone number (e.g. +880 1711-000001)
- `whatsapp` — WhatsApp number digits only, no spaces (e.g. 8801711000001)
- `photo` — Direct image URL (optional, leave blank if none)
- `description` — Short description
- `facebook` — Facebook page URL (optional)
- `maplink` — Google Maps share link (optional). Find location → Share → Copy link

**Category guide:**
| Category | বাংলা | Use for |
|----------|-------|---------|
| `food` | খাদ্য ও মুদিখানা | Grocery, restaurant, food shop |
| `clothing` | পোশাক ও টেইলার | Clothing, tailoring |
| `health` | স্বাস্থ্য ও চিকিৎসা | Doctor, clinic, pharmacy |
| `electronics` | ইলেকট্রনিক্স ও মেরামত | Mobile, laptop, repairs |
| `education` | শিক্ষা ও প্রতিষ্ঠান | Teacher, tutor, school, madrasah, college |
| `other` | অন্যান্য সেবা | Driver, carpenter, any personal service |

> **Note:** For `education` and `other`, the **owner/person's name** is shown as the main title on the card — making it person-first for individual service providers.

---

### Step 2 — Publish Your Sheet as CSV

1. Open your Google Sheet
2. Go to **File → Share → Publish to web**
3. Select **Sheet1** and **Comma-separated values (.csv)**
4. Click **Publish** → Copy the URL

---

### Step 3 — Connect to the Website

Open `index.html` and find this line near the top of the `<script>` section:

```javascript
const SHEET_CSV_URL = 'YOUR_GOOGLE_SHEET_CSV_URL_HERE';
```

Replace it with your copied URL:

```javascript
const SHEET_CSV_URL = 'https://docs.google.com/spreadsheets/d/YOUR_ID/pub?output=csv';
```

---

## 🌐 Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `skws-family`)
2. Upload `index.html` to the root of the repo
3. Go to **Settings → Pages**
4. Source: **Deploy from branch → main → / (root)**
5. Your site will be live at: `https://yourusername.github.io/skws-family/`

---

## ➕ Adding a New Member / Shop (Admin)

Just open your Google Sheet and add a new row. The website **automatically updates** — no code, no GitHub needed for data changes.

---

## 📁 File Structure

```
/
└── index.html       ← The entire website (single file)
└── README.md        ← This file
```

That's it. One file. 🎉
