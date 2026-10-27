# MindStack — Your Personal Second Brain

MindStack is a static, local-first personal knowledge management app built with HTML, CSS, and vanilla JavaScript. It has no backend, login, cloud sync, or required API.

## Features
- Responsive dashboard with dynamic counts and activity
- Notes, autosave, folders, tags, pin/favourite, archive, trash, restore, duplication, version snapshots, Markdown/plain-text export
- Global search (`Ctrl/Cmd + K`) across notes, tasks, and bookmarks
- Connected notes and an interactive canvas knowledge graph
- Developer notes with programming-language labels
- Tasks with priorities, due dates, statuses, and a monthly calendar
- Flashcards with review intervals and user-created multiple-choice quizzes
- Bookmarks with URL validation and duplicate detection
- Reusable note templates
- Data-derived inventory analytics
- Dark/light/system theme options and accent/font preferences
- JSON backup export/import and destructive-action confirmation

## Run locally
Open `index.html` in a modern browser. For the most consistent browser behavior, run a static server from this directory, e.g. `python -m http.server 8000`, then open `http://localhost:8000`. No package installation is required.

## Deploy to Vercel
1. Push the project folder contents to a GitHub repository.
2. Import that repository in Vercel.
3. Choose **Other** as the framework preset.
4. Leave build and install commands blank; set output directory to `.`.
5. Deploy. The root `index.html` and relative asset paths are suitable for static hosting.

No deployment has been performed or verified as part of this archive.

## Data and privacy
- Records live in browser `localStorage` and are specific to this browser profile and website origin.
- There is no cloud synchronization, account system, encryption claim, or cross-device transfer.
- Export a JSON backup regularly. Clearing site data or changing origin/browser may make records unavailable.
- Do not store passwords or sensitive credentials.
- Import validates the schema and asks for confirmation before replacing existing data.
- The interface starts empty. No sample notes, tasks, or bookmarks are preloaded.

## Testing
See `tests/test-plan.md`. The package includes a manual QA checklist. Automated browser end-to-end testing and a live Vercel deployment were not available in this environment, so they are not claimed as completed.
