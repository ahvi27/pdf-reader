# 📄 PaperView — PDF Reader

A simple PDF reader built with HTML, CSS, and JavaScript. Open local documents in a clean purple interface with light and dark themes.

## Features

- Open PDFs from your device
- Drag and drop a PDF to read it
- Light and dark mode with saved theme preference
- Fullscreen reading on supported browsers
- Open the document in a separate tab
- Download the selected PDF
- Display the filename and file size
- Responsive layout
- Local file handling without uploads

## Built With

- HTML5
- CSS3
- Vanilla JavaScript
- Browser’s built-in PDF viewer

## Getting Started

1. Download or clone this repository.
2. Open `index.html` in your browser.
3. Click **Choose PDF** or drag a PDF into the upload area.

No installation, API key, or build tools are required.

## Project Structure

```text
paperview/
├── index.html
└── README.md
```

## How to Use

| Control | Action |
|---|---|
| Choose PDF | Select a local PDF |
| Open another | Replace the current document |
| Open in tab | Open the PDF in a separate browser tab |
| Download | Save a copy of the selected file |
| Fullscreen | Expand the reader where supported |
| Close | Close the document |
| Dark mode / Light mode | Switch the interface theme |

Use the browser’s PDF toolbar for page navigation, search, zoom, and printing. Available controls depend on your browser.

## Privacy

PDF files are processed locally through browser object URLs. The application does not upload documents to a server.

Only the theme preference is saved in local storage when available. Documents are not saved by the app or restored after a refresh.

## Browser Compatibility

A browser with a built-in PDF viewer is required for embedded reading. Mobile behavior and fullscreen support vary.

If a PDF does not appear, use **Open in tab** or **Download**.

## Limitations

- PDF viewing controls depend on the browser.
- Dark mode changes the app interface, not the PDF’s page colors.
- The app does not edit, annotate, merge, or convert PDFs.
- A PDF signature check does not guarantee that a file is valid or readable.

## Customization

Edit the CSS variables in `index.html` to change the theme:

```css
:root {
  --bg: #f5f3ff;
  --surface: #ffffff;
  --text: #28233f;
  --primary: #7955db;
}
```
