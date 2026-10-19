# Accessible Task Builder v6 - section-by-section AI permissions

This package is ready for **GitHub Pages**. It is a single-file browser app, with no server installation required.

## What's new

In the **Task editor -> Steps for Success** tab, each numbered section has an optional **AI use** selector:

- Level 1 - NO AI (red)
- Level 2 - AI PLANNING (yellow)
- Level 3 - AI COLLABORATION (green)
- Level 4 - FULL AI (blue)
- Level 5 - AI EXPLORATION (purple)

Selections appear as compact labels beside each section heading in the student screen viewer and in Word and interactive PDF exports. Students can click a label in the screen viewer to read a brief explanation. The colours are slightly adjusted for contrast on the small labels.

**The default is Not set.** Existing tasks and imported files do not automatically receive an AI permission. The responsible teacher must select the applicable level. The school AI-use poster and the teacher's instructions remain authoritative.

Individual JSON exports, batch ZIP exports, imports and browser backups preserve per-section `aiLevel` values (integer 1-5, or null). Older task JSON remains compatible. The `JSON template` includes this optional property.

## Deploy to GitHub Pages

Replace the repository-root `index.html` with the one in this package and commit. Keep `.nojekyll`. Once GitHub Pages deploys, perform a hard refresh (**Ctrl+Shift+R** in Chrome or Edge).

This is a **browser-local application**. Tasks and progress remain in the browser where they were created. Export a backup before changing the website. The optional marking criteria, converter sidebar, and Word/PDF exports remain available.
