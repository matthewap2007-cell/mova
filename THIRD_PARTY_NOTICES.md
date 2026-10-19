# Third-party notices

Mova bundles two helper programs, `ffmpeg` and `ffprobe` (inside `Mova.app/Contents/Helpers`).
Mova runs them as separate programs to read video and audio and to write MP3, M4A, WAV and WEBP files.
They are built, unmodified, from these open-source projects:

| Component | Version | License | Website |
|---|---|---|---|
| FFmpeg | 9.0.2 | GNU LGPL 2.1 or later | https://ffmpeg.org |
| LAME (libmp3lame) | 3.100 | GNU LGPL 2 or later | https://lame.sourceforge.io |
| libwebp | 1.6.0 | BSD 3-Clause + Google patent grant | https://chromium.googlesource.com/webm/libwebp |

FFmpeg is configured **without** `--enable-gpl`, `--enable-nonfree` or network protocols. The exact configuration is
printed in the app's Acknowledgements (Help & Feedback → Acknowledgements) and in `BUILD-INFO.txt`.

## Source code
Each release on the [Releases page](https://github.com/matthewap2007-cell/mova/releases) includes
`Mova-<version>-third-party-source.tar.gz`, with:
- the original source archives of FFmpeg, LAME and libwebp exactly as built, plus checksums;
- `build-ffmpeg.sh`, the script that builds the bundled helpers (Xcode Command Line Tools only);
- the full license texts.

Under the LGPL you may modify these libraries and use your own builds: replace the two files in
`Mova.app/Contents/Helpers` with your own `ffmpeg` and `ffprobe`. (Changing the app bundle breaks
its code signature; re-sign it locally with `codesign --force --deep --sign - Mova.app`.)

## Apple frameworks and symbols
Mova uses Apple system frameworks (ImageIO, PDFKit, Vision, Core Image, AppKit, SwiftUI) and SF Symbols,
which are part of macOS and used under Apple's terms.

## Full license texts
The app contains the complete license texts. Open Mova's menu bar icon → Help & Feedback → Acknowledgements.
They're also included in the third-party source archive.
