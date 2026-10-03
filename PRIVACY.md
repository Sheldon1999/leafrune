# Privacy

**Short version:** Leafrune reads your PDFs and answers your questions on your
own computer. Nothing about your documents, questions or usage is sent
anywhere.

## What goes over the network

Leafrune connects to the internet for one thing only: **downloading its AI
models** from Hugging Face (`huggingface.co`). This happens on first launch,
and again only if an update changes a model.

- The download fetches fixed files at fixed revisions (see
  [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)) and checks their SHA-256
  hashes. It sends no information about you or your documents; Hugging Face
  sees an ordinary file download from your IP address.
- Leafrune uses your system's proxy settings.
- After the models are downloaded, Leafrune works fully offline.

There is **no telemetry, no analytics, no crash reporting, no account and no
advertising.**

## What is stored on your computer

Leafrune keeps its data in its application-data folder:

- macOS: `~/Library/Application Support/com.leafrune.reader`
- Windows: `%APPDATA%\com.leafrune.reader` (the window's web-view cache is in
  `%LOCALAPPDATA%\com.leafrune.reader`)

| Data                                                                                                                                 | Why                                                                               | How to remove                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| AI model files (`models/`, about 531 MB)                                                                                             | To answer questions offline                                                       | Delete the folder; they download again when needed              |
| Recent files: file paths and when you opened them                                                                                    | The start screen list                                                             | Remove entries from the list, or delete the database            |
| Reading position per document                                                                                                        | Reopen where you left off                                                         | Delete the database                                             |
| A fingerprint (SHA-256) of each opened PDF, its page count, its text split into passages, and a numeric "meaning" vector per passage | To find the passages that answer a question, without re-reading the PDF each time | Delete the database                                             |
| Your questions and the assistant's answers, per document                                                                             | Your conversation history                                                         | The trash button in the assistant panel, or delete the database |
| Settings (for example Invert colors, panel widths)                                                                                   | To remember your preferences                                                      | Delete the database                                             |

- The database is a single file, `library.db`.
- If it is ever found damaged, Leafrune sets it aside as
  `library.db.broken-<time>` and starts a new one; you can delete the old copy.
- **Your PDF files are not copied or modified.**
- **Passwords of protected PDFs are never stored.**

To remove all Leafrune data, quit the app and delete its application-data
folder.

## AI answers

Answers are generated locally by the models listed in
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). Your documents are not used
to train any model.

## When you report a problem

Issues you open in this repository are public. Do not attach confidential PDFs
or paste private text into an issue. For security problems, follow
[SECURITY.md](SECURITY.md).
