# Third-party notices

Leafrune is built on the open-source software and openly licensed AI models
below. Thank you to their authors.

- This file lists the main components and the AI models.
- [THIRD_PARTY_LICENSES.txt](THIRD_PARTY_LICENSES.txt) contains the full
  license texts and copyright notices of every component (656 of them).

## AI models

The models are **not included in the installer**. Leafrune downloads them once,
on first launch, from Hugging Face, at the exact revisions listed here, and
checks each file's SHA-256 hash.

| Model                                                                                 | Used for                                    | Author          | File used                                                                                                                                                     | License                                                                 |
| ------------------------------------------------------------------------------------- | ------------------------------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| [Gemma 4 E2B](https://huggingface.co/google/gemma-4-E2B-it)                           | Writing answers                             | Google DeepMind | [unsloth/gemma-4-E2B-it-GGUF](https://huggingface.co/unsloth/gemma-4-E2B-it-GGUF) `gemma-4-E2B-it-Q4_K_M.gguf`, revision `0314792d` (quantization by Unsloth) | [Apache-2.0](https://huggingface.co/google/gemma-4-E2B-it)              |
| [snowflake-arctic-embed-s](https://huggingface.co/Snowflake/snowflake-arctic-embed-s) | Finding the passages that answer a question | Snowflake       | [Snowflake/snowflake-arctic-embed-s](https://huggingface.co/Snowflake/snowflake-arctic-embed-s) `onnx/model.onnx` and `tokenizer.json`, revision `e596f507`   | [Apache-2.0](https://huggingface.co/Snowflake/snowflake-arctic-embed-s) |

Leafrune does not modify the models. Answers generated with them are produced
on your device and are not reviewed by the model authors.

## Main software components

| Component                                                   | Version                | License                | Source                                                                           |
| ----------------------------------------------------------- | ---------------------- | ---------------------- | -------------------------------------------------------------------------------- |
| Tauri (app framework), wry, tao                             | 2.12.3, 0.57.0, 0.37.1 | Apache-2.0 / MIT       | https://github.com/tauri-apps/tauri                                              |
| Tauri plugins: dialog, single-instance, opener              | 2.8.2, 2.5.3, 2.7.1    | Apache-2.0 / MIT       | https://github.com/tauri-apps/plugins-workspace                                  |
| PDF.js (PDF rendering, text layer, find)                    | 6.3.289                | Apache-2.0             | https://github.com/mozilla/pdf.js                                                |
| Svelte (user interface runtime)                             | 5.57.1                 | MIT                    | https://github.com/sveltejs/svelte                                               |
| llama.cpp / ggml (runs the language model), via llama-cpp-2 | crate 0.1.157          | MIT                    | https://github.com/ggml-org/llama.cpp, https://github.com/utilityai/llama-cpp-rs |
| tract (runs the embedding model)                            | 0.23.8                 | Apache-2.0 / MIT       | https://github.com/sonos/tract                                                   |
| Hugging Face tokenizers                                     | 0.23.2                 | Apache-2.0             | https://github.com/huggingface/tokenizers                                        |
| SQLite (bundled via rusqlite)                               | 3.53.2                 | Public domain          | https://sqlite.org                                                               |
| rusqlite                                                    | 0.40.2                 | MIT                    | https://github.com/rusqlite/rusqlite                                             |
| sqlite-vec (vector search)                                  | 0.1.9                  | Apache-2.0 / MIT       | https://github.com/asg017/sqlite-vec                                             |
| mimalloc (memory allocator)                                 | 0.1.52                 | MIT                    | https://github.com/microsoft/mimalloc                                            |
| reqwest, rustls (model download over HTTPS)                 | 0.13.5, 0.23.37        | Apache-2.0 / ISC / MIT | https://github.com/seanmonstar/reqwest, https://github.com/rustls/rustls         |
| Fluent UI System Icons (Windows user-interface icons)       | 1.1.343                | MIT                    | https://github.com/microsoft/fluentui-system-icons                               |
| Phosphor Icons (macOS user-interface icons)                 | 2.1.1                  | MIT                    | https://github.com/phosphor-icons/core                                           |

## Files bundled with PDF.js

| Files                                          | License                                    | Notes                                                                                                                                                       |
| ---------------------------------------------- | ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Foxit standard fonts (`Foxit*.pfb`)            | BSD-3-Clause (PDFium)                      | Used to draw the 14 standard PDF fonts                                                                                                                      |
| Liberation Sans fonts (`LiberationSans-*.ttf`) | GPL-2.0 with the Liberation font exception | Unmodified. The font files are their own source; the font is used only to display documents, and the exception keeps documents and the app outside the GPL. |
| Character maps (`cmaps/*.bcmap`)               | BSD-3-Clause (Adobe)                       | For Chinese, Japanese and Korean text                                                                                                                       |
| ICC colour profile                             | CC0-1.0                                    |                                                                                                                                                             |
| JBIG2 decoder (WebAssembly)                    | BSD-3-Clause (PDFium) / Apache-2.0         | Scanned-image decoding                                                                                                                                      |
| OpenJPEG decoder (WebAssembly)                 | BSD-2-Clause                               | JPEG 2000 images                                                                                                                                            |
| qcms (WebAssembly)                             | MIT                                        | Colour management                                                                                                                                           |

## MPL-2.0 components

These components are used **unmodified**. Their source code is available from
the links below, as MPL-2.0 requires:

| Component                   | Version       | Source                                  |
| --------------------------- | ------------- | --------------------------------------- |
| cssparser, cssparser-macros | 0.36.0, 0.6.1 | https://github.com/servo/rust-cssparser |
| selectors                   | 0.36.1        | https://github.com/servo/stylo          |
| dtoa-short                  | 0.3.5         | https://github.com/upsuper/dtoa-short   |
| option-ext                  | 0.2.0         | https://github.com/soc/option-ext       |

`r-efi` is offered under MIT, Apache-2.0 or LGPL-2.1-or-later; Leafrune uses
it under MIT / Apache-2.0.

## Leafrune's own assets

The Leafrune name, logo and user-interface icons (except the Fluent UI System
Icons used on Windows and the Phosphor Icons used on macOS, listed above) are
original work by the Leafrune author and are not third-party material.
