# Elerivo & Elerivo Junior

[Product portfolio](https://github.com/Mahmutakin99/project-portfolio) · [Feedback](https://github.com/Mahmutakin99/project-portfolio/issues/new/choose)

Two language-learning products being developed on a shared Flutter and Django foundation, with separate adult and junior applications.

**Stage:** engineering foundation completed; learning experience and live AI evaluation are pending. **Source:** private.

## Product problem

Adult and younger learners need different content, interactions, and commercial boundaries. Sharing infrastructure should not accidentally expose the junior product to adult-only dependencies or payment behavior.

## Work completed

The project establishes two independently buildable mobile applications, a shared foundation package, and a minimal Django backend in one monorepo. Development, staging, and production profiles are separated. Product and dependency policies are validated as structured contracts rather than being left as prose alone.

- Separate adult and junior Flutter shells for iOS and Android
- Shared package with explicit application profiles
- Backend environment validation and configuration checks
- Locked toolchains and reproducible bootstrap
- CI for policy validation, static analysis, tests, and mobile artifacts
- Artifact checksums and release preflight checks
- Synthetic writing-evaluation cases and an offline request preparation workflow
- Two-stage blind authoring and expert-review materials for educational content

## Engineering decisions

The junior profile prohibits payment, sponsor, and live scenario-generation dependencies at this stage. Dependency checks also inspect transitive workspace dependencies. The AI evaluation tooling prepares and validates requests without sending them to providers, keeping experiment preparation separate from live evaluation.

The educational-content workflow separates independent teacher authoring from review of drafts. Its capacity results remain pending until human authorship, review time, and rights are confirmed.

## Technology

Flutter, Dart, Python, Django, JSON Schema, YAML policy contracts, GitHub Actions, Android build flavors, and iOS schemes.

## Evidence and limits

The September 2026 project status records successful adult/junior Android debug and unsigned iOS simulator builds, CI jobs, checksum verification, and policy tests. These are recorded development results; they were not rerun for this presentation.

The current mobile applications are minimal branded shells. Lessons, learning navigation, production APIs, a validated AI feedback system, store distribution, and learning-outcome evidence are not represented as completed features. The case study has no verified product screenshots because those experiences have not yet been built.

## Availability

This is a development case study. Source, unpublished pedagogy contracts, provider configuration, and operational identifiers remain private.

## Feedback and content rights

Use the issue form for product questions or corrections. Remove personal information from screenshots and reports. This is a public product presentation; application source remains private.

[Content rights](NOTICE.md). Previously licensed assets retain their existing permissions.
