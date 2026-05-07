# Raw

This folder is the immutable source layer.

It is not the main Obsidian reading surface. Use `sources/` as the canonical starting point; use `raw/` when a separate replay/provenance copy is useful.

Use it for:

- clipped web articles
- user-pasted email captures with article URLs, snippets, separators, and PNote annotations
- exported book highlights
- transcripts
- meeting notes
- PDFs
- image assets
- metadata-only source stubs that point to an external canonical file

Rules:

- Do not overwrite a source just because the synthesis changes.
- For short link-plus-highlights article submissions, a compact raw record is enough when the source page preserves the exact captures in `Your Captures`.
- For URL-based article, essay, and blog ingests, this layer should preserve what the user actually provided, which may be highlights and PNotes rather than the full article.
- For long captures, imports, Kobo highlights, PDFs, transcripts, lab records, spreadsheets, and source-like pasted text, keep the full submitted capture here and only selected navigation excerpts in the source page.
- Keep the canonical URL in the raw capture when available so the source summary can be based on the full original source.
- If a source needs cleanup, preserve the original and create a clearly named cleaned copy only when necessary.
- Keep attachments close to the source or under a sensible domain subfolder.
- Use `inbox/sources/` for newly added material that has not been processed yet.
- Prefer domain subfolders such as `health/`, `company-building/`, `finance/`, `reading-writing/`, `travel/`, `philosophy-politics/`, and `misc/`.
- Within `reading-writing`, use `books/` and `blogs-essays-articles/` when helpful.
- Prefer human-readable filenames and store capture dates in frontmatter. Use date prefixes only for daily batches, imports, records, or ambiguous captures.
