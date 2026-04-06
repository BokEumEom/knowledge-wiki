---
title: LLM Wiki
type: source-summary
date: 2026-04-06
source_path: raw/processed/articles/2026/2026-04-06__karpathy__llm-wiki.md
source_kind: article
status: active
tags: [llm, wiki, knowledge-management]
related_pages:
  - wiki/topics/ai-agents.md
  - wiki/projects/knowledge-wiki.md
---

# Summary
Karpathy의 아이디어는 RAG처럼 매번 원문에서 다시 찾는 대신, LLM이 지속적으로 유지·갱신하는 wiki 레이어를 두자는 것이다.

# Key Claims
- raw sources / wiki / schema의 3층 구조가 중요하다
- ingest / query / lint의 반복 루프가 필요하다
- index.md와 log.md가 위키의 핵심 운영 파일이다
- 지식은 답변 순간이 아니라 지속적으로 축적되는 구조여야 한다

# Evidence / Notes
- wiki는 compounding knowledge artifact 역할을 한다
- query 결과도 다시 wiki에 축적할 수 있다

# Related Pages
- [[../../topics/ai-agents.md]]
- [[../../projects/knowledge-wiki.md]]