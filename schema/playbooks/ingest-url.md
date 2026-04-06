# ingest-url playbook

Goal:
Turn one URL into raw evidence plus updated wiki knowledge.

Steps:
1. Fetch the URL content.
2. Determine:
   - title
   - source type
   - author or publisher
   - capture date
3. Create a source id:
   - YYYY-MM-DD__author-or-site__slug
4. Create:
   - `raw/sources/YYYY/<source-id>/meta.yaml`
   - `raw/sources/YYYY/<source-id>/source.url`
   - `raw/sources/YYYY/<source-id>/original.*`
5. Create or update:
   - `wiki/sources/YYYY/<slug>.md`
6. Fill:
   - Summary
   - Key Claims
   - Evidence / Notes
   - Why It Matters
   - Open Questions
   - Related Pages
7. Update:
   - `wiki/index.md`
   - `wiki/log.md`
8. Update at least one related page in:
   - `wiki/topics/`
   - or `wiki/projects/`

Rules:
- raw stores evidence only
- wiki stores synthesis only
- do not delete or overwrite previous raw captures
- if claims conflict, update `wiki/dashboards/contradictions.md`