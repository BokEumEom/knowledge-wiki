---
title: LLM Wiki
type: source-summary
date: 2026-04-06
source_path: raw/processed/articles/2026/2026-04-06__karpathy__llm-wiki.md
source_kind: article
status: active
tags: [llm, wiki, knowledge-management, rag]
related_pages:
  - wiki/projects/knowledge-wiki.md
  - wiki/topics/claude-code.md
  - wiki/topics/codex.md
---

# Summary
Karpathy의 핵심 아이디어는 문서를 질문 시점마다 다시 찾는 RAG 중심 구조를 넘어서, LLM이 지속적으로 유지·갱신하는 wiki 레이어를 두는 것이다. 원문과 사용자 사이에 interlinked markdown wiki를 두고, 새 소스가 들어올 때마다 지식을 축적하는 방식이다.

# Key Claims
- RAG는 질문마다 지식을 다시 찾고 합성하므로 축적성이 약하다.
- 더 나은 방식은 `raw sources / wiki / schema`의 3층 구조를 두는 것이다.
- wiki는 단순 요약 저장소가 아니라 점진적으로 업데이트되는 persistent knowledge layer다.
- 핵심 운영 루프는 `ingest / query / lint`다.
- `index.md`와 `log.md`는 위키 운영의 중심 파일이다.

# Evidence / Notes
- 새 소스를 넣으면 LLM은 단순 색인이 아니라 기존 페이지를 갱신하고 연결해야 한다.
- query 결과도 일회성 응답으로 끝내지 않고 다시 wiki에 저장할 수 있다.
- 작은 규모에서는 임베딩 기반 검색 없이도 markdown wiki와 파일 탐색만으로 유용하게 운영할 수 있다.
- 사람이 하기 귀찮았던 위키 유지보수 비용을 LLM이 줄여줄 수 있다는 점이 핵심이다.

# Why It Matters
이 저장소는 단순 파일 보관함이 아니라, 시간이 지날수록 더 좋아지는 개인 knowledge OS를 목표로 한다. 이 문서는 그 운영 철학의 출발점이다.

# Open Questions
- source summary와 topic page의 업데이트 경계를 어디까지 나눌 것인가
- answer page를 모두 저장할지, 재사용 가치가 있는 답만 저장할지
- contradictions 페이지를 수동 검토 단계와 어떻게 연결할지

# Related Pages
- [[../../projects/knowledge-wiki.md]]
- [[../../topics/claude-code.md]]
- [[../../topics/codex.md]]