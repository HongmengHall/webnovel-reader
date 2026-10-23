# Webnovel Reader

A free, static web reader for your own EPUB, PDF and TXT files. No server and no account. Your books are stored in your own browser (IndexedDB), so nothing is uploaded anywhere.

## Features

- Add EPUB, PDF and TXT files from the Library panel, or drag them onto the page
- Two reading modes: **infinite scroll** (chapters load as you go) and **page turn** (tap the left or right side, swipe, or use arrow keys, Space and PageUp/PageDown)
- Background and text colour: 7 presets plus free colour pickers
- 12 fonts, plus font size and line height
- Adjustable page width
- Chapter list, and your position is saved for every book
- Settings are remembered between visits

## Deploy on GitHub Pages

1. Create a new repository on GitHub, for example `webnovel-reader`.
2. Upload `index.html` and `README.md`, or push from your computer:
   ```bash
   git init
   git add .
   git commit -m "Add webnovel reader"
   git branch -M main
   git remote add origin https://github.com/<your-username>/webnovel-reader.git
   git push -u origin main
   ```
3. In the repository, go to **Settings → Pages**. Under **Build and deployment**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute your reader is live at `https://<your-username>.github.io/webnovel-reader/`.

To run it locally instead, open `index.html` in a browser. If a browser blocks something on `file://`, run `python3 -m http.server` in this folder and open `http://localhost:8000`.

## Notes and limits

- **Books are per browser and per device.** Your library on your phone and your laptop are separate. Clearing site data removes the library.
- **PDFs are shown as reflowed text** so that colours, fonts and width can change. Paragraphs are rebuilt from the text layer, so complex layouts, columns and tables may come out imperfect. Scanned PDFs have no text layer and need OCR first.
- **EPUB links** inside chapters are disabled. Use the Chapters list to jump around. Publisher styling is removed so your theme applies.
- DRM-protected EPUBs can't be opened.
- Fonts load from Google Fonts, and the EPUB and PDF libraries (JSZip, PDF.js) load from cdnjs, so the first load needs internet.

## Ideas for later

Bookmarks and search, a custom font upload, text-to-speech, and syncing progress between devices.
