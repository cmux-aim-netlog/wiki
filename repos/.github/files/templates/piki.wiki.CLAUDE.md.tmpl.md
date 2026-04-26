---
repo: .github
last_synced_commit: 2e7f8ab90e8e608c41c2974ec03d98058c54157e
---
# templates/piki.wiki.CLAUDE.md.tmpl

이 파일은 piki 위키의 동작 규칙과 구조를 정의하는 `CLAUDE.md` 스키마 파일의 템플릿입니다.

## 템플릿의 역할

`CLAUDE.md` 파일은 piki maintainer 에이전트(LLM)가 위키 문서를 생성하고 업데이트할 때 따라야 할 지침서입니다. `[piki_init.py 스크립트](../../scripts/piki_init.py.md)`는 위키 리포지터리를 초기화할 때 이 템플릿을 사용하여 `CLAUDE.md` 파일을 생성합니다.

이 스키마 파일에는 다음과 같은 내용이 포함됩니다.

- **조직 및 위키 정보**: 위키가 속한 조직과 리포지터리 이름.
- **핵심 규칙**:
  - 위키의 운영 범위 (예: 조직 단위 단일 위키).
  - 소스 리포지터리 수정 금지.
  - 모든 사실에 대한 출처(citation) 명시 의무.
  - 불확실한 내용에 대한 처리 방법 (예: `[NEEDS HUMAN INPUT]` 태그 사용).

> src: .github@2e7f8ab9:templates/piki.wiki.CLAUDE.md.tmpl

이 템플릿을 통해 생성된 `CLAUDE.md`는 piki 시스템이 일관되고 신뢰할 수 있는 방식으로 문서를 유지보수하도록 보장하는 핵심적인 역할을 합니다.

## 관련
- `[.github 리포지터리 개요](../../overview.md)`
- `[piki_init.py 스크립트](../../scripts/piki_init.py.md)`

## 변경 이력
- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [.github 리포지터리 개요](../../overview.md)
<!-- piki:backlinks-end -->
