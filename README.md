# Vocabulary Study

A vocabulary flashcard and quiz app for studying definitions. Built as a static site for GitHub Pages.

## Running Locally

The site uses `fetch()` to load vocabulary data from JSON files, so it must be served by an HTTP server (opening `index.html` directly from the filesystem won't work).

**Using Python:**

```bash
cd /path/to/this/project
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.

**Using Node.js (npx):**

```bash
npx serve .
```

## How It Works

1. Pick who's studying (Liam or Dylan) on the main page
2. Choose **Flashcards** to flip through vocabulary cards, or **Quiz** to take a multiple-choice test
3. Quiz stats and progress are saved per child in the browser's localStorage

## Adding Vocabulary

Vocabulary files live in the `data/` directory as JSON arrays:

```json
[
  { "word": "Example", "definition": "a thing used to illustrate a rule" }
]
```

To add a new child, create a new JSON file in `data/` (e.g., `data/alex.json`) and add a selection card in `index.html`.
