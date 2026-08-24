# SmartDoc Query

An iOS document assistant that lets users import PDF files, ask questions about their content, and inspect the source pages behind each answer.

## Problem

Long or scanned documents are difficult to search with exact keywords, and cloud-based document assistants can introduce privacy concerns when sensitive files leave the device.

## Solution

SmartDoc Query processes documents into searchable text chunks, retrieves relevant context with semantic search, and produces grounded answers. Its local mode keeps PDF processing, embeddings, retrieval, and answer generation on the device. An optional strong mode can send only selected context through a configured Firebase Functions proxy for more complex requests.

## Core capabilities

- PDF import and text extraction with Vision OCR fallback for scanned pages
- Semantic chunking, Core ML embeddings, vector search, and reranking
- On-device answer paths using BERT, Apple frameworks, and a managed Qwen 2.5 model through `llama.cpp`
- Page-level citations with in-document highlighting
- Voice questions and spoken answers
- Per-document chat history and multi-document library management
- Keychain-backed storage for user-provided API configuration

## Engineering approach

The application follows MVVM with programmatic UIKit and a container-based navigation structure. PDF processing, embeddings, retrieval, answer orchestration, speech, and persistence are separated into focused services so local and optional cloud-assisted answer paths can share the same document pipeline.

```mermaid
flowchart LR
    A[PDF] --> B[PDFKit / Vision OCR]
    B --> C[Semantic chunks]
    C --> D[Core ML embeddings]
    D --> E[Vector retrieval]
    E --> F[Grounded answer]
    F --> G[Page citation and highlight]
```

## Technology

Swift, UIKit, MVVM, PDFKit, Vision, Core ML, Natural Language, Speech, AVFoundation, SQLite, Keychain, Firebase Functions, and `llama.cpp`.

## Privacy and availability

Local mode is designed to process document content on the device. Source code is private; a product walkthrough or controlled review may be provided upon request.

