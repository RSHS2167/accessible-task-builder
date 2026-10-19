# Accessible Task Builder v3

A browser-first assessment task creator, student reader and exporter.

## GitHub Pages: manual update
1. Open your existing GitHub repository.
2. Replace the **root** `index.html` with the one in this ZIP and commit.
3. GitHub Pages automatically republishes from the selected branch, usually after a short delay.
4. Refresh the site using Ctrl+F5 if the old version remains cached.

## What's updated
- More compact task actions. Use **Import JSON / ZIP**, **Export ZIP** and **More** instead of the older wide action bar.
- Resizable, viewport-aware student reader. Long task content is divided across more screens rather than forced onto one A4-shaped screen. Very long individual descriptors may still scroll rather than become illegibly small.
- Import tolerant of incomplete or partially converted JSON tasks. Drafts are grouped by faculty, subject and unit. Red ! icons identify files requiring review. In **Edit > Review & supports**, see warnings and mark conversion reviewed after checking the original.
- **School settings > Convert Word task sheets** can convert multiple DOCX files or one ZIP containing DOCX files *inside your browser*, then download a batch JSON or import drafts directly. Uses the browser's built-in ZIP decompression in current Chrome or Edge; no server upload.
- Preserves existing Word and fillable PDF exports, landscape A–E marking rubric pages and locally saved drafts.

## Important limitations
- Converted Word tasks are draft extracts, not certified copies. Complex merged tables, images, worksheets, teacher notes and criteria must be checked against the original Word document before publishing.
- Data is saved in the local browser, not GitHub or a shared school database. GitHub Pages is only hosting this static app. Use backups, especially before clearing browser data.
- A shared school database, user permissions and staff confirmation workflow with authentication require separately hosted backend infrastructure.
- The student and staff display switch is not access control. Do not upload student-identifying data to a public repository.

## Optional Python converter
The full suite includes the earlier offline Python batch converter as a separate option for difficult files; it is not necessary for the built-in web converter.
