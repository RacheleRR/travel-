# ✈️ Travel Plans for 2

A shared, real-time trip planner built for two (or more). Plan your route, itinerary, budget, and packing list together — any change one person makes is instantly visible to everyone.

🌍 **Live at:** `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME`

---

## Features

- **🗺 Interactive Route Map** — Add destinations by name or by clicking the map, connected by a visual route line
- **🗓 Day-by-Day Itinerary** — Plan activities with times and types (food, stay, travel, activity), with real dates shown on each day
- **💸 Budget Tracker** — Track expenses by category with a live progress bar and spending breakdown
- **🎒 Packing List** — Pre-filled categories you can check off and customise
- **📓 Notes & Links** — Free-form notes plus a saved links section for bookings and resources
- **📊 Overview Dashboard** — Trip summary with countdown to departure, total days, stops, and remaining budget
- **🖨 Print / Export** — Clean print layout of the full plan
- **🔄 Real-time sync** — Powered by Firebase Realtime Database. Everyone sees the same data, live

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

### 2. Open locally

Just open `index.html` in any browser. No build step, no dependencies to install.

> ⚠️ Without Firebase configured, data saves to your browser's local storage only.

### 3. Set up shared sync (Firebase)

To enable real-time shared data for all collaborators:

1. Go to [console.firebase.google.com](https://console.firebase.google.com) and open your project
2. Navigate to **Build → Realtime Database** and create a database in test mode
3. Go to **Project Settings → Your apps** and copy your `firebaseConfig`
4. Open `index.html` and find the `FIREBASE_CONFIG` block near the bottom of the file — paste your values in
5. In the Firebase console, set your database rules to allow read/write:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

6. Push to GitHub — done!

### 4. Deploy to GitHub Pages

1. Go to your repo on GitHub → **Settings → Pages**
2. Under **Source**, select `main` branch and `/ (root)` folder
3. Click **Save** — your site will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME`

Share that link with your travel partner and you're both in sync 🎉

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Vanilla HTML/CSS/JS | No framework, runs anywhere |
| [Leaflet.js](https://leafletjs.com) | Interactive map |
| [OpenStreetMap](https://www.openstreetmap.org) | Map tiles & geocoding |
| [Firebase Realtime Database](https://firebase.google.com/products/realtime-database) | Live shared data sync |
| Google Fonts (Lora + DM Sans) | Typography |

---

## Project Structure

```
/
└── index.html      # The entire app — single self-contained file
└── README.md       # This file
```

---

## Notes

- All data is stored in Firebase under a single shared `trip` node — everyone edits the same plan
- If Firebase is not configured, the app falls back to `localStorage` (per-device only)
- The app is intentionally a single HTML file — easy to host anywhere, no server needed
- To reset all shared data, use the 🗑 **Clear all data** button in the bottom-left corner

---

*Made with ❤️ for adventure*
