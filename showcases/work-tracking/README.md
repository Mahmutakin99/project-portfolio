# ASO Work Tracking System

[Product portfolio](https://github.com/Mahmutakin99/project-portfolio) · [Feedback](https://github.com/Mahmutakin99/project-portfolio/issues/new/choose)

An internal project and task management platform developed during an Information Technology internship at the ASO 1st Organized Industrial Zone Directorate.

## Context

The IT & Communications Directorate needed a centralized workflow for work that had been distributed across spreadsheets, messaging, and third-party task tools.

## Contribution

Designed and developed a full-stack internal platform at the department manager's request, covering project setup, task assignment, personal work queues, managerial visibility, reporting, and controlled on-premises deployment.

## Core capabilities

- Personal task workspace with optimistic completion and undo
- Project list, Kanban, and calendar views
- Drag-and-drop task ordering and multi-criteria filtering
- Turkish full-text search and keyboard command palette
- Task details with assignees, labels, checklists, subtasks, custom fields, comments, attachments, and activity history
- Notifications for assignments, mentions, upcoming deadlines, and overdue work
- Manager dashboard with workload, project status, overdue work, and budget summaries
- Individual and bulk user administration through CSV/XLSX import
- CSV exports for project, personal, and dashboard views
- Project templates, scheduled summaries, and stale-task automation

## Engineering approach

The application uses Laravel and Inertia to keep authorization, validation, and domain workflows on the server while delivering a React/TypeScript interface. PostgreSQL row-level security provides database-level tenant isolation, and the production stack is prepared for Docker-based on-premises deployment.

```mermaid
flowchart LR
    A[React / TypeScript] --> B[Inertia.js]
    B --> C[Laravel application]
    C --> D[Policies, actions, queries, services]
    D --> E[PostgreSQL with RLS]
    C --> F[Queue, notifications, file storage]
```

## Technology

PHP, Laravel 13, Inertia.js 3, React 19, TypeScript, Tailwind CSS 4, PostgreSQL 17, Laravel Fortify, Docker, Pest, Vitest, PHPStan, ESLint, and TypeScript strict mode.

## Quality and security

- The development record reports 714 backend tests (704 passed, 10 skipped) and 163 frontend tests. These recorded results were not rerun for this presentation.
- PHPStan level 7 and TypeScript strict mode were used as quality gates.
- Database isolation, authorization policies, upload validation, append-only activity history, security headers, and dependency audits were included in the production-readiness work.

## Workflow and status

An authorized user creates a project and task, assigns colleagues, adds detail and supporting files, and tracks progress from a personal queue or Kanban board. Managers inspect workload and overdue work, while administrators manage users and templates. Reports and reminders support follow-up outside the task screen.

The repository documents a working internal application with browser validation and an on-premises deployment approach. This presentation does not establish a live institutional deployment, independent security audit, or current build result. Email-to-task support is documented as a provider-agnostic interface whose external provider was not yet connected in the inspected status record.

## Confidentiality

This case study intentionally excludes source code, real data, screenshots, infrastructure identifiers, network topology, and operational configuration. The institutional source repository is not available for public or private third-party distribution.

## Feedback and content rights

Use the issue form for product questions or corrections. Remove personal information from screenshots and reports. This is a public product presentation; application source remains private.

[Content rights](NOTICE.md). Previously licensed assets retain their existing permissions.
