---
repo: .github
last_synced_commit: 2e7f8ab90e8e608c41c2974ec03d98058c54157e
---
# .github 리포지터리 개요

이 리포지터리는 `cmux-aim-netlog` 조직의 GitHub 관련 설정을 중앙에서 관리합니다. 조직 프로필, 이슈 템플릿, 그리고 가장 중요하게는 piki 위키 시스템을 초기화하고 동기화하기 위한 워크플로우와 스크립트를 포함합니다.

## 주요 구성 요소

### Piki 위키 연동 시스템

이 리포지터리는 조직 내 다른 리포지터리들을 piki 위키 시스템에 온보딩하고, 코드 변경 사항을 위키에 자동으로 반영하는 핵심 로직을 담고 있습니다.

- **초기화 스크립트**: 새로운 리포지터리를 piki 시스템에 등록하는 스크립트입니다.
  - `[scripts/piki_init.py](./files/scripts/piki_init.py.md)`
> src: .github@2e7f8ab9:scripts/piki_init.py

- **워크플로우**: GitHub Actions 워크플로우는 초기화 및 동기화 프로세스를 자동화합니다.
  - `[piki-init.yml](./files/workflows/piki-init.yml.md)`: piki 초기화 스크립트를 수동으로 실행하는 워크플로우입니다.
  - `[piki-sync.yml](./files/workflows/piki-sync.yml.md)`: 이 `.github` 리포지터리 자체의 변경 사항을 piki 위키에 동기화하는 워크플로우입니다.
> src: .github@2e7f8ab9:.github/workflows/piki-init.yml
> src: .github@2e7f8ab9:.github/workflows/piki-sync.yml

- **템플릿**: 초기화 스크립트가 사용하여 각 소스 리포지터리와 위키 리포지터리에 필요한 파일들을 생성합니다.
  - `[piki.repo.workflow.yml.tmpl](./files/templates/piki.repo.workflow.yml.tmpl.md)`: 각 소스 리포지터리에 설치될 동기화 워크플로우 템플릿입니다.
  - `[piki.wiki.dispatch.workflow.yml.tmpl](./files/templates/piki.wiki.dispatch.workflow.yml.tmpl.md)`: 위키 리포지터리에서 동기화 요청을 받아 처리하는 워크플로우 템플릿입니다.
  - `[piki.wiki.CLAUDE.md.tmpl](./files/templates/piki.wiki.CLAUDE.md.tmpl.md)`: 위키의 동작 규칙을 정의하는 `CLAUDE.md` 스키마 템플릿입니다.
> src: .github@2e7f8ab9:templates/

## 변경 이력
- 2026-04-26: 최초 생성
