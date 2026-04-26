---
repo: piki
last_synced_commit: 0012803588dcb14e23c3492764da54437ac5a5c9
---
# `piki/main.py`

이 파일은 `piki` CLI 애플리케이션의 주 진입점입니다. `typer` 라이브러리를 사용하여 커맨드 라인 인터페이스를 구성합니다.

> src: piki@00128035:piki/main.py#L1-L3

주요 역할은 `piki.commands` 패키지에 정의된 각 명령어 모듈(예: `init_cmd`, `ingest_cmd`)을 `app` 객체에 등록하여 하위 명령어로 사용할 수 있게 하는 것입니다.

> src: piki@00128035:piki/main.py#L5-L11

## 관련
- `[piki overview](../../overview.md)`
- `[piki API](../../api.md)`

## 변경 이력
- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [piki 리포지토리 개요](../../overview.md)
<!-- piki:backlinks-end -->
