<p align="center">
  <img src="assets/logo/leafrune-256.png" alt="Leafrune logo" width="128" height="128">
</p>

<h1 align="center">Leafrune</h1>

<p align="center">
  <strong>A fast, private PDF reader with an AI assistant that runs on your own computer.</strong>
</p>

<p align="center">
  <a href="https://github.com/Sheldon1999/leafrune/releases/download/v0.9.5/Leafrune_0.9.5_aarch64.dmg"><strong>Download for Mac</strong></a>
  ·
  <a href="https://apps.microsoft.com/detail/9pd85b3k3t39"><strong>Get it for Windows</strong></a>
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

| System                             | Download                                                                                                                                   |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| macOS (Apple silicon: M1 or later) | **[Leafrune_0.9.5_aarch64.dmg](https://github.com/Sheldon1999/leafrune/releases/download/v0.9.5/Leafrune_0.9.5_aarch64.dmg)** (0.9.5 Beta) |
| Windows 10 / 11 (64-bit)           | **[Microsoft Store](https://apps.microsoft.com/detail/9pd85b3k3t39)** (0.9.5 Beta)                                                         |

Every Mac download is listed on the [Releases](https://github.com/Sheldon1999/leafrune/releases)
page. To check that the DMG is complete and unchanged, compare its SHA-256 with
the release's `SHA256SUMS.txt`. In Terminal:

```sh
shasum -a 256 ~/Downloads/Leafrune_0.9.5_aarch64.dmg
```

## Installing

### macOS

1. Open `Leafrune_0.9.5_aarch64.dmg` from your Downloads folder.
2. In the window that appears, drag **Leafrune** onto the **Applications**
   folder.
3. Eject the Leafrune disk (the eject button next to it in the Finder
   sidebar).
4. Open **Leafrune** from your Applications folder.

The beta is **not notarized by Apple yet**, so the first time macOS says it
cannot verify Leafrune and does not open it. This is expected; allow it once:

5. Click **Done** in that message.
6. Open **System Settings ▸ Privacy & Security** and scroll down to
   **Security**. Next to the message that Leafrune was blocked, click
   **Open Anyway**.
7. Click **Open Anyway** again and enter your password. Leafrune opens, and
   from now on it opens normally.

Leafrune can become your default PDF app: select any PDF in Finder, choose
**File ▸ Get Info**, set **Open with** to **Leafrune**, then click
**Change All…** to use it for every PDF.

### Windows

1. Open [Leafrune in the Microsoft Store](https://apps.microsoft.com/detail/9pd85b3k3t39)
   and click **Get** (or **Install**).
2. Open **Leafrune** from the Start menu. The Store keeps it up to date.

Leafrune can become your default PDF app: right-click any PDF ▸ **Open with** ▸
**Choose another app** ▸ **Leafrune** ▸ **Always**.

## First launch

- Leafrune opens straight away and you can start reading.
- In the background it downloads its two AI models once from Hugging Face
  (**about 3.2 GB**). Nothing is shown unless you open the assistant, where
  you can follow the progress.
- The first time you open the assistant, the computer prepares its graphics
  processor for it. On a Mac this takes about 20 seconds, once.
- A dropped connection is no problem: the download continues where it stopped,
  even after a restart, and every file is checked before use.
- After that, Leafrune never needs the internet again.

## What Leafrune can do

**Reading**

- Open PDFs from the **Open…** button, by dragging them onto the window, from
  the **Recent** list, or by double-clicking them in Finder or File Explorer.
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

**Forms**

- Fill in text fields, checkboxes, radio buttons and drop-down lists.
- **Save** (Ctrl+S, ⌘S on a Mac) writes the values into the same PDF; **Save
  a Copy…** (Ctrl+Shift+S, ⇧⌘S) writes them to a new file and leaves the
  original as it was. Other PDF apps show the saved values.
- Unsaved changes show in the title. Closing, opening another PDF or quitting
  asks whether to save them.
- PDFs that do not allow filling in show their fields read-only.

**Printing**

- The **Print** button, **File ▸ Print…** or Ctrl+P (⌘P on a Mac) open
  Leafrune's Print window: printer or **Save as PDF**, copies, two-sided,
  grayscale, page ranges (all, current, "1-3, 6", odd or even, reversed).
- **Page Sizing & Handling** like Acrobat: fit, actual size or a custom scale;
  **Poster** (one page across several sheets); **Multiple** pages per sheet;
  **Booklet**.
- A preview of every sheet. Filled-in form fields print, and pages print in
  normal colors even with Invert on.
- Leafrune remembers your choices for next time (except pages and copies).

**Comfort**

- **Invert colors** for reading at night (pages only).
- **Light, Dark or system theme**: View ▸ Theme.
- **Full screen** with F11 (⌃⌘F on a Mac).
- On a Mac: the toolbar in the title bar, a translucent sidebar, your accent
  color and the macOS menu bar.
- On Windows: native menus with keyboard access (Alt), and your recent files
  when you right-click Leafrune on the taskbar.

## The assistant

Open it with the chat button in the toolbar, **⌘/** on a Mac, **Ctrl+/** on
Windows, or View ▸ Assistant.

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
- **It reads filled-in forms.** Ask _"What did I put as my last name?"_ or
  _"What's still empty?"_; the answer links to the field. It sees the values
  you have saved, so save after filling in.

When you open a PDF for the first time, Leafrune reads its text in the
background (a long book takes a minute or two). You can keep reading meanwhile;
the next time, the assistant is ready at once.

> The assistant uses a small AI model so it can run on an ordinary laptop. Its
> answers can be incomplete or wrong. **Check the cited pages** before you rely
> on an answer.

## Keyboard shortcuts

The table lists the Windows shortcuts. On a Mac, most use ⌘ instead of Ctrl,
and the menus show every shortcut.

| Action                           | Shortcut                                |
| -------------------------------- | --------------------------------------- |
| Open a PDF                       | Ctrl+O                                  |
| Save / save a copy               | Ctrl+S / Ctrl+Shift+S                   |
| Print                            | Ctrl+P                                  |
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

|        | macOS                                 | Windows                                  |
| ------ | ------------------------------------- | ---------------------------------------- |
| System | Mac with Apple silicon (M1 or later)  | Windows 10 or 11, 64-bit (x64) with AVX2 |
| Disk   | about 3.5 GB free (app and AI models) | about 3.5 GB free (app and AI models)    |
| Memory | 8 GB recommended                      | 8 GB recommended                         |

- Reading needs no more than an ordinary PDF viewer.
- While the assistant answers, Leafrune uses more memory (about 2 GB on a
  Mac); it frees it again two minutes after your last question.
- On a Mac the assistant runs on the built-in graphics processor. On Windows
  it uses the graphics card when its driver supports Vulkan (NVIDIA, AMD,
  Intel), and otherwise the processor (no graphics card needed).

## Privacy

- Everything happens on your computer: reading, searching, and the assistant's
  answers.
- The only network use is the one-time AI model download from Hugging Face.
- No telemetry, analytics, crash reports, accounts or ads.
- Your PDFs are never copied, and changed only when you save a form in them.

Details, and how to delete everything Leafrune stores, are in
[PRIVACY.md](PRIVACY.md).

## Known limitations

- **Scanned PDFs** (pages that are only images) can be read, but the assistant
  cannot answer questions about them: there is no text recognition (OCR) yet.
- **The assistant works best in English.** Its search model was trained mainly
  on English text.
- **Forms** that run their own scripts (calculated totals, checks) are filled
  in without them, signature fields are not supported, and XFA forms can only
  be viewed.
- **No annotations** (highlights, notes) yet.
- **Mac:** Intel Macs are not supported yet. The beta is tested on macOS 27.
- **Linux** is not supported in the beta.

## Feedback

Leafrune is in beta, and your reports shape it.

- **Something broken?** Open an [issue](https://github.com/Sheldon1999/leafrune/issues/new/choose)
  with your macOS or Windows version, the Leafrune version (**Leafrune ▸ About
  Leafrune** on a Mac, **Help ▸ About Leafrune** on Windows) and the steps to
  see it.
- **A wrong or odd answer?** Report it with the question, the answer and the
  page it should have used.
- **Ideas** are welcome as issues too.

**Issues are public.** Do not attach confidential PDFs or paste private text;
a public-domain or self-made PDF that shows the problem is ideal.

Security problems: please follow [SECURITY.md](SECURITY.md) instead of opening
an issue.

## Uninstalling

- **Mac:** quit Leafrune, then drag it from your Applications folder to the
  Trash.
- **Windows:** Settings ▸ Apps ▸ Installed apps ▸ Leafrune ▸ Uninstall.

To also remove your recent files, reading positions, conversations and the AI
models, delete Leafrune's data folder as described in
[PRIVACY.md](PRIVACY.md#what-is-stored-on-your-computer).

## License

Leafrune is free to use on any number of your own devices, for personal and
professional use. The beta is closed source; the source code is planned to be
published under an open-source license with version 2.0. See
[LICENSE.md](LICENSE.md).

Leafrune is built on open-source software and openly licensed AI models:
Gemma 4 E2B by Google DeepMind and snowflake-arctic-embed-s by Snowflake.
Thank you to their authors. Credits and licenses:
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and
[THIRD_PARTY_LICENSES.txt](THIRD_PARTY_LICENSES.txt) (for the current version),
also in the app under Help ▸ Open-Source Software.
