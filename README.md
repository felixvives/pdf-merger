# Folio — PDF Tools

A lightweight, client-side PDF utility tool inspired by iLovePDF. No servers, no uploads, no accounts — everything runs entirely in your browser.

---

## Getting Started

No installation needed. Just open `index.html` in any modern browser and you're ready to go.

```
open pdf-tool.html
```

An internet connection is required on first load to fetch two CDN libraries (pdf-lib and PDF.js) and the Google Fonts used in the UI. After that, all file processing happens locally on your machine.

---

## Features

### Merge PDFs
Combine multiple PDF files into a single document.

- Drag and drop or browse to add PDF files
- Reorder files using the ↑ ↓ buttons before merging
- Remove individual files with the ✕ button
- Requires at least 2 files to merge
- Output: `merged.pdf`

### Reorganize Pages
Rearrange, rotate, or remove individual pages within a PDF.

- Load a single PDF to see all pages as visual thumbnails
- Drag and drop pages to reorder them
- Hover over a page to reveal rotate (↻) and delete (✕) controls
- Rotation is applied in 90° increments
- Output: `[original-name]_reorganized.pdf`

### PDF → PNG Images
Export each page of a PDF as a PNG image file.

- Supports three resolution scales: Standard (1×), High (2×), Ultra (3×)
- Click any page thumbnail to download that page individually
- Use "Export All Pages" to download every page in sequence
- Output: `page_1.png`, `page_2.png`, etc.

### Images → PDF
Convert PNG or JPG images into a single PDF document.

- Supports PNG, JPG, and WEBP formats
- Reorder images with ↑ ↓ buttons before converting
- Three page size options:
  - **Fit to image** — page dimensions match each image
  - **A4** — 595 × 842 pt, images centered and scaled to fit
  - **Letter** — 612 × 792 pt, images centered and scaled to fit
- Output: `images.pdf`

---

## Privacy

All file processing happens entirely in your browser using JavaScript. No files are sent to any server. Nothing is stored, logged, or transmitted.

---

## Browser Compatibility

Works in any modern browser with JavaScript enabled.

| Browser | Support |
|---|---|
| Chrome / Edge | ✓ Full support |
| Firefox | ✓ Full support |
| Safari | ✓ Full support |
| Mobile browsers | ✓ Functional (desktop recommended for drag-and-drop) |

---

## Dependencies

Loaded from CDN at runtime — no local installation required.

| Library | Version | Purpose |
|---|---|---|
| [pdf-lib](https://pdf-lib.js.org/) | 1.17.1 | PDF creation, merging, page manipulation |
| [PDF.js](https://mozilla.github.io/pdf.js/) | 3.11.174 | PDF rendering and page preview thumbnails |
| [Syne](https://fonts.google.com/specimen/Syne) | — | Display / heading font |
| [DM Sans](https://fonts.google.com/specimen/DM+Sans) | — | UI body font |

---

## Known Limitations

- Very large PDFs (100+ pages or 50MB+) may be slow to preview in the Reorganize tool due to in-browser rendering
- The "Export All Pages" feature triggers sequential downloads; some browsers may block multiple downloads — allow popups/downloads if prompted
- WEBP images in the Image → PDF converter require browser support for canvas encoding (available in all modern browsers)

---

## License

This project has no external license restrictions. The two runtime libraries are open-source:

- pdf-lib is MIT licensed
- PDF.js is Apache 2.0 licensed
