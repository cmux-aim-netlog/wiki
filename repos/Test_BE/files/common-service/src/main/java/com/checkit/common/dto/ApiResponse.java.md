---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
--- 
# ApiResponse.java

이 파일은 모든 API 응답에 대한 표준 래퍼(wrapper) 클래스를 정의합니다.

## 목적

클라이언트에게 일관된 응답 구조를 제공하기 위해 사용됩니다. 성공 여부, 상태 코드, 메시지, 그리고 실제 데이터(`result`)를 포함하는 제네릭 클래스입니다.

## 구조

- `isSuccess`: 요청 성공 여부 (boolean)
- `code`: HTTP 상태 코드 또는 비즈니스 코드 (String)
- `message`: 응답 메시지 (String)
- `result`: 실제 응답 데이터 (Generic Type `T`)

> src: Test_BE@4f502763:common-service/src/main/java/com/checkit/common/dto/ApiResponse.java#L16-L22

정적 팩토리 메서드 `onSuccess`와 `onFailure`를 통해 성공 및 실패 응답 객체를 쉽게 생성할 수 있습니다.

> src: Test_BE@4f502763:common-service/src/main/java/com/checkit/common/dto/ApiResponse.java#L30-L42

## 관련

- [API 문서](../../../api.md)
- [코딩 컨벤션](../../../conventions.md)

## 변경 이력

- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [Test_BE API](../../../../../../../../../api.md)
- [Test_BE 코딩 컨벤션](../../../../../../../../../conventions.md)
<!-- piki:backlinks-end -->
