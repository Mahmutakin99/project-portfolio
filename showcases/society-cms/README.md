# Physics & Astronomy Society CMS

[Product portfolio](https://github.com/Mahmutakin99/project-portfolio) · [Feedback](https://github.com/Mahmutakin99/project-portfolio/issues/new/choose)

A database-backed website and administration panel for publishing a student society's announcements, activities, and astronomy content.

**Stage:** implemented website and CMS; live deployment not verified. **Source:** private.

## Problem

A society needs to keep its public website current without asking a developer to edit page markup for every announcement, board change, or event.

## Workflow

An administrator signs in to a management dashboard, edits events or announcements, manages membership and board content, and updates site settings. Public pages present the resulting content through shared page templates.

## Capabilities

- Public home, events, announcements, board, and privacy-information pages
- Administration dashboard and member management
- Announcement and event publishing
- Astronomy-event management with expiry and cleanup behavior
- Board profiles, photos, and social links
- Administrative user, profile, and password management
- Login logs and configurable site settings
- Background-video upload with a star-animation fallback

## Engineering approach

PHP renders the public site and administrative surfaces from a MySQL data model. Common authentication and rendering helpers support the connected pages. Uploaded photos and video stay in the filesystem; structured records stay in the database.

The repository documents password hashing, CSRF tokens, output escaping, and server access restrictions as implementation measures. These are engineering details, not a claim of independent security certification.

## Technology

PHP, MySQL, HTML, CSS, JavaScript, and Apache configuration.

## Evidence and limits

The source inventory includes public pages, eleven administrative page types, a database schema, shared authentication helpers, and deployment notes. The January 2026 completion record describes implemented functionality while leaving domain, database, and HTTPS setup as deployment prerequisites.

No verified screenshots with sample data were available. Existing uploaded member imagery, organizational records, database settings, and deployment identifiers are excluded from this presentation. The source repository name is WebSiteDesign.

## Feedback and content rights

Use the issue form for product questions or corrections. Remove personal information from screenshots and reports. This is a public product presentation; application source remains private.

[Content rights](NOTICE.md). Previously licensed assets retain their existing permissions.
