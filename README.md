# OCR & Documents

> Extract text from images and scanned documents using Tesseract OCR with multi-language support and PDF handling.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/Marrowleaf/hermes-ocr-and-documents)

## Features

- Optical character recognition (OCR) from images and scanned PDFs
- Multi-language text extraction (English, CJK, European languages)
- PDF to text conversion with layout preservation
- Document pre-processing (deskew, denoise, threshold adjustment)
- Batch processing of multiple files
- Output to plain text, Markdown, or Obsidian notes
- Handwriting recognition support (limited accuracy)
- Table extraction from structured documents

## Installation

```bash
hermes skills install productivity/ocr-and-documents
```

Or manually clone into `~/.hermes/skills/productivity/ocr-and-documents/`.

## Usage

```
ocr extract /path/to/document.pdf
ocr extract /path/to/photo.jpg --language eng
ocr extract /path/to/folder/ --batch --output obsidian
ocr table /path/to/invoice.pdf
ocr preprocess /path/to/scan.png --deskew --denoise
```

## Configuration

- `TESSERACT_LANGUAGES`: Installed language packs (default: eng)
- Additional Tesseract language packs can be installed via `apt install tesseract-ocr-{lang}`
- Output directory for processed files configurable in `config.md`

## Requirements

- Hermes Agent v0.12+
- Tesseract OCR (`tesseract-ocr`)
- Poppler Utils (`poppler-utils` for PDF processing)
- ImageMagick (for pre-processing)

## License

MIT

## Related Hermes Skills
- [hermes-airtable](https://github.com/Marrowleaf/hermes-airtable) — Airtable integration and automation
- [hermes-budget-tracker](https://github.com/Marrowleaf/hermes-budget-tracker) — Personal budget tracking and analysis
- [hermes-consensus-engine](https://github.com/Marrowleaf/hermes-consensus-engine) — Multi-model consensus and decision engine
- [hermes-nano-pdf](https://github.com/Marrowleaf/hermes-nano-pdf) — Lightweight PDF processing and manipulation
- [hermes-notion](https://github.com/Marrowleaf/hermes-notion) — Notion integration and management
