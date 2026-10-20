# Changelog

## 0.9.5 Beta — fill in and save forms (Mac)

**Forms**

- Fill in text fields, checkboxes, radio buttons and drop-down lists, then
  **File ▸ Save** (⌘S) or **File ▸ Save a Copy…** (⇧⌘S). The values are
  written into the PDF, so other PDF apps show them too; password-protected
  forms stay protected.
- Unsaved changes show in the title; closing, opening another PDF or quitting
  asks whether to save them.
- PDFs that do not allow filling in show read-only fields.
- The first time you open a fillable form, a short note explains that the
  assistant sees your values once you save (you can turn it off).

**Assistant**

- Reads form fields: ask about one field (_"What did I put as my last
  name?"_) or the whole form (_"What's still empty?"_, _"Is the form
  complete?"_). Answers link to the field and highlight it.
- After a save, only the changed fields are read again.

**Known limitations**

- Form scripts (calculated fields, checks) do not run; signature fields and
  XFA-only forms cannot be filled in.
- Still no printing.

## 0.9.4 Beta — Leafrune for Mac (Apple silicon)

Leafrune now runs on Macs with Apple silicon (M1 or later). Download the DMG
and follow the steps in the [README](README.md#macos).

**A Mac app**

- The toolbar sits in the title bar; the sidebar is translucent (solid with
  Reduce Transparency).
- Your accent and highlight colors from System Settings.
- The macOS menu bar, the system About panel (Leafrune ▸ About Leafrune) and
  Help ▸ Report a Problem….
- Find opens as a bar under the toolbar, as in Safari; password prompts open
  as a sheet.
- The window reopens at its last size and place.

**Assistant**

- Answers are written by Gemma 4 E2B (Google DeepMind) on the Mac's graphics
  processor.
- A **Report answer** button under each answer opens a filled-in report that
  you can check and edit before sending.
- The one-time AI model download is about 3.2 GB.

**Known limitations**

- Not notarized by Apple yet: macOS asks once (System Settings ▸ Privacy &
  Security ▸ Open Anyway).
- Intel Macs are not supported yet.
- Same as on Windows: no text recognition for scanned PDFs, no printing, form
  values are not saved, no annotations; the assistant works best with English
  documents.

## 0.9.2 Beta — first public beta (Windows)

The first public release of Leafrune: a private PDF reader with an AI assistant
that runs on your own computer. Download it from the
[README](README.md#download).

**Reading**

- Open PDFs from the Open… button, drag and drop, the Recent list, or by
  double-clicking them in File Explorer (one window; a second file opens in it).
- Reopens the last document, and every document where you left off.
- Zoom (Ctrl+wheel, touchpad pinch, presets, fit page / fit width) and rotate,
  remembered per document.
- Sidebar with the table of contents and page thumbnails.
- Back and forward through jumps (links, contents, search results, citations).
- Find with every match highlighted (Ctrl+F, F3 / Shift+F3).
- Password-protected PDFs; the password is never stored.
- Links open in your browser or mail app; Copy Page as Image.

**Assistant**

- Ask questions about the open PDF; answers cite the pages they come from, and
  a click highlights the passage.
- Overview, page count and "what does page N say" questions.
- Says so when the document does not cover a question.
- Shows its steps while it works; one conversation per document.
- Runs fully on your computer after a one-time download of two AI models
  (about 531 MB), which resumes after interruptions and is checked file by
  file.

**Windows**

- Windows 11 look: Segoe UI Variable, your accent color, Fluent icons, thin
  overlay scrollbars, light and dark themes (View ▸ Theme).
- Native menus with Alt access keys; Help ▸ About Leafrune.
- Opens centered at 80% of the screen; Full Screen with F11.
- Recent files in the taskbar Jump List.

**Known limitations**

- Not code-signed yet: Windows SmartScreen asks once (More info ▸ Run anyway).
- No text recognition for scanned PDFs, no printing, form values are not saved,
  no annotations.
- The assistant works best with English documents.
- macOS: coming soon.
