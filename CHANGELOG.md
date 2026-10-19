# Changelog

All notable changes to Mova are listed here. Versions follow [Semantic Versioning](https://semver.org);
dates are when the release was published.

## [0.1.0-beta] — unreleased

The first public beta.

### Added
- **Radial menu:** while dragging files, tap Shift to open actions around the cursor. Tap again to switch between formats and tools. The bubbles adapt to the type and number of files.
- **Liquid Glass design:** the radial menu, toasts and every window use native Liquid Glass on macOS 26 and translucent materials on macOS 14–15. Light and dark mode, Reduce Motion and Reduce Transparency are respected.
- **Settings window** (menu bar icon → Settings…) with the same preferences as the menu.
- **Image conversion:** JPG, PNG, WEBP, HEIC, TIFF, AVIF, BMP, PDF and DOCX, with EXIF orientation applied and metadata kept.
- **PDF conversion:** DOCX, JPG/PNG (300 dpi, one file per page) and TXT, with on-device text recognition for scanned pages.
- **Document conversion** between TXT, Markdown, RTF, HTML, DOCX, ODT and PDF. HTML is imported without loading anything from the internet.
- **Video and audio → MP3** (320 kbps), M4A or WAV for MP4, MOV, MKV, M4V, WEBM, AVI and common audio formats, with live progress. Videos without sound get a clear message.
- **Combine PDF:** drop several images, PDFs or documents on PDF to reorder files and pages in a preview, then export one PDF. PDF pages stay vector, and JPEGs are embedded without re-compression.
- **Tools:** Compress, Info (view or remove metadata, including location), Adjust, Markup, Backdrop, Crop, Redact (with text and face detection), and Rotate / Split for PDFs.
- **Batches:** several files convert in parallel, with progress and a summary of anything that failed. Four or more results go into a new folder.
- **Never overwrites:** results always get a new name, and originals are only read.
- **Menu bar:** Open Files…, Recent Results, trigger key (Shift or Control), where to save, sound, Launch at Login, Folder Access Settings, Report a Bug, Copy Diagnostics, Acknowledgements.
- **Universal app** for Apple silicon and Intel, macOS 14 or later. FFmpeg, LAME and libwebp are bundled, so nothing else needs installing.
- **Compress PDF** leaves a PDF alone, and says so, when it is already as small as it can be.

### Known issues
See *Known limitations* in the [README](README.md#known-limitations-beta).
