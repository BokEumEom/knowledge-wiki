---
title: Codex AGENTS and Skills
type: source-summary
date: 2026-04-06
source_path: raw/processed/articles/2026/2026-04-06__openai__codex-agents-and-skills.md
source_kind: documentation
status: active
tags: [codex, agents, skills, instructions]
related_pages:
  - wiki/topics/codex.md
  - wiki/projects/knowledge-wiki.md
---

# Summary
Codex는 작업을 시작하기 전에 `AGENTS.md` 계층을 읽고, 반복 가능한 워크플로는 skills로 분리해 사용한다. knowledge-wiki repo에서는 얇은 `AGENTS.md`로 저장소 규칙을 정의하고, ingest / answer / lint 같은 반복 작업은 별도 skill로 유지하는 구조가 잘 맞는다.

# Key Claims
- Codex는 작업 전에 `AGENTS.md`를 읽는다.
- instructions는 전역 홈 디렉터리에서 시작해 repo root에서 현재 디렉터리까지 계층적으로 합쳐진다.
- 하위 디렉터리의 guidance가 뒤에 붙으므로 더 구체적인 규칙이 우선한다.
- skills는 reusable workflow를 담는 기본 단위다.
- skill은 `SKILL.md`와 선택적 scripts/references/assets로 구성된다.
- Codex는 각 skill의 `name`, `description`, file path 등의 메타데이터를 먼저 보고, 필요할 때만 전체 내용을 불러오는 progressive disclosure 방식을 쓴다.

# Evidence / Notes
- `AGENTS.md`는 작고 지속적인 repo guidance에 적합하다.
- 반복되는 실수나 리뷰 피드백은 `AGENTS.md`에 반영해 다음 세션에도 이어지게 할 수 있다.
- skill의 `description`은 암묵적 트리거 품질에 큰 영향을 준다.
- skills는 workflow authoring 형식이고, plugin은 배포 단위다.

# Why It Matters
이 저장소에서 `AGENTS.md`는 “항상 적용되는 repo 운영 규칙”만 담고, 실제 작업 흐름은 skill로 분리하는 편이 Codex의 동작 방식과 가장 잘 맞는다. 즉, 규칙은 얇게, 작업 플레이북은 skill로, 지식은 wiki로 분리하는 구조다.

# Recommended Repo Implications
- 루트 `AGENTS.md`는 짧고 명확하게 유지
- topic별로 규칙이 달라지면 하위 디렉터리에 추가 `AGENTS.md` 또는 override 고려
- skill 이름과 설명은 trigger 범위가 겹치지 않게 설계
- 긴 절차 설명은 skill 쪽으로 보내고, repo 규칙은 `AGENTS.md`에 남김

# Open Questions
- 현재 repo에서 하위 디렉터리별 `AGENTS.md`가 필요한 시점은 언제인가
- ingest/answer/lint 외에 compare, timeline, export skill도 분리할지
- skills에 scripts를 붙일 단계가 언제인가

# Related Pages
- [[../../topics/codex.md]]
- [[../../projects/knowledge-wiki.md]]