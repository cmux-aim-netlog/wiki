---
repo: .github
last_synced_commit: 2e7f8ab90e8e608c41c2974ec03d98058c54157e
---
# scripts/piki_init.py

이 Python 스크립트는 새로운 소스 코드 리포지터리를 piki 위키 시스템에 온보딩(onboarding)하는 초기화 작업을 수행합니다.

## 주요 기능

`piki_init.py` 스크립트는 지정된 리포지터리에 대해 다음과 같은 작업을 자동화합니다.

1.  **워크플로우 파일 생성**: `[piki.repo.workflow.yml.tmpl](../../templates/piki.repo.workflow.yml.tmpl.md)` 템플릿을 사용하여, 대상 리포지터리의 `main` 브랜치에 push가 발생할 때마다 위키 동기화를 요청하는 GitHub Actions 워크플로우 파일을 생성하고 추가합니다.
2.  **위키 파일 생성**: 위키 리포지터리에 `[piki.wiki.dispatch.workflow.yml.tmpl](../../templates/piki.wiki.dispatch.workflow.yml.tmpl.md)`, `[piki.wiki.CLAUDE.md.tmpl](../../templates/piki.wiki.CLAUDE.md.tmpl.md)` 등의 템플릿을 기반으로 초기 설정 파일들을 생성합니다.

이 스크립트는 `[piki-init.yml 워크플로우](../workflows/piki-init.yml.md)`에 의해 실행되며, 새로운 서비스를 piki 기반의 자동화된 문서화 시스템에 통합하는 첫 단계를 담당합니다.

> src: .github@2e7f8ab9:scripts/piki_init.py

## 관련
- `[.github 리포지터리 개요](../../overview.md)`

## 변경 이력
- 2026-04-26: 최초 생성
