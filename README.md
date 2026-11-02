# Lịch Âm Cao Niên — Portable Web App

This folder is a standalone Progressive Web App (PWA) conversion of the Android app's existing HTML/CSS/JavaScript interface.

## Run locally

A PWA must be served from `localhost` or HTTPS; opening `index.html` directly with `file://` will not enable offline installation/service workers.

With Python installed:

```bash
cd pwa
python -m http.server 8080
```

Then open http://localhost:8080 in a browser.

## Install

- **Android (Chrome):** open the hosted HTTPS address, then choose **Install app** or **Add to Home screen** from the browser menu.
- **Windows / desktop (Chrome or Edge):** open the hosted HTTPS address and use the install icon in the address bar, or the browser menu's **Install** option.
- **iPhone/iPad (Safari):** Share → **Add to Home Screen**.

## Publish

Upload the *contents* of this `pwa` folder to any static HTTPS host, such as GitHub Pages. No build step or server-side application is required.

## Offline and online features

The calendar, lunar calculations, monthly view, good/bad day information and prayer content are bundled locally and cached for offline use after the first successful visit. News and lottery RSS feeds require internet access and use the public AllOrigins raw CORS proxy so a browser can request the feeds. This third-party proxy is not part of this app and may occasionally be unavailable; the offline calendar remains usable.

## Notes

- The original Android-only JavaScript bridge is optional; browser mode now opens external news links in a new tab.
- This PWA does not include the Android APK or Kotlin/Compose wrapper.
