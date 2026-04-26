---
repo: .github
last_synced_commit: 2e7f8ab90e8e608c41c2974ec03d98058c54157e
---
# workflows/piki-sync.yml

이 GitHub Actions 워크플로우는 `.github` 리포지터리 자체의 변경 사항을 piki 위키에 동기화하는 역할을 합니다.

## 주요 특징

- **트리거**: 이 리포지터리의 `main` 브랜치에 코드가 push될 때 자동으로 실행됩니다.
> src: .github@2e7f8ab9:.github/workflows/piki-sync.yml
- **동기화 요청**: 워크플로우가 실행되면, piki 위키 리포지터리로 `repository_dispatch` 이벤트를 전송합니다.
> src: .github@2e7f8ab9:.github/workflows/piki-sync.yml
- **페이로드**: 이벤트 페이로드에는 이 리포지터리의 이름(`.github`)과 변경이 발생한 커밋의 SHA가 포함됩니다. 이 정보는 위키 리포지터리의 수신 워크플로우가 어떤 리포지터리의 어떤 변경 사항을 처리해야 할지 결정하는 데 사용됩니다.
> src: .github@2e7f8ab9:.github/workflows/piki-sync.yml

다른 모든 소스 리포지터리에도 `[piki.repo.workflow.yml.tmpl](../../templates/piki.repo.workflow.yml.tmpl.md)` 템플릿을 기반으로 한 유사한 동기화 워크플로우가 설치됩니다.

## 관련
- `[.github 리포지터리 개요](../../overview.md)`

## 변경 이력
- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [.github 리포지터리 개요](../../overview.md)
<!-- piki:backlinks-end -->
