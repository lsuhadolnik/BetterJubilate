# Songbook with Chords

A lightweight, offline‑capable songbook viewer for `JUBILATE.json`. Lists songs, highlights chords above lyrics, supports playlists, mobile sidebar toggle, font/scroll controls, and PWA install.

## Run locally
```sh
python -m http.server 8000
# or any static server
```
Then open `http://localhost:8000/`.

## PWA / offline
- Service worker: `sw.js` caches `index.html`, `JUBILATE.json`, manifest, and icons.
- Manifest: `manifest.webmanifest` with icons `icon-192.png`, `icon-512.png`.
- Works over `http://localhost` or HTTPS. Reload once online to warm the cache; then it will work offline.

## Features
- Song list with search (tags/categories included).
- Song view with chords above lyrics, font-size controls, quick scroll hotkeys (Enter down, Space up), scroll-step input, and list toggle.
- Playlist tab: create/select default playlist, add via “+ Add”, reorder/remove entries, prev/next navigation.
- Mobile: sidebar hidden by default; toggle via header.

## Keyboard / Page Turner
- Enter: scroll down by step (smooth).
- Space: scroll up by step (smooth).

## Customize cache
Update `ASSETS` in `sw.js` if you add new static files that should be available offline. After changes, bump the cache name to force refresh (e.g., `songbook-cache-v2`).
