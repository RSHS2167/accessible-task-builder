# Accessible Task Suite v2 (prototype)

Two connected applications:

1. **Accessible Task Builder (`index.html`)**: create, view and edit tasks, including faculty organisation, conditions, steps, rubric editing, support prompts, local confirmation records, batch JSON importing, batch Word/PDF exporting and marking on fillable landscape PDF pages.
2. **Batch converter (`convert_app.py`)**: takes a ZIP of existing Word `.docx` task sheets and produces task JSON files, a whole-batch import JSON and a review report. Text is extracted rather than rewritten.

## Quick start: review the 22 converted tasks

1. Open `index.html` in Chrome or Edge, or replace the `index.html` file in your GitHub Pages repository with this newer version.
2. Choose **Batch import JSON** from the Faculty Organiser.
3. Select `import_all_tasks.json` from the `Converted_Tasks.zip` archive (extract the archive first).
4. The converted tasks appear as **drafts**. In each task, open **Review & supports** to see any conversion warnings, and **Marking criteria** to check imported A–E standards.
5. Compare with the original Word document before confirming/publishing. The converter does not infer missing standards or recreate attached folio worksheets, graphics and embedded media.

## Run the batch converter yourself (Windows)

1. Have Python 3 installed. Ensure the Python installer adds Python to PATH.
2. Double-click `Start_Converter.bat` (installs `python-docx` if required).
3. Open `http://127.0.0.1:8765` if it did not appear automatically.
4. Upload a ZIP containing Word `.docx` assessment task sheets, then select **Convert and download**.
5. Extract the returned ZIP and use `import_all_tasks.json` in the web app. Check `conversion_report.csv` for every file.

Command line alternative:

```powershell
python -m pip install -r requirements.txt
python converter.py "OneDrive_1_19-10-2026.zip" -o converted_tasks.zip
```

The converter runs **on your own computer** and does not upload the documents to a third-party server.

## Export and mark tasks

The Word and PDF exports maintain the established portrait assessment layout: title, task, conditions, key terms, followed by Steps for Success. **Longer content may now continue onto more portrait pages instead of being shortened or omitted.** If A–E marking criteria have been entered, the last page or pages are **A4 landscape** with selectable descriptor cells, editable teacher comments and a final result field in the PDF.

To mark the PDF, open it in a PDF reader supporting AcroForm fields, select the appropriate rubric cells, type comments and a grade, then save the completed PDF. Reader support and checkbox appearance vary; desktop Adobe Acrobat Reader is a useful choice. The built-in EV3 marking descriptors are **illustrative only**, not an official QCAA marking instrument.

In the task viewer, choose **Standard**, **Guided** or **Extension** to display optional additional support. This does not change the official marking standards. Use **Review & supports** to configure these prompts.

**Batch export ZIP** creates individual JSON and Word files, and tries to create a fillable PDF for every task. If a particular PDF cannot be laid out, a named error text file is included instead of silently truncating the task.

## Local database pilot (optional)

Run `Start_Database_Pilot.bat`. This launches the task builder at `http://127.0.0.1:8766` with a **local SQLite task database**. On the Faculty Organiser select **Save to local database** or **Load from local database**.

This is intentionally limited to the same computer. It is **not a shared school database**, not an authenticated approval workflow and not secure for hosting on a public network. Actual school-wide use would need Department/school IT approval, staff authentication, permissions, backups, access logging, student data protections and a properly deployed secure service. GitHub Pages is static and **cannot provide database synchronisation on its own**.

Staff 'confirmation' in this prototype is an unverified local record, not a digital signature or formal approval.

## Content and accuracy

- The converter processed 22 supplied `.docx` files in this example batch.
- 5 contained A–E grade tables that could be recognised automatically. For the other 17, an A–E standards matrix was **not detected**. This does not mean the subject has no achievement standards; add them from the approved original assessment criteria.
- Some source documents also include production worksheets, student folio pages and long merged tables. These require human review. Unsupported content is flagged in the CSV instead of invented.
- Original wording from the supplied files was preserved where it could be extracted; no AI rewriting was applied to the imported tasks.
- Do not publish the imported tasks without checking the context, requirements, Steps for Success and marking criteria against the originals.

## GitHub Pages

Upload `index.html` to your existing repository's root. Keep `README.md` and `.nojekyll` with it if desired. The app runs on GitHub Pages, but browser storage remains per-device. The two local Python utilities will **not** run on GitHub Pages.
