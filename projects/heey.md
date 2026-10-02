# Heey

<img src="../assets/case-studies/heey/icon.png" alt="Original Heey application icon" width="110">

A local-first iOS messaging application designed around end-to-end encrypted delivery and device-owned message history.

**Stage:** implemented application under development; store distribution not verified. **Source:** private.

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

## User workflow

A user creates an account, verifies a phone number, grants contact access, and starts a conversation with a matched contact. Outgoing messages enter local history before upload. The recipient decrypts and stores the message, then acknowledges delivery so the temporary queue entry can be removed. Failed uploads remain visible locally and can be retried.

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

## Evidence and limits

The repository README documents the local SQLite source of truth, materialized conversation index, encrypted delivery queue, acknowledgement flow, account gates, and retry behavior. Cryptographic primitives are an implementation description; forward secrecy, independent protocol assurance, and measured production reliability are not claimed.

The visual above is original application artwork. No verified screenshots with public-safe contacts or conversations were available. No current device run or delivery benchmark was performed for this presentation.
