---
repo: piki
last_synced_commit: 0012803588dcb14e23c3492764da54437ac5a5c9
---
# piki 리포지토리 개요

piki는 LLM을 사용하여 팀의 코딩 지식 기반을 유지 관리하기 위한 패턴 및 도구입니다. 이 시스템의 핵심 아이디어는 에이전트가 매번 코드를 재분석하는 대신, 코드베이스와 함께 지속적으로 업데이트되는 영구적인 위키를 구축하고 활용하는 것입니다.

> src: piki@00128035:piki/templates/piki.md#L3-L4

이 위키는 코드만으로는 표현할 수 없는 결정 사항, 사용 중단된 기능, 컨벤션, 여러 리포지토리에 걸친 흐름, 주의사항 등을 구조화된 마크다운 파일로 관리합니다.

> src: piki@00128035:piki/templates/piki.md#L15-L18

## 아키텍처

piki 시스템은 네 가지 주요 계층으로 구성됩니다:

1.  **소스 리포지토리**: 팀의 실제 코드. piki는 이 리포지토리들을 읽기만 합니다.
2.  **위키**: 이 지식 베이스가 저장되는 단일 git 리포지토리입니다.
3.  **스키마 (`CLAUDE.md`)**: 위키의 구조와 유지보수 에이전트의 작동 방식을 정의합니다.
4.  **스킬 (`SKILL.md`)**: 소비자 에이전트가 piki CLI를 언제 어떻게 호출해야 하는지 정의합니다.

> src: piki@00128035:piki/templates/piki.md#L35-L50

## 주요 구성 요소

- **CLI 도구**: `piki` 명령어는 위키를 초기화, 업데이트, 쿼리하는 기본 인터페이스입니다. 자세한 내용은 `[piki API](./api.md)` 문서를 참조하세요.
- **진입점**: CLI 애플리케이션의 시작점은 `[piki/main.py](./files/piki/main.py.md)`입니다.
- **설정 관리**: 리포지토리 설정은 `[piki/config.py](./files/piki/config.py.md)`에서 처리합니다.
- **핵심 로직**: 소스 코드 변경 사항을 위키에 반영하는 핵심 로직은 `[piki/commands/ingest_cmd.py](./files/piki/commands/ingest_cmd.py.md)`에 구현되어 있습니다.
- **설치**: piki는 Homebrew를 통해 설치할 수 있습니다.

> src: piki@00128035:Formula/piki.rb#L1-L15

## 관련 문서
- `[piki API](./api.md)`
- `[Conventions](./conventions.md)`
- `[Gotchas](./gotchas.md)`

## 변경 이력
- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [Piki 위키 시스템](../../concepts/piki-wiki-system.md)
- [piki API (CLI)](api.md)
- [piki Conventions](conventions.md)
- [`piki/commands/ingest_cmd.py`](files/piki/commands/ingest_cmd.py.md)
- [`piki/config.py`](files/piki/config.py.md)
- [`piki/main.py`](files/piki/main.py.md)
- [`piki/templates/piki.md`](files/piki/templates/piki.md.md)
- [`piki/wiki/db.py`](files/piki/wiki/db.py.md)
- [piki Gotchas](gotchas.md)
<!-- piki:backlinks-end -->
