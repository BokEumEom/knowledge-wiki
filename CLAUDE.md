# knowledge-wiki project instructions

This repository stores source evidence in `raw/` and synthesized knowledge in `wiki/`.

When a URL is provided:
1. Use the `ingest-url` skill.
2. Capture the source into `raw/sources/YYYY/<source-id>/`.
3. Create or update `wiki/sources/YYYY/<slug>.md`.
4. Update related topic or project pages.
5. Update `wiki/index.md` and `wiki/log.md`.

Rules:
- raw is evidence, wiki is synthesis
- do not modify raw content after capture
- prefer updating existing pages over creating near-duplicates
- record unresolved conflicts in `wiki/dashboards/contradictions.md`