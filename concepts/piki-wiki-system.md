---
type: concept
last_synced_at: 2026-04-26T09:05:53Z
links_to: [".github", "piki", "Test_BE", "Test_FE"]
---
# Piki 위키 시스템

이 문서는 `cmux-aim-netlog` 조직에서 사용되는 piki 위키 시스템의 구성과 작동 방식을 설명합니다. piki는 코드 변경 사항을 기반으로 팀의 지식 기반을 자동으로 구축하고 유지 관리하는 시스템입니다.

## 핵심 구성 요소

piki 시스템은 여러 리포지터리의 상호 작용을 통해 운영됩니다.

- **`piki` 리포지터리**: piki 시스템의 핵심 도구인 `piki` CLI를 포함합니다. 이 CLI는 위키를 초기화, 동기화, 쿼리하는 데 사용됩니다.
  - 관련 페이지: `[piki overview](../repos/piki/overview.md)`

- **`.github` 리포지터리**: 조직의 piki 위키 연동을 총괄하는 중앙 허브입니다. 새로운 리포지터리를 piki 시스템에 온보딩하고 동기화 워크플로우를 설정하는 스크립트와 템플릿을 관리합니다.
  - 관련 페이지: `[`.github` overview](../repos/.github/overview.md)`

- **소스 리포지터리** (예: `Test_BE`, `Test_FE`): 실제 애플리케이션 코드가 포함된 리포지터리입니다. 각 소스 리포지터리에는 `.github` 리포지터리의 템플릿을 통해 생성된 GitHub Actions 워크플로우가 설치되어, `main` 브랜치의 변경 사항을 위키에 자동으로 동기화합니다.
  - 관련 페이지: `[Test_BE overview](../repos/Test_BE/overview.md)`, `[Test_FE overview](../repos/Test_FE/overview.md)`

## 동기화 흐름

1.  **초기화**: `[scripts/piki_init.py](../repos/.github/files/scripts/piki_init.py.md)` 스크립트를 사용하여 새로운 소스 리포지터리를 piki 시스템에 등록합니다.
2.  **워크플로우 설치**: 초기화 과정에서 `[piki.repo.workflow.yml.tmpl](../repos/.github/files/templates/piki.repo.workflow.yml.tmpl.md)` 템플릿이 각 소스 리포지터리에 복사되어 동기화 워크플로우가 설정됩니다.
3.  **변경 감지 및 동기화**: 개발자가 소스 리포지터리의 `main` 브랜치에 코드를 푸시하면, 설치된 워크플로우가 트리거됩니다.
4.  **위키 업데이트**: 워크플로우는 `piki ingest` 명령을 실행하여 변경된 파일의 내용을 분석하고, 관련 위키 페이지를 생성하거나 업데이트합니다. 이 과정은 위키 리포지터리에서 중앙 집중적으로 처리됩니다.

이 아키텍처를 통해 조직의 모든 코드베이스에서 발생하는 중요한 변경 사항과 컨텍스트가 중앙 위키에 지속적으로 축적됩니다.
