---
title: "LLM Wiki"
type: source-summary
date: 2026-04-04
source_path: raw/sources/2026/2026-04-04__karpathy__llm-wiki/original.md
source_kind: gist
status: active
tags: [llm, knowledge-management, wiki, rag, personal-knowledge-base, obsidian]
related_pages: [../../topics/llm-knowledge-management.md]
---

# Summary

Andrej Karpathy가 제안하는 LLM 기반 개인 지식 베이스 구축 패턴. 기존 RAG(질의 시마다 원문에서 재검색)와 달리, LLM이 **지속적으로 위키를 갱신하는 컴파운딩 아티팩트**를 만드는 방식이다. 사람은 소스 큐레이션과 질문을 담당하고, LLM이 요약·교차참조·일관성 유지 등 모든 정리 작업을 수행한다.

# Key Claims

- RAG는 매 질의마다 지식을 처음부터 재구성하므로 축적이 없다
- LLM이 점진적으로 구조화된 위키를 빌드·유지하면 지식이 복리로 축적된다
- 위키는 persistent, compounding artifact — 교차참조와 모순 플래깅이 사전에 완료됨
- 아키텍처는 3계층: raw sources(불변) → wiki(LLM 소유) → schema(운영 규칙)
- 핵심 운영: Ingest(소스 투입), Query(질의+위키 반영), Lint(건강성 검사)
- 사람의 역할은 큐레이션과 사고, LLM의 역할은 그 외 모든 정리 작업
- Vannevar Bush의 Memex(1945) 비전과 정신적으로 연결됨

# Evidence / Notes

- Karpathy 본인이 Obsidian + LLM 에이전트 조합으로 실제 사용 중
- 단일 소스 인제스트가 10-15개 위키 페이지를 업데이트할 수 있음
- index.md(콘텐츠 카탈로그) + log.md(시간순 기록)로 네비게이션
- 검색 도구로 qmd(BM25 + 벡터 하이브리드) 추천
- 도구: Obsidian Web Clipper, Marp(슬라이드), Dataview(프론트매터 쿼리)
- 위키가 git 레포이므로 버전 관리·브랜칭·협업이 무료

# Why It Matters

이 프로젝트(knowledge-wiki)가 정확히 이 패턴의 구현체이다. Karpathy의 설계 원칙(raw/wiki/schema 3계층, ingest-query-lint 운영, index+log 네비게이션)이 현재 레포 구조와 거의 1:1로 대응한다. 이 글은 프로젝트의 사상적 원류이자 설계 근거 문서 역할을 한다.

# Open Questions

- 위키 규모가 커지면(수백 페이지 이상) index.md 기반 탐색의 한계는 어디인가?
- 여러 에이전트(Claude Code, Codex 등)가 동일 위키를 동시에 갱신할 때 충돌 관리 방안은?
- Lint 운영의 적절한 주기와 자동화 수준은?

# Related Pages

- [LLM 지식 관리](../../topics/llm-knowledge-management.md)
