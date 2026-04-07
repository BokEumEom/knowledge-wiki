---
title: "LLM 지식 관리"
type: topic
status: active
updated: 2026-04-07
tags: [llm, knowledge-management, rag, wiki, personal-knowledge-base]
sources: [../sources/2026/llm-wiki.md]
---

# Overview

LLM을 활용한 지식 관리 접근법들. 기존 RAG(검색 증강 생성)부터 LLM이 직접 위키를 유지·갱신하는 패턴까지 포괄한다.

# Current Understanding

**RAG 방식의 한계**: 질의 시마다 원문에서 관련 청크를 검색하여 답변을 생성. 지식이 축적되지 않고 매번 재구성됨. NotebookLM, ChatGPT 파일 업로드 등이 이 방식.

**LLM Wiki 패턴** (Karpathy, 2026): LLM이 점진적으로 구조화된 마크다운 위키를 빌드·유지. 소스 투입 시 요약 작성, 교차참조 갱신, 모순 플래깅이 한 번에 이루어짐. 지식이 복리(compounding)로 축적되는 것이 핵심 차별점.

3계층 아키텍처:
- **Raw sources**: 불변 원본 증거
- **Wiki**: LLM이 소유·유지하는 합성 레이어
- **Schema**: 에이전트 운영 규칙과 컨벤션

핵심 운영 3가지:
- **Ingest**: 소스 투입 → 위키 갱신 (1개 소스가 10-15 페이지 터치)
- **Query**: 위키 기반 질의 → 좋은 답변을 다시 위키에 반영
- **Lint**: 모순, 고아 페이지, 누락 참조 등 건강성 점검

# Key Sources

- [LLM Wiki (Karpathy)](../sources/2026/llm-wiki.md) — 패턴의 원본 제안 문서

# Open Questions

- RAG와 LLM Wiki 패턴의 하이브리드 접근은 가능한가?
- 위키 규모 확장 시 임베딩 기반 검색(qmd 등) 도입 시점은?
- 멀티 에이전트 환경에서의 위키 동시 갱신 충돌 관리

# Related Pages

- [LLM Wiki source summary](../sources/2026/llm-wiki.md)
