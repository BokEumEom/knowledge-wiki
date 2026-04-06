# Workflows

## Ingest
1. 새 자료를 `raw/inbox/`에 넣는다
2. 자료를 읽고 source summary를 만든다
3. 관련 topic/entity/project 페이지를 갱신한다
4. index와 log를 갱신한다

## Query
1. 먼저 `wiki/`에서 관련 페이지를 찾는다
2. 부족하면 `raw/` 원문을 확인한다
3. 유의미한 답변은 다시 위키에 저장한다

## Lint
- 오래된 주장
- 끊어진 링크
- 고아 페이지
- 누락된 연결
- 상충 내용
을 점검한다