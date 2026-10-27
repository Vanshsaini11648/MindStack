# MindStack — Project Report

## Abstract
MindStack is a static, local-first personal knowledge management system for capturing and organizing notes, programming references, tasks, study cards, quizzes, and bookmarks. It is designed to run from static hosting without a mandatory backend.

## Problem statement
Learning material, coding references, tasks, and links often become scattered across applications. MindStack brings these records into a single searchable workspace while keeping data in the user's browser.

## Objectives
- Provide a unified place for notes, tasks, bookmarks, and study material.
- Support basic organization through folders, tags, favourites, pinning, and archive/trash.
- Make stored knowledge searchable.
- Allow user-owned backups and restore through JSON.
- Offer a responsive interface suitable for desktop and mobile browsers.
- Deploy as a static website without backend configuration.

## Scope
The current implementation includes local notes, folder/tag management, global search, note links and a canvas graph, developer notes, tasks, a due-date calendar, bookmarks, flashcards, multiple-choice quizzes, templates, data inventory analytics, theme preferences, and JSON/Markdown export.

## Technology stack
- HTML5 for semantic application structure.
- CSS3 for responsive layout, themes, and components.
- Vanilla JavaScript (ES6+) for application logic.
- LocalStorage for structured local persistence.
- SVG for the application icon.
- Vercel static hosting for optional deployment.

## Architecture
The app is composed of a root HTML shell, one stylesheet, and two JavaScript modules. `core.js` contains the local data model, persistence, validation, dialogs, and backup utilities. `app.js` renders views and handles UI interactions. There is no API server or cloud database.

## Data model
Records are stored under a versioned LocalStorage key and include notes, folders, tags, tasks, bookmarks, flashcards, quizzes, study sessions, activity, and preferences. Each created record receives a generated identifier and timestamps where applicable.

## Module descriptions
- Dashboard: real counts, recent notes, activity, and upcoming tasks.
- Notes: editing, local autosave, folders, tags, pin/favourite, archive/trash, duplication, version snapshots, export, and links.
- Search: searches saved notes, tasks, and bookmarks.
- Knowledge graph: visualizes actual notes and explicit note links.
- Developer library: notes labeled by programming language.
- Study: flashcards, review intervals, study-session logging, and authored quizzes.
- Tasks/calendar: task status, priority, due date, and month view.
- Bookmarks: URL validation, duplicate checking, category, tags, and external links.
- Templates: creates real editable notes with suggested structures.
- Settings/backup: theme, accent, font size, JSON import/export, Markdown export, and clear-data confirmation.

## Testing methodology
The delivered package has been checked for JavaScript syntax, local asset references, and ZIP integrity. A manual test checklist is included in `tests/test-plan.md`. Full browser-based end-to-end testing and live Vercel deployment verification have not been performed in this environment.

## Limitations
- LocalStorage is browser-profile and origin specific; it is not cloud sync and is not encrypted by this app.
- Large data volumes may encounter browser storage quotas.
- No login, multi-user collaboration, system notifications, or cloud synchronization is included.
- Markdown editing is text-based; the preview is intentionally basic.
- The graph layout is a compact overview rather than a full graph editor with zoom/pan.
- No claim is made that the app has been deployed to Vercel.

## Future enhancements
- Add IndexedDB for larger attachments.
- Improve Markdown preview and accessible rich-text editing.
- Add graph zoom, pan, and relationship types.
- Add automated browser tests and performance checks.
- Add optional, user-configured synchronization only if a backend is intentionally introduced.

## Viva overview
MindStack is a browser-based second-brain app built with HTML, CSS, and vanilla JavaScript. It stores user records in LocalStorage, supports notes and productivity tools, and exports JSON backups for portability. Its main design choice is local-first storage, which allows static hosting and avoids a mandatory backend, but means users must back up their data manually.
