# ChatLy

A native iOS messaging prototype covering the complete path from account creation to a real-time one-to-one conversation.

**Stage:** implemented prototype; public release not verified. **Source:** retained privately for portfolio presentation.

<img src="../assets/case-studies/chatly/login.png" alt="Original ChatLy login screen with empty email and password fields" width="270">

*Original application screenshot. The selected screen contains empty fields and no personal conversation or account data.*

## User workflow

A user registers with an email address and password, signs in, selects another user, and opens a conversation. The recent-conversation list exposes the latest message for quick return visits. Profile management includes photo upload and sign-out.

## Capabilities

- Email/password registration and authentication
- Real-time one-to-one message updates through Firestore
- User discovery and conversation initiation
- Recent conversations with last-message previews
- Profile-photo upload through Firebase Storage
- Loading feedback and meaningful authentication error alerts

## Engineering approach

Programmatic UIKit keeps screen layout in code. MVVM separates presentation state from controllers, while dedicated services wrap authentication, messaging, and storage. The project demonstrates asynchronous backend interaction across several connected screens rather than an isolated chat mockup.

## Technology

Swift, UIKit, MVVM, Firebase Authentication, Firestore, Firebase Storage, JGProgressHUD, and SDWebImage.

## Evidence and limits

The source README and existing screenshots document registration, login, conversation lists, messaging, and profile screens. The selected login image was visually reviewed for public presentation. Screens containing account identities or message content are excluded.

This prototype does not carry the local-first delivery architecture or end-to-end encryption claims of [Heey](heey.md). No store release, independent security audit, scale benchmark, or current device validation is claimed.
