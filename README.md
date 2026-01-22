# 📻 Ham Radio Logbook & QSL Generator

A modern, beautiful web application for viewing amateur radio logbook statistics and generating QSL cards.

🔗 **Live Demo:** [https://ea7lhs.github.io/ea7lhs](https://ea7lhs.github.io/ea7lhs)

![Ham Radio Logbook](https://img.shields.io/badge/Ham%20Radio-Logbook-success)
![QSL Generator](https://img.shields.io/badge/QSL-Generator-blue)


<img width="1920" height="1280" alt="hamlog1" src="https://github.com/user-attachments/assets/f0fce88a-a419-4d75-9cbf-f53e4176045e" />


---

## 🌟 What is this?

This is **EA7LHS's personal ham radio logbook** viewer and QSL card generator. You can:

- 📊 View my operating statistics and activity
- 🔍 Search through my contacts
- 🎴 Generate and download QSL cards for any QSO
- 🎨 Switch between different visual themes

The application is updated regularly with my latest contacts.

---

## 🚀 How to Use

### View Statistics

Simply visit the main page to see:
- Total QSOs, countries worked, modes, and bands
- Activity heatmap (GitHub-style) showing operating patterns
- Top countries and modes
- Recent contacts

### Search for a QSO

1. Use the search box to find specific contacts
2. Search by: callsign, name, country, mode, band, or grid square
3. Click **"VIEW QSL"** on any contact to generate a card

### Generate a QSL Card

1. Find your contact using search or the recent contacts table
2. Click the **"VIEW QSL"** button
3. The card will be generated automatically
4. Click **"DOWNLOAD QSL CARD"** to save as PNG

**Direct Link Method:**

You can also generate a QSL card directly using this URL format:

```
https://ea7lhs.github.io/ham-radio-logbook/qsl.html?call=YOURCALL&date=YYYYMMDD&time=HHMM
```

---

## 🎨 Available Themes

Click the theme selector (if available) or bookmark different versions:

### 🌌 Default (Retro-Futuristic)
Dark theme with neon green and cyan accents, perfect for late-night browsing.

### 📜 Classic (Traditional)
Minimalist design with cream backgrounds, like a traditional logbook.

### 🎯 Brutalist (Bold)
Raw, bold design with thick borders and asymmetric layout.

### 🌸 Vaporwave (80s Neon)
Purple and pink gradients with synthwave aesthetics.

### 🌫️ Neumorphism (Soft UI)
Modern soft shadows design with elegant depth.

### 💻 Terminal (Hacker)
Green phosphor text on black, classic terminal look.

---

## ❓ FAQ

### Can I use this for my own logbook?

**Yes!** This is open-source. You can:

1. Fork this repository
2. Replace `logbook.adi` with your own ADIF file
3. Edit `config.json` with your station info
4. Deploy to GitHub Pages

See the [Installation Guide](#-installation-for-your-own-station) below.

### What information is shown?

Shown Information from the logbook:
- Callsign
- Date and time
- Frequency and mode
- Band
- Country
- RST reports

### Can others get a QSL card for our QSO?

Yes! Search for your callsign, generate the card, and download it.

### What format is the logbook?

Standard ADIF (Amateur Data Interchange Format) exported from my logging software.

---

## 🔧 Installation for Your Own Station

Want to create your own logbook viewer? Here's how:

### 1. Fork or Download

Get the code from: [GitHub Repository](https://github.com/ea7lhs/public-hamlog)

### 2. Prepare Your Files

```
your-logbook/
├── index.html
├── qsl.html
├── config.json          ← Edit this
├── logbook.adi          ← Replace with yours
└── default.css (+ other themes)
```

### 3. Configure Your Station

Edit `config.json`:

```json
{
  "callsign": "YOUR-CALL",
  "name": "Your Name",
  "location": "Your QTH",
  "cssFile": "default.css",
  "qslBackgroundImage": "",
  "qslBackgroundBlur": 8,
  "qslBackgroundOpacity": 0.7,
  "display": {
    "topCountries": 5,
    "topModes": 10,
    "recentContacts": 10,
    "maxSearchResults": 50
  }
}
```

### 4. Add Your Logbook

Export your logbook from your logging software or platform (N1MM+, Logger32, QRZ.com, etc.) as ADIF format and save as `logbook.adi`

### 5. Deploy

**GitHub Pages (Recommended):**

1. Create a new **public** repository on GitHub
2. Upload all files
3. Go to Settings → Pages
4. Select main branch as source
5. Your site will be at: `https://yourusername.github.io/repository-name`


### 6. Keep It Updated

After each operating session:
1. Export new ADIF from your logger
2. Replace `logbook.adi`
3. Commit and push to GitHub

---

## 🎴 QSL Card Customization

Want to add your antenna or shack photo to QSL cards?

1. Add an image file (e.g., `antenna.jpg`) to your repository
2. Edit `config.json`:

```json
{
  "qslBackgroundImage": "antenna.jpg",
  "qslBackgroundBlur": 8,        // 0-50 (lower = sharper)
  "qslBackgroundOpacity": 0.7    // 0.0-1.0 (lower = more visible)
}
```

**Tips:**
- Use landscape photos (1400×900 or similar ratio)
- Try `blur: 5, opacity: 0.5` for visible backgrounds
- Try `blur: 15, opacity: 0.9` for subtle backgrounds

---

## 📊 Features

### Statistics Dashboard
- **Total Counts:** QSOs, countries, modes, bands
- **Activity Heatmap:** GitHub-style visualization with year navigation
- **Top Lists:** Most worked countries and modes
- **Recent Contacts:** Latest QSOs with all details

### Advanced Search
Search across your entire logbook by:
- Callsign (e.g., "EA7")
- Country (e.g., "Spain")
- Mode (e.g., "FT8")
- Band (e.g., "20M")
- Grid square
- Name or QTH

### QSL Card Generator
- Automatic card generation from logbook data
- Theme-aware design (adapts to selected CSS)
- Custom background images
- High-quality PNG export (1400×900px)
- Print-ready output

### Multiple Themes
Six beautiful themes to choose from:
- Default (Retro-Futuristic)
- Classic (Traditional)
- Brutalist (Bold)
- Vaporwave (80s Neon)
- Neumorphism (Soft UI)
- Terminal (Hacker)

---

## 🛠️ Technical Stack

- Pure HTML5, CSS3, and JavaScript
- No frameworks or dependencies
- Fully static (works for free on GitHub Pages)
- Responsive design (mobile-friendly)
- ADIF parser built-in

---

## 📞 Contact

**Station:** EA7LHS  
**Name:** Daniel

- 📧 Email: qrzea7lhs@gmail.com
- 🔗 QRZ: [qrz.com/db/ea7lhs](https://www.qrz.com/db/ea7lhs)
- 📻 LoTW: EA7LHS
- 💬 eQSL: EA7LHS

---

## 🙏 Credits

Built with ❤️ for the ham radio community.

**73 de EA7LHS!** 📻

*Last updated: January 2026*
