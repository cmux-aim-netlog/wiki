---
repo: .github
last_synced_commit: 2e7f8ab90e8e608c41c2974ec03d98058c54157e
---
# templates/piki.wiki.dispatch.workflow.yml.tmpl

이 파일은 piki 위키 리포지터리 자체에 위치할 메인 동기화 워크플로우의 템플릿입니다.

## 템플릿의 역할

이 템플릿으로 생성된 워크플로우는 piki 위키의 핵심적인 자동 동기화 허브 역할을 합니다.

1.  **트리거**: `repository_dispatch` 이벤트가 발생했을 때 실행됩니다. 이 이벤트는 `[piki.repo.workflow.yml.tmpl](./piki.repo.workflow.yml.tmpl.md)`에 의해 각 소스 리포지터리에서 전송됩니다.
2.  **이벤트 처리**: 이벤트 페이로드에 포함된 소스 리포지터리 이름과 커밋 SHA를 파싱합니다.
3.  **Piki Maintainer 실행**: 파싱된 정보를 바탕으로 piki maintainer 에이전트(LLM)를 실행하여 해당 리포지터리의 변경 사항을 분석하고 관련된 위키 문서를 생성하거나 업데이트합니다.
4.  **커밋 및 PR 생성**: 업데이트된 위키 페이지를 위키 리포지터리에 커밋하고, 필요한 경우 리뷰를 위해 Pull Request를 생성합니다.

> src: .github@2e7f8ab9:templates/piki.wiki.dispatch.workflow.yml.tmpl

이 워크플로우는 전체 piki 시스템의 심장부로, 모든 소스 리포지터리의 변경 사항을 취합하여 위키에 반영하는 작업을 총괄합니다.

## 관련
- `[.github 리포지터리 개요](../../overview.md)`
- `[piki_init.py 스크립트](../../scripts/piki_init.py.md)`

## 변경 이력
- 2026-04-26: 최초 생성
