# H4ck2.github.io

Public research notes for kyun0 / H4ck2.

## Site structure

This site is built by GitHub Pages/Jekyll.

- `_data/research.yml` is the source of truth for research cards.
- `index.html` renders the latest cards from `_data/research.yml`.
- `notes.html` renders the full card list from `_data/research.yml`.
- `research/*.html` contains the public detail pages.
- `favicon.ico` / `favicon.png` are shared across pages.

## Add a new research card

1. Create the detail page under `research/`, for example:

   ```text
   research/example-research-note.html
   ```

2. Add one item to `_data/research.yml`:

   ```yaml
   - title: "Example research note"
     date: "2026-06-09"
     display_month: "June 2026"
     meta_index: "coordinated disclosure · June 2026"
     meta_notes: "web · June 2026"
     category: "web"
     badge: "PUBLIC"
     url: "./research/example-research-note.html"
     description: "Short public description shown on cards."
     status_label: "Status"
     status: "Public"
     metric2_label_index: "Class"
     metric2_index: "Web Security"
     metric2_label_notes: "Category"
     metric2_notes: "Web"
     detail_label: "Detail"
     detail: "Short detail"
   ```

3. Keep `date` in `YYYY-MM-DD` format. Cards are sorted by this field.

## Publication notes

- Do not publish private advisory text, private PoC payloads, or exploit chains.
- For hardening-only OSS work, avoid CVE/advisory language unless the upstream project assigned it.
- Keep old redirect files only when preserving an existing public URL.
