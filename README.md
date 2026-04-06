# knowledge-wiki

Claude Code와 Codex가 URL을 받아 raw source를 축적하고,
지속적으로 wiki를 갱신하는 개인 지식 저장소.

## 구조
- `raw/`: 원본 증거 저장
- `wiki/`: 요약, 연결, 해석이 축적되는 지식 레이어
- `schema/`: 에이전트가 따를 운영 규칙과 템플릿

## 기본 흐름
1. URL 입력
2. 에이전트가 원문을 `raw/`에 저장
3. 에이전트가 `wiki/sources/` 요약 페이지 생성
4. 관련 `topics/`, `projects/` 페이지 갱신
5. `index.md`, `log.md` 갱신