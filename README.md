# upskill-courses

Three self-contained, single-file training courses on Microsoft 365 Copilot,
served as static HTML via GitHub Pages.

- `index.html` — landing page linking the three courses
- `intro-copilot-chat.html` — Introduction to M365 Copilot Chat (14 lessons)
- `intro-copilot-chat-agents.html` — Introduction to Copilot Chat Agents (13 lessons)
- `intro-copilot-cowork.html` — Introduction to Copilot Cowork (15 lessons)

## Running a course locally

Each course is a single HTML file with inline CSS and inline JavaScript —
there's no build step, no bundler, no backend, and no package dependencies.
To run one locally, just open the file directly in a browser:

```
open intro-copilot-chat.html      # macOS
xdg-open intro-copilot-chat.html  # Linux
```

Or serve the folder with any static file server, e.g. `python3 -m http.server`,
and visit the file in your browser.

Course content (sections, lessons, and quizzes) lives in JS arrays
(`SECTIONS`, `LESSONS`, `INLINE_QUIZZES`, `FINAL_QUIZ`) near the top of each
file's `<script>` tag and is rendered into the page at runtime. Progress is
tracked client-side only, in memory for the current page load.

## Deployment

This repo is served directly by GitHub Pages from the root of `main` — the
`.nojekyll` file disables Jekyll processing so the HTML files are served as-is.
