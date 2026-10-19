# Compatibility

## Requirements
- **macOS 14 Sonoma or later**: 14, 15 Sequoia and 26 Tahoe.
- **Apple silicon or Intel:** one universal app, running natively on both.
- About 27 MB of disk space. Memory use is about 16 MB idle and 150–250 MB while converting a 12-megapixel photo. Batches adjust how many files run at once to your Mac's memory.
- **Design:** Liquid Glass on macOS 26 Tahoe. macOS 14 and 15 get the same layout with the system's translucent materials.

## What was tested for v0.1.0-beta
| Configuration | Status |
|---|---|
| macOS 26.3 on Apple silicon (native arm64) | ✅ Automated suite: 63 checks on the installed release build, covering conversions, Combine PDF, MP4→MP3, tools, editors, originals unchanged and no network. |
| Drag and Shift, live on the installed build | ✅ Photo → PNG, MP4 → MP3, PDF → ⇧⇧ → Rotate, three files → Combine PDF; originals unchanged. Drop targets for every menu size are also checked automatically. |
| Intel build (x86_64) on macOS 26.3 under Rosetta 2 | ✅ HEIC→JPG/WEBP, video→MP3, DOCX→PDF, Combine PDF |
| macOS 14 Sonoma / macOS 15 Sequoia | ⚠️ Built for and expected to work, not yet run on these versions |
| A physical Intel Mac | ⚠️ Not yet tested on real Intel hardware |

## Features that depend on your Mac
- **HEIC and AVIF output** use macOS's own encoders. If your Mac or macOS version can't write a format, Mova hides that bubble rather than failing.
- **Text recognition** in scanned PDFs, and Find Text / Find Faces in Redact, use Apple's Vision framework, available on all supported Macs.
- Everything else, including MP3, M4A, WAV and WEBP via the bundled FFmpeg, works the same on every supported Mac.

## Not supported
- macOS 13 Ventura and earlier.
- Drags that carry no real file, such as photos dragged straight out of Photos or some browser and mail attachments. Save the file first, or use **Open Files…**.

Found a compatibility problem? [Report it](https://github.com/matthewap2007-cell/mova/issues/new/choose), including the text from **Copy Diagnostics** (menu bar icon → Help & Feedback).
