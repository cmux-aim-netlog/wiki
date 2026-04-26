---
repo: piki
last_synced_commit: 0012803588dcb14e23c3492764da54437ac5a5c9
---
# `piki/commands/ingest_cmd.py`

이 파일은 `piki ingest` 명령어의 구현을 포함하며, piki 시스템의 핵심 자동화 기능을 담당합니다. 

주요 기능은 지정된 소스 리포지토리의 변경 사항을 분석하고, 이 변경 사항을 기반으로 LLM 에이전트를 호출하여 관련 위키 페이지를 생성하거나 업데이트하는 것입니다. 이는 piki 패턴에서 설명하는 'Sync' 작업에 해당합니다.

> src: piki@00128035:piki/templates/piki.md#L54-L59

`ingest` 함수는 `typer`에 의해 CLI 명령어로 등록되며, 소스 리포지토리의 경로와 같은 인자를 받습니다.

> src: piki@00128035:piki/commands/ingest_cmd.py#L6-L10

## 관련
- `[piki overview](../../../overview.md)`
- `[piki API](../../../api.md)`

## 변경 이력
- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [piki 리포지토리 개요](../../../overview.md)
<!-- piki:backlinks-end -->
