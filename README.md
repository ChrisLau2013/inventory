# Inventory Counting App

A PWA (Progressive Web App) for iPhone inventory counting — works offline, installable to home screen.

## Files

```
inventory-app/
├── index.html      ← Main app
├── manifest.json   ← PWA manifest (home screen install)
├── sw.js           ← Service worker (offline support)
├── icon.png        ← App icon (180×180 px) ← YOU MUST ADD THIS
└── README.md
```

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `inventory-app`)
2. Upload all files in this folder to the repo root
3. Go to **Settings → Pages → Source → Deploy from branch → main / root**
4. Your app will be live at: `https://YOUR_USERNAME.github.io/inventory-app/`

> ⚠️ HTTPS is required for camera (OCR/Barcode scan). GitHub Pages provides this automatically.

## Add to iPhone Home Screen

1. Open the app URL in Safari
2. Tap the **Share** button (square with arrow)
3. Tap **Add to Home Screen**
4. The app now works like a native app, including offline

## CSV Format

Your product list CSV must have these columns (header row required):

```
category,product,unit,supplier,brand
Dry Goods,Flour 25kg,bag,ABC Supplier,Brand X
Dry Goods,Sugar 10kg,bag,XYZ Co,Brand Y
```

## Features

- 📷 OCR scan (reads product labels with camera)
- 🔳 Barcode scan (reads barcodes)
- 🔒 Location lock (lock location while counting same area)
- 📥 Export CSV (date and time in separate columns)
- 📱 Offline support via Service Worker
- ➕ Manual entry for unlisted products
- 📄 Paginated history (20 records per page)
- ＋/− quantity adjustment buttons
