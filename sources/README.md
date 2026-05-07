# Sources

This folder holds one canonical human-readable page per source.

For a submitted source, this is the page the user should open first in Obsidian. It should work as a source hub: source metadata, raw capture link, summary basis, exact user captures, LLM synthesis, durable links, and filing notes.

Each page should answer:

- What is this source about?
- What are the key claims, ideas, or observations?
- What is the summary based on: full source URL, user-provided excerpts, metadata stub, or mixed access?
- What exact personal highlights, imported notes, or PNotes were supplied, if any?
- What other pages should be updated because of it?
- What is still uncertain or worth following up?

Link each summary back to the raw source capture under `raw/` when one exists. For short link-plus-highlights submissions where the source page itself preserves the exact capture, make that basis explicit in frontmatter and `Summary Basis`.

For URL-based articles, essays, and blog posts, summarize the original source when it is accessible. Keep exact user highlights and PNotes in a separate `Your Captures` section. If the original source is inaccessible, say that directly and summarize only from the captured excerpts or metadata.

For article, essay, and blog source pages, prefer this section pattern:

- `Summary Basis`
- `What This Source Is`
- `Source Summary`
- `Key Ideas`
- `Your Captures`
- `Capture-Based Synthesis`
- `Claims Worth Tracking`
- `Caveats`
- `Related Pages`

For books and long Kobo highlight imports, do not write as if the full book has been summarized unless the full book has actually been reviewed. Use `summary_basis: imported Kobo highlights` or similar.

Book source pages are highlight-led reading pages. Prefer this section pattern:

- `Summary Basis`
- `What This Page Is`
- `Highlight Map`
- `Your Captures`
- `Capture-Based Synthesis`
- `Reusable Ideas`
- `Possible Uses`
- `Open Questions`
- `Related Pages`

For `Your Captures`, link to the raw quote export for the complete exact highlight set. Preserve exact personal notes on the source page when they exist. Use selected highlight anchors to make the page navigable without copying the entire raw export.

Prefer human-readable filenames such as `Author - Source Title.md`; keep publication and ingest dates in frontmatter unless the date is part of the source's canonical title.

Use digest pages only when many small fragments truly belong together, such as:

- multiple tweets on the same theme
- several podcast snippets from one episode
- a batch of article bookmarks on a single question
