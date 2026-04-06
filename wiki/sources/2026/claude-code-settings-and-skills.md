---
title: Claude Code Settings and Skills
type: source-summary
date: 2026-04-06
source_path: raw/processed/articles/2026/2026-04-06__anthropic__claude-code-settings-skills.md
source_kind: documentation
status: active
tags: [claude-code, settings, skills, agents]
related_pages:
  - wiki/topics/claude-code.md
  - wiki/projects/knowledge-wiki.md
---

# Summary
Claude Code는 설정을 scope별로 나누어 관리하고, skills를 통해 반복 가능한 작업 흐름을 확장한다. 이 knowledge-wiki repo에서는 공통 규칙은 `CLAUDE.md`, 프로젝트 설정은 `.claude/settings.json`, 반복 작업은 skill 또는 agent 역할로 분리하는 방식이 적합하다.

# Key Claims
- Claude Code 설정은 managed, user, project, local scope로 나뉜다.
- 프로젝트 공용 설정은 `.claude/` 아래에 두고, 로컬 전용 설정은 별도로 분리할 수 있다.
- skills는 `SKILL.md` 파일을 중심으로 정의된다.
- Claude는 관련성이 있을 때 skill을 자동으로 사용하거나, 사용자가 직접 호출할 수 있다.
- Claude Code skills는 Agent Skills open standard를 따르되, invocation control, subagent execution, dynamic context injection 같은 확장을 가진다.

# Evidence / Notes
- project scope는 저장소 협업자와 공유되는 설정에 적합하다.
- local scope는 개인 전용 설정에 적합하며 커밋 대상이 아니다.
- 기존 custom commands는 skills와 같은 체계 안으로 통합되었다.
- skill은 단순 명령이 아니라, Claude가 도구를 활용해 작업을 오케스트레이션하는 플레이북 역할을 할 수 있다.

# Why It Matters
이 저장소에서는 지식의 정본은 repo 안 wiki에 두고, Claude Code의 local memory나 개인 설정은 보조 계층으로 취급하는 편이 안정적이다. 반복 작업은 별도 skill/agent 역할로 빼서 지식 파일과 작업 규칙을 분리할 수 있다.

# Recommended Repo Implications
- 공용 규칙: `CLAUDE.md`
- 프로젝트 설정: `.claude/settings.json`
- 개인 전용 예외: `.claude/settings.local.json`
- 반복 작업: ingest / answer / lint 성격의 skill 또는 subagent 분리

# Open Questions
- Claude 전용 skills를 `.claude/skills/`에도 둘지, 현재처럼 공용 구조 중심으로 유지할지
- subagent를 언제부터 도입할지
- local memory 사용 규칙을 repo 차원에서 어디까지 명시할지

# Related Pages
- [[../../topics/claude-code.md]]
- [[../../projects/knowledge-wiki.md]]