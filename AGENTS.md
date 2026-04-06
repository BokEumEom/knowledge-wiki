# Repo Instructions

이 저장소는 파일 기반 개인 지식 위키다.

먼저 읽을 파일:
- schema/wiki-conventions.md
- schema/workflows.md
- wiki/index.md

규칙:
- `raw/`는 읽기 전용 원본 자료다.
- `wiki/`는 지속적으로 유지되는 지식 베이스다.
- ingest 시 source summary, index, log, 관련 페이지를 함께 갱신한다.
- query 시 wiki를 먼저 보고, 부족할 때만 raw source를 확인한다.
- 가치 있는 답변은 `wiki/answers/` 등에 저장한다.