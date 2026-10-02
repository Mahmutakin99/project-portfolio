# SoulMate

A private one-to-one iOS communication experience designed exclusively for two paired users.

## Problem

General-purpose messaging products are optimized for large contact lists and group communication rather than a focused, private space shared by a single pair.

## Solution

SoulMate combines paired-user access, local-first messaging, end-to-end encrypted payloads, read state, lightweight interactions, and a shared daily-notes calendar.

## Core capabilities

- Pair-restricted one-to-one messaging
- End-to-end encryption using ECDH, HKDF-SHA256, and AES-GCM
- Local-first message storage with GRDB/SQLite
- Sent, delivered, and read states
- Emoji reactions and heartbeat interaction
- Single-device session locking
- Shared day-based notes
- Firebase-backed delivery, acknowledgements, reactions, pairing, and push notifications

## Engineering approach

Programmatic UIKit presents local data first, while synchronization services manage queue, retry, acknowledgement, and read-state transitions. Cryptographic and persistence responsibilities are separated from interface code.

```mermaid
flowchart LR
    A[UIKit] --> B[Local GRDB store]
    B <--> C[Sync service]
    C <--> D[Firebase Realtime Database]
    D <--> E[Cloud Functions / Messaging]
```

## Technology

Swift, UIKit, GRDB/SQLite, CryptoKit, Firebase Auth, Realtime Database, Cloud Functions, Firebase Messaging, APNs, and SDWebImage.

## Security note

The application uses standard platform cryptographic primitives but has not been presented as independently security-audited. Source code and backend configuration remain private.

## Presentation limits

The case describes the application's development architecture. It does not assert an independent protocol audit, current store release, or measured delivery reliability. No verified screenshots with public-safe paired-user or conversation data were selected for this case.
