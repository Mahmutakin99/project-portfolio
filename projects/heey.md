# Heey

A local-first iOS messaging application designed around end-to-end encrypted delivery and device-owned message history.

## Problem

Many chat applications treat the cloud as the permanent source of truth, which increases network dependence and centralizes message history.

## Solution

Heey stores conversations and messages in a local GRDB/SQLite database first. Firebase acts as a temporary delivery queue: recipients decrypt and store incoming messages locally, acknowledge successful storage, and then remove the queued cloud item.

## Core capabilities

- Local-first conversation and message storage
- End-to-end encryption using P-256 ECDH, HKDF, and AES-GCM
- Temporary delivery queue with acknowledgement and retry behavior
- Delete-for-everyone tombstone flow
- Emoji reactions and paginated chat history
- Contact discovery using hashed phone identity matching
- APNs and Firebase Cloud Messaging notifications
- Turkish and English localization
- Profile and account management

## Engineering approach

Local SQLite tables are the source of truth for first paint and offline behavior. A materialized conversation index avoids expensive startup reconstruction, while incremental updates reduce full chat reloads.

```mermaid
flowchart LR
    A[Sender local store] --> B[Encrypt]
    B --> C[Temporary Firebase queue]
    C --> D[Recipient decrypts]
    D --> E[Recipient local store]
    E --> F[Acknowledge and remove queue item]
```

## Technology

Swift, UIKit, GRDB/SQLite, CryptoKit, Firebase Auth, Firestore, Storage, Cloud Functions, Firebase Messaging, APNs, Swift Package Manager, and Node.js 22.

## Security note

The application uses standard platform cryptographic primitives but has not been presented as independently security-audited. Source code and backend configuration remain private; an architecture walkthrough may be provided upon request.

