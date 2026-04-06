# Knowledge Wiki Rules

이 저장소는 지속적으로 관리되는 개인 지식 위키다.

우선 읽을 파일:
1. schema/wiki-conventions.md
2. schema/workflows.md
3. wiki/index.md

규칙:
- `raw/`는 원본 자료이며 수정하지 않는다.
- `wiki/`는 정제된 지식 레이어다.
- 새 자료를 ingest할 때는 반드시 아래를 갱신한다:
  - source summary 1개 이상
  - `wiki/index.md`
  - `wiki/log.md`
  - 관련 topic/entity/project 페이지
- 충돌하는 내용은 `wiki/dashboards/contradictions.md`에 기록한다.
- 삭제보다 deprecated 표기를 우선한다.