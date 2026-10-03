<p align="center">
  <img src="assets/logo/leafrune-256.png" alt="Leafrune logo" width="128" height="128">
</p>

<h1 align="center">Leafrune</h1>

<p align="center">
  <strong>A fast, private PDF reader with an AI assistant that runs on your own computer.</strong>
</p>

<p align="center">
  <a href="download/Leafrune_0.9.2_x64-setup.exe"><strong>Download for Windows</strong></a>
  ·
  macOS coming soon
  ·
  <a href="CHANGELOG.md">What's new</a>
  ·
  <a href="https://github.com/Sheldon1999/leafrune/issues/new/choose">Report a problem</a>
</p>

Read any PDF, then ask it questions: _"What is this document about?"_, _"What
does section 3 say about pricing?"_, _"What's on the last page?"_. Every answer
links to the pages it comes from. Click a link and Leafrune scrolls there and
highlights the sentence.

Your documents never leave your computer. There is no account, no cloud, no
telemetry. After a one-time model download, Leafrune works fully offline.

> **Beta.** Leafrune 0.9 is free to use and still being polished. Please
> [report anything that looks wrong](#feedback); that is how the beta gets
> better.

<!-- Screenshots go here: start screen, reading with the sidebar, the assistant
     answering with page links, a highlighted citation, Invert colors, Find. -->

---

## Contents

- [Download](#download)
- [Installing](#installing)
- [First launch](#first-launch)
- [What Leafrune can do](#what-leafrune-can-do)
- [The assistant](#the-assistant)
- [Keyboard shortcuts](#keyboard-shortcuts)
- [System requirements](#system-requirements)
- [Privacy](#privacy)
- [Known limitations](#known-limitations)
- [Feedback](#feedback)
- [Uninstalling](#uninstalling)
- [License](#license)

---

## Download

| System                   | Download                                                                                        |
| ------------------------ | ----------------------------------------------------------------------------------------------- |
| Windows 10 / 11 (64-bit) | **[Leafrune_0.9.2_x64-setup.exe](download/Leafrune_0.9.2_x64-setup.exe)** (Leafrune 0.9.2 Beta) |
| macOS (Apple Silicon)    | **Coming soon**                                                                                 |

To check that your download is complete and unchanged, compare its SHA-256
with [download/SHA256SUMS.txt](download/SHA256SUMS.txt). In PowerShell:

```powershell
Get-FileHash .\Leafrune_0.9.2_x64-setup.exe -Algorithm SHA256
```

## Installing

The beta installer is **not code-signed yet**, so Windows will warn you the
first time. This is expected.

### Windows

1. Run `Leafrune_0.9.2_x64-setup.exe`.
2. If Windows shows **"Windows protected your PC"**, click **More info**, then
   **Run anyway**.
3. Follow the installer. If your PC does not have Microsoft Edge WebView2 (most
   Windows 10 and all Windows 11 PCs already do), the installer downloads it,
   so keep the internet connected during setup.

Leafrune can become your default PDF app: right-click any PDF ▸ **Open with** ▸
**Choose another app** ▸ **Leafrune** ▸ **Always**.

### macOS

Coming soon. Watch this repository (**Watch ▸ Custom ▸ Releases**) to hear
when the Mac version is out.

## First launch

- Leafrune opens straight away and you can start reading.
- In the background it downloads its two AI models once (**about 531 MB**)
  from Hugging Face. Nothing is shown unless you open the assistant, where you
  can follow the progress.
- A dropped connection is no problem: the download continues where it stopped,
  even after a restart, and every file is checked before use.
- After that, Leafrune never needs the internet again.

## What Leafrune can do

**Reading**

- Open PDFs from the **Open…** button, by dragging them onto the window, from
  the **Recent** list, or by double-clicking them in File Explorer.
- Leafrune remembers where you were in every document and reopens the last one
  where you left off.
- Zoom, fit to page or width, Ctrl+mouse wheel and touchpad pinch.
- Rotate sideways pages; the rotation is remembered per document.
- **Sidebar** with the table of contents and page thumbnails.
- **Back and Forward** through your jumps (links, contents, search results,
  citations), like a web browser.
- **Find** in the document, with every match highlighted.
- **Password-protected PDFs** (the password is never stored).
- Links in a PDF open in your web browser or mail app.
- Copy text, or right-click a page to **Copy Page as Image**.

**Comfort**

- **Invert colors** for reading at night (pages only).
- **Light, Dark or system theme**: View ▸ Theme.
- **Full screen** with F11.
- Native Windows menus with keyboard access (Alt), and your recent files when
  you right-click Leafrune on the taskbar.

## The assistant

Open it with the chat button in the toolbar, **Ctrl+/** or
View ▸ Assistant.

- **Ask in your own words.** The assistant finds the passages that answer
  your question and writes a short answer from them.
- **Every answer cites its pages.** Click a page link and Leafrune jumps there
  and highlights the passage.
- **It also knows the whole document.** _"What is this about?"_ gets an
  overview; _"How many pages?"_ and _"What does page 12 say?"_ work too.
- **It says when it does not know.** If the document does not cover your
  question, it tells you instead of guessing.
- **It shows what it is doing**: loading the model, searching, reading passages.
- **Each document keeps its own conversation.** Copy an answer with the copy
  button; clear the conversation with the trash button.

When you open a PDF for the first time, Leafrune reads its text in the
background (a long book takes a minute or two). You can keep reading meanwhile;
the next time, the assistant is ready at once.

> The assistant uses a small AI model so it can run on an ordinary laptop. Its
> answers can be incomplete or wrong. **Check the cited pages** before you rely
> on an answer.

## Keyboard shortcuts

| Action                           | Shortcut                                |
| -------------------------------- | --------------------------------------- |
| Open a PDF                       | Ctrl+O                                  |
| Reload / close the document      | Ctrl+R / Ctrl+W                         |
| Find                             | Ctrl+F                                  |
| Next / previous match            | Ctrl+G / Ctrl+Shift+G, or F3 / Shift+F3 |
| Go to page                       | Ctrl+L                                  |
| Next / previous page             | N / P                                   |
| First / last page                | Ctrl+Home / Ctrl+End                    |
| Back / forward                   | Alt+← / Alt+→                           |
| Zoom in / out / automatic        | Ctrl+= / Ctrl+- / Ctrl+0                |
| Fit page / fit width / automatic | F / W / A                               |
| Rotate left / right              | Ctrl+← / Ctrl+→                         |
| Sidebar                          | F9                                      |
| Invert colors                    | Ctrl+I                                  |
| Assistant                        | Ctrl+/                                  |
| Full screen                      | F11                                     |

## System requirements

|        | Windows                             |
| ------ | ----------------------------------- |
| System | Windows 10 or 11, 64-bit (x64)      |
| Disk   | about 1 GB free (app and AI models) |
| Memory | 8 GB recommended                    |

The macOS version (Apple Silicon) is coming soon.

- Reading needs no more than an ordinary PDF viewer.
- While the assistant answers, Leafrune uses about 1 GB more memory; it frees
  it again two minutes after your last question.
- The assistant runs on the processor (no graphics card needed).

## Privacy

- Everything happens on your computer: reading, searching, and the assistant's
  answers.
- The only network use is the one-time AI model download from Hugging Face.
- No telemetry, analytics, crash reports, accounts or ads.
- Your PDFs are never copied or modified.

Details, and how to delete everything Leafrune stores, are in
[PRIVACY.md](PRIVACY.md).

## Known limitations

- **Scanned PDFs** (pages that are only images) can be read, but the assistant
  cannot answer questions about them: there is no text recognition (OCR) yet.
- **The assistant works best in English.** Its search model was trained mainly
  on English text.
- **Printing** is not available yet.
- **Forms:** you can type into form fields, but the values are not saved yet.
- **No annotations** (highlights, notes) yet.
- **Windows only for now:** the macOS version is coming soon; Linux is not
  supported in the beta.

## Feedback

Leafrune is in beta, and your reports shape it.

- **Something broken?** Open an [issue](https://github.com/Sheldon1999/leafrune/issues/new/choose)
  with your Windows version, the Leafrune version (Help ▸ About Leafrune) and
  the steps to see it.
- **A wrong or odd answer?** Report it with the question, the answer and the
  page it should have used.
- **Ideas** are welcome as issues too.

**Issues are public.** Do not attach confidential PDFs or paste private text;
a public-domain or self-made PDF that shows the problem is ideal.

Security problems: please follow [SECURITY.md](SECURITY.md) instead of opening
an issue.

## Uninstalling

- **Windows:** Settings ▸ Apps ▸ Installed apps ▸ Leafrune ▸ Uninstall.

To also remove your recent files, reading positions, conversations and the AI
models, delete Leafrune's data folder as described in
[PRIVACY.md](PRIVACY.md#what-is-stored-on-your-computer).

## License

Leafrune is free to use on any number of your own devices, for personal and
professional use. The beta is closed source; the source code is planned to be
published under an open-source license with version 2.0. See
[LICENSE.md](LICENSE.md).

Leafrune is built on open-source software and openly licensed AI models
(Qwen3-0.6B by the Qwen team, Alibaba Cloud; snowflake-arctic-embed-s by Snowflake). Thank you
to their authors. Credits and licenses: [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)
and [THIRD_PARTY_LICENSES.txt](THIRD_PARTY_LICENSES.txt), also in the app
under Help ▸ Open-Source Software.
