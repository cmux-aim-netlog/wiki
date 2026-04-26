---
type: concept
last_synced_at: 2026-04-26T09:05:53Z
links_to: ["Test_BE", "Test_FE"]
---
# CheckIt 서비스 아키텍처

CheckIt 서비스는 백엔드와 프론트엔드 애플리케이션으로 구성된 클라이언트-서버 아키텍처를 따릅니다. 각 애플리케이션은 별도의 리포지터리에서 관리됩니다.

## 구성 요소

### 백엔드: `Test_BE`

- **설명**: Java와 Spring Boot를 기반으로 하는 CheckIt 서비스의 백엔드입니다. 데이터베이스 관리, 비즈니스 로직 처리, 그리고 외부 클라이언트를 위한 REST API 제공을 담당합니다.
- **API**: `community-service` 모듈을 통해 문의사항(Inquiry) 및 댓글(Comment)과 관련된 API를 노출합니다.
- **관련 페이지**:
  - `[Test_BE overview](../repos/Test_BE/overview.md)`
  - `[Test_BE API](../repos/Test_BE/api.md)`

### 프론트엔드: `Test_FE`

- **설명**: React Native로 개발된 안드로이드 애플리케이션입니다. 사용자를 위한 UI를 제공하며, `Test_BE`에서 제공하는 API와 통신하여 서비스 기능을 구현합니다.
- **패키지 이름**: `com.checkmate`
- **관련 페이지**:
  - `[Test_FE overview](../repos/Test_FE/overview.md)`

## 상호 작용

`Test_FE` 애플리케이션은 사용자의 요청을 받아 `Test_BE`의 API 엔드포인트(예: `/api/inquiries`)로 전송합니다. `Test_BE`는 요청을 처리한 후 결과를 `Test_FE`에 반환하여 사용자에게 표시합니다.

이 두 리포지터리 간의 계약은 `Test_BE`에서 정의한 API 명세에 의해 결정됩니다. `[NEEDS HUMAN INPUT]` 프론트엔드에서 실제 API를 호출하는 코드의 위치나 구체적인 데이터 모델 매핑에 대한 문서는 아직 위키에 없습니다.
