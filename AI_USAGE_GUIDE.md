# AI Usage Guide

This guide explains how AI tools should use this repository.

## Priority Order

1. Read `DATA_CATALOG.md` first to understand the corpus.
2. Prefer files in `normalized/` for search, summarization, and retrieval.
3. Use `metadata/` files to understand ownership, date, sensitivity, topic, and relationships.
4. Use `chunks/` for vector search and retrieval testing.
5. Use `source/` when original formatting, media inspection, citations, or verification are required.
6. Cite original source files from `source/`, not only derived files.

## Retrieval Guidance

- Use metadata fields such as `topics`, `media_type`, `sensitivity`, `created_date`, and `source_path` for filtering.
- Preserve source IDs when creating answers.
- If a chunk comes from a transcript, image description, OCR file, or table export, trace it back to the original source file.

## Multimodal Guidance

- For images: use `normalized/image_descriptions/` and `metadata/images/`.
- For scanned documents: use `normalized/ocr/`.
- For audio and video: use `normalized/transcripts/`.
- For spreadsheets: use `normalized/tables/` and associated data dictionaries.
