# AI Reference Proof of Concept Repository

This repository contains a sample-ready structure for testing how AI tools can reference, retrieve, summarize, extract, and reason across multiple media types.

## Goals

- Test how AI tools reference different media types.
- Compare raw source files against normalized AI-readable derivatives.
- Evaluate retrieval accuracy using known questions and expected sources.
- Demonstrate metadata-driven search and filtering.
- Prepare for a future workplace implementation using sanitized or synthetic examples.

## Recommended Workflow

```text
Original file -> Normalized text/JSON -> Metadata -> Chunks -> Evaluation question
```

## Main Folder Layers

- `source/`: Original files exactly as collected.
- `normalized/`: AI-friendly text, Markdown, transcript, OCR, table, and image-description derivatives.
- `metadata/`: Sidecar metadata for every important file.
- `chunks/`: Retrieval-ready JSONL chunks.
- `evaluation/`: Test questions, expected answers, and retrieval scoring notes.

## Important Note

Do not place confidential workplace data in this proof of concept unless you have approval. Use synthetic, redacted, or sanitized examples where possible.
