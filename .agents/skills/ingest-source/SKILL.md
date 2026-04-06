---
name: ingest-source
description: Process a new source into the wiki by creating a source summary, updating index/log, and linking related topic or project pages.
---

# Goal
Turn a new raw source into persistent wiki knowledge.

# Steps
1. Read a file from `raw/inbox/` or `raw/processed/`.
2. Create or update a source summary in `wiki/sources/YYYY/`.
3. Update `wiki/index.md`.
4. Append a dated note to `wiki/log.md`.
5. Update at least one related page in:
   - `wiki/topics/`
   - `wiki/projects/`
   - `wiki/entities/`
6. If the source introduces uncertainty, update:
   - `wiki/dashboards/open-questions.md`
7. If the source conflicts with existing knowledge, update:
   - `wiki/dashboards/contradictions.md`

# Rules
- Never edit files under `raw/` except moving from inbox to processed folders.
- Prefer updating existing topic pages over creating duplicates.
- Keep summaries concise and link outward.