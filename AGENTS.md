# knowledge-wiki repo rules

This repository is an agent-maintained knowledge wiki.

When the user provides a URL:
1. Use the `ingest-url` skill.
2. Capture the source into `raw/sources/YYYY/<source-id>/`.
3. Save:
   - `meta.yaml`
   - `source.url`
   - `original.*`
4. Create or update a source summary in `wiki/sources/YYYY/`.
5. Update at least one related page in:
   - `wiki/topics/`
   - or `wiki/projects/`
6. Update:
   - `wiki/index.md`
   - `wiki/log.md`

Rules:
- `raw/` stores evidence only.
- `wiki/` stores interpretation only.
- Never overwrite existing raw evidence unless explicitly asked.
- Prefer updating existing topic/project pages over creating duplicates.
- Record unresolved conflicts in `wiki/dashboards/contradictions.md`.