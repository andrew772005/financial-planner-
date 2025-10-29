Personal Finance Tracker — PWA
================================

This is a Progressive Web App (PWA) version tailored for Android Chrome (e.g., POCO F5). It works offline and keeps data using IndexedDB (with a localStorage fallback), and it can be installed to your Home Screen like a native app.

Files
-----
- index.html — the app UI and logic (no external libraries)
- sw.js — service worker for offline caching
- manifest.webmanifest — PWA manifest
- /icons/icon-192.png and /icons/icon-512.png — app icons

How to run & install on Android (POCO F5)
-----------------------------------------
1. Copy the folder to any static hosting (recommend: GitHub Pages, Netlify, Cloudflare Pages), OR run a local server on your laptop/phone.
   - Option A (GitHub Pages): upload all files to a repo → Settings → Pages → Deploy → open the URL in Chrome on your phone.
   - Option B (Local quick test on PC): `python -m http.server 8080` in the folder, then open `http://<your_pc_ip>:8080` on your phone (same Wi‑Fi).
2. Open the site in Chrome (Android).
3. You should see an “Install app” banner; or open the Chrome menu ⋮ → “Add to Home screen”.
4. After installation, you can open it from your Home Screen. It works offline and stores data on-device.

Notes
-----
- Service workers only register on https (or localhost). Opening index.html via `file://` won’t install the PWA; the app still works and saves using IndexedDB.
- Use Export JSON/CSV to move data between devices.
