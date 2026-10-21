# 📄 PaperView — Read & Study

A PDF reader and study workspace built with HTML, CSS, and vanilla JavaScript. Read local PDFs, write notes, bookmark page numbers, and stay focused with a study timer.

## Features

- 📂 Open local PDF files
- 🖱️ Drag-and-drop upload
- 📝 Write and automatically save notes for each document
- 🔖 Add, remove, and revisit page bookmarks
- 📍 Jump to a specified page
- 📤 Export notes and bookmarks as a `.txt` file
- ⏱️ Study timer with start, pause, reset, and custom duration
- 🎯 Focus mode that hides study tools
- 🌙 Light and dark themes
- ⛶ Fullscreen reading where supported
- ⬇️ Download the selected PDF
- 📱 Responsive layout

## Technologies

- HTML5
- CSS3
- Vanilla JavaScript
- Local Storage
- Web Crypto API, when available
- Browser’s built-in PDF viewer

## Getting Started

1. Download or clone the repository.
2. Open `index.html` in your browser.
3. Click **Choose PDF** or drop a PDF into the upload area.

No installation, dependencies, API keys, or build commands are required.

## Project Structure

```text
paperview/
├── index.html
└── README.md
```

## Using PaperView

### Reading PDFs

Choose a local PDF to open it. Use the browser’s embedded PDF toolbar for zoom, search, printing, and page navigation.

Select **Open in tab** if the embedded viewer does not work.

### Notes

Write in **My notes** to save notes automatically.

Notes are stored in this browser and associated with the selected document. Reopening the document restores them when browser storage is available.

Click **Export notes (.txt)** to download your notes and bookmarked page numbers.

### Bookmarks

1. Enter a page number in **Page shortcuts**.
2. Click **Bookmark this number**.
3. Click a saved bookmark to request that page.
4. Click **×** to remove a bookmark.

Enter the page number manually: the app cannot detect the embedded viewer’s current page.

### Study Timer

- Enter a duration from **1 to 180 minutes** and click **Set**.
- Click **Start** to begin.
- Click **Pause** to pause.
- Click **Reset** to restore the selected duration.

The timer displays a completion message. It does not send system notifications or play an alarm.

### Focus and Fullscreen

**Focus** hides the header and study sidebar. Click **Exit focus** to restore them.

**Fullscreen** expands the workspace on supported browsers.

## Privacy and Storage

- PDF files remain on your device and are not uploaded.
- Notes, bookmarks, and theme preferences use browser Local Storage.
- The PDF itself is not saved by the app.
- Reopen your PDF after refreshing the page.
- Notes do not sync between devices or browsers.
- Clearing browser data may delete saved notes and bookmarks.
- Export important notes to keep a separate copy.

When available, the Web Crypto API calculates a local file hash to identify a document. Otherwise, the app uses its filename, size, and modification date.

## Browser Compatibility

Embedded PDF rendering requires a browser with a built-in PDF viewer.

Page shortcuts, fullscreen, and mobile PDF viewing depend on browser support. Use **Open in tab** or **Download** if embedded viewing is unavailable.

## Limitations

- The app cannot detect the PDF viewer’s current page or total page count.
- Page shortcuts cannot verify whether a page exists.
- Dark mode changes the interface, not PDF page colors.
- The app does not edit or annotate the PDF itself.
- Saved notes require available browser storage.
- The timer does not continue after closing or refreshing the app.
- PDF signature checking does not guarantee that a file is valid or readable.

## Customization

Change the CSS variables in `index.html` to customize the interface:

```css
:root {
  --bg: #f5f3ff;
  --panel: #ffffff;
  --text: #28233f;
  --accent: #7955db;
  --soft: #efe9ff;
}
```

Edit the `body.dark` variables to customize dark mode.

## Possible Future Improvements

- PDF.js integration for consistent rendering
- Automatic page count and reading progress
- Text highlighting and PDF annotations
- Thumbnail navigation
- Notes import and backup restoration
- Optional timer sounds
