---
repo: piki
last_synced_commit: 0012803588dcb14e23c3492764da54437ac5a5c9
---
# `piki/config.py`

이 모듈은 piki 애플리케이션의 설정을 관리합니다. `pydantic`과 `toml`을 사용하여 `piki.toml` 파일에서 설정을 로드하고 유효성을 검사하는 역할을 할 것으로 보입니다.

> src: piki@00128035:piki/config.py#L1-L6

`Config` 클래스는 위키 리포지토리, 소스 리포지토리 목록, LLM 설정 등 piki 운영에 필요한 모든 설정 정보를 담는 데이터 구조를 정의합니다.

> src: piki@00128035:piki/config.py#L9-L21

## 관련
- `[piki overview](../../overview.md)`

## 변경 이력
- 2026-04-26: 최초 생성
