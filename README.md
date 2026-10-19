# Accessible Task Builder v7

Static, browser-based task authoring and accessible student viewer, suitable for GitHub Pages.

## Publish to your existing GitHub Pages site

Replace the root `index.html` with this version, commit the change, and reload the site (Ctrl+Shift+R).
Existing tasks stored in this browser on the same domain should remain available. Always export a backup first.

## Changes in v7

- Faculty organiser starts with all faculties collapsed; searching expands matching faculties.
- Task editor includes **6. Tier variations**. Enter optional Guided or Extension task text, section headings, and individual lettered step alternatives. Blank entries fall back to Standard wording.
- Choose **Standard**, **Guided** or **Extension** at the top of the editor or student viewer. The selected version is labelled in previews, the exported task title, and file names.
- Word and PDF exports use hanging indents for wrapped a/b/c steps.
- Bulk export includes Standard and any non-empty Guided/Extension alternatives.
- Three built-in examples include editable tier variations.

## Data / safety

Tasks save locally in your browser (localStorage), not on GitHub. Different staff and students are not synchronised. This static site has no user authentication or school database.
The default Guided and Extension variations are sample prompts. Teachers need to check that variations remain fair, valid and aligned with the task's approved achievement standards.

## Word conversion

Use **Convert Word Tasks** under School Settings in the left sidebar to process task sheet DOCX files or ZIPs containing DOCX files. Review conversions before use.
