---
repo: piki
last_synced_commit: 0012803588dcb14e23c3492764da54437ac5a5c9
---
# piki API (CLI)

piki의 주요 인터페이스는 `piki` 명령어를 통해 제공되는 CLI입니다. 각 명령어는 `piki/commands` 디렉토리 내의 개별 모듈로 구현되어 있습니다.

> src: piki@00128035:piki/main.py#L5-L11

## 주요 명령어

- `piki init`
  새로운 piki 위키를 초기화합니다. 이 과정에서 위키 리포지토리의 기본 구조와 설정 파일(`piki.md`, `CLAUDE.md` 등)을 생성합니다.
  > src: piki@00128035:piki/commands/init_cmd.py

- `piki ingest`
  소스 리포지토리의 변경 사항을 감지하여 위키 페이지를 생성하거나 업데이트합니다. 이 명령어가 piki의 핵심적인 자동 동기화 기능을 수행합니다.
  > src: piki@00128035:piki/commands/ingest_cmd.py

- `piki show`
  위키에 저장된 특정 페이지나 정보를 터미널에 표시합니다.
  > src: piki@00128035:piki/commands/show_cmd.py

- `piki wiki`
  위키 리포지토리 자체를 관리하는 명령어 그룹입니다 (예: lint, health-check).
  > src: piki@00128035:piki/commands/wiki_cmd.py

- `piki config`
  piki 설정을 확인하거나 수정합니다.
  > src: piki@00128035:piki/commands/config_cmd.py

- `piki skill`
  소스 리포지토리에서 사용될 `SKILL.md` 파일을 관리합니다.
  > src: piki@00128035:piki/commands/skill_cmd.py

## 관련
- `[piki overview](./overview.md)`

## 변경 이력
- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [`piki/commands/ingest_cmd.py`](files/piki/commands/ingest_cmd.py.md)
- [`piki/main.py`](files/piki/main.py.md)
- [piki 리포지토리 개요](overview.md)
<!-- piki:backlinks-end -->
