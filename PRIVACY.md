# Privacy

**Short version: Mova doesn't collect, send or share anything. Your files never leave your Mac.**

## What Mova does with your files
- It reads only the files you drop on it, or choose with *Open Files…*.
- It writes results next to the originals, or to Downloads or Desktop if you choose that under *Save Results To*.
- It never changes, moves or deletes your originals, and never replaces an existing file.
- Temporary working files are kept in macOS's private temporary folder. They're deleted as soon as each job finishes, and again when Mova quits.

## Network
- Mova makes **no network connections** of its own: no analytics, crash reporting, update checks, ads or accounts.
- The bundled FFmpeg helper is built **without network support**; it can only read and write local files.
- HTML documents are imported with all remote images, stylesheets, scripts and frames removed first, so converting a web page never contacts a server.
- Your web browser opens only when you choose *Report a Bug…*, *Mova on GitHub* or *Show in Maps* (for a photo's location in the Info tool). Report a Bug fills in your Mova version, macOS version, Mac type and settings, and nothing is sent unless you submit the form.

## Text and face recognition
*Find Text* and *Find Faces* (in Redact) and text recognition for scanned PDFs use Apple's Vision framework, **on your Mac**.

## What's stored on your Mac
Mova keeps its settings in macOS's standard preferences:
- the trigger key, where results are saved, and the sound and batch-folder options;
- the paths of your last 10 results, for the *Recent Results* menu.

Clear the list with *Recent Results → Clear Recent Results*, or delete the preferences file
`~/Library/Preferences/io.github.matthewap2007-cell.Mova.plist`.

## macOS permissions
- **Files & Folders.** The first time you convert a file in Desktop, Documents or Downloads, macOS asks whether Mova may open files there. You can change this anytime in System Settings → Privacy & Security → Files & Folders.
- Mova does **not** need Accessibility, Input Monitoring, Screen Recording, Camera, Microphone, Contacts or Location access. It notices file drags without watching your keyboard or screen.

## Contact
Questions about privacy: [open an issue](https://github.com/matthewap2007-cell/mova/issues).
