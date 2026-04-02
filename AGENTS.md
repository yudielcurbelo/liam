# Repository Guidelines

## Project Overview
- This repo is a static vocabulary study site for GitHub Pages.
- The app is driven by `index.html`, `VocabularyFlashcard.html`, `VocabularyQuiz.html`, and JSON files in `data/`.
- There is no build step or framework setup; keep changes compatible with a plain static host.

## Working Conventions
- Preserve the static-site approach. Do not introduce package managers, bundlers, or build tooling unless explicitly requested.
- When testing locally, use an HTTP server because the pages load vocabulary data with `fetch()`. Do not rely on opening HTML files directly from the filesystem.
- Keep implementations lightweight and browser-native. Prefer small inline JavaScript and existing Tailwind utility patterns over adding new dependencies.
- Reuse the existing child selection flow and query parameter behavior when extending features across pages.

## Data And Content
- Vocabulary files in `data/` must remain JSON arrays of objects with `word` and `definition` string fields.
- If you add a new child, update both the matching `data/*.json` file and the selection UI in `index.html`.
- Keep image asset references in `images/` aligned with any new child cards or profile displays.

## Editing Notes
- Match the existing HTML, CSS, and JavaScript style in each page. Keep changes localized and easy to read.
- Prefer incremental edits over large rewrites, especially in the inline scripts inside the HTML files.
- If you add local-only files or generated output, update `.gitignore` in the same change.
