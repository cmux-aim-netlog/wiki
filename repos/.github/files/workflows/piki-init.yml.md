---
repo: .github
last_synced_commit: 2e7f8ab90e8e608c41c2974ec03d98058c54157e
---
# workflows/piki-init.yml

이 GitHub Actions 워크플로우는 새로운 리포지터리를 piki 위키 시스템에 등록하는 초기화 프로세스를 실행합니다.

## 주요 특징

- **수동 실행 (`workflow_dispatch`)**: 이 워크플로우는 자동으로 실행되지 않고, GitHub Actions UI에서 사용자가 직접 실행해야 합니다.
> src: .github@2e7f8ab9:.github/workflows/piki-init.yml
- **입력 파라미터**: 실행 시 piki 시스템에 온보딩할 대상 리포지터리의 이름을 파라미터로 전달받습니다.
> src: .github@2e7f8ab9:.github/workflows/piki-init.yml
- **스크립트 실행**: 워크플로우의 핵심 작업은 `[scripts/piki_init.py](../scripts/piki_init.py.md)` 스크립트를 실행하여 실제 초기화 로직을 수행하는 것입니다.
> src: .github@2e7f8ab9:.github/workflows/piki-init.yml

이 워크플로우를 통해 신규 프로젝트를 piki 위키와 간편하게 연동할 수 있습니다.

## 관련
- `[.github 리포지터리 개요](../../overview.md)`
- `[piki_init.py 스크립트](../scripts/piki_init.py.md)`

## 변경 이력
- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [scripts/piki_init.py](../scripts/piki_init.py.md)
- [.github 리포지터리 개요](../../overview.md)
<!-- piki:backlinks-end -->
