---
repo: .github
last_synced_commit: 2e7f8ab90e8e608c41c2974ec03d98058c54157e
---
# templates/piki.repo.workflow.yml.tmpl

이 파일은 piki 위키 시스템과 연동되는 각 소스 코드 리포지터리에 설치될 GitHub Actions 워크플로우의 템플릿입니다.

## 템플릿의 역할

`[piki_init.py 스크립트](../../scripts/piki_init.py.md)`는 이 템플릿을 사용하여 각 소스 리포지터리의 `.github/workflows/` 디렉토리에 `piki-sync.yml`과 같은 워크플로우 파일을 생성합니다.

생성된 워크플로우는 다음과 같이 동작합니다.
1.  해당 리포지터리의 `main` 브랜치에 push가 발생하면 트리거됩니다.
2.  piki 위키 리포지터리로 `repository_dispatch` 이벤트를 전송합니다.
3.  이벤트 페이로드(payload)에 자신의 리포지터리 이름과 최신 커밋 SHA를 담아 보냅니다.

이 메커니즘을 통해 소스 코드의 변경 사항이 발생했을 때 중앙 위키 리포지터리가 이를 인지하고 자동으로 문서 동기화 프로세스를 시작할 수 있습니다.

> src: .github@2e7f8ab9:templates/piki.repo.workflow.yml.tmpl

## 관련
- `[.github 리포지터리 개요](../../overview.md)`
- `[piki_init.py 스크립트](../../scripts/piki_init.py.md)`

## 변경 이력
- 2026-04-26: 최초 생성
