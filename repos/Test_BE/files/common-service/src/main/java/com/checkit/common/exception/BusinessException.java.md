---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
--- 
# BusinessException.java

이 파일은 애플리케이션의 비즈니스 로직과 관련된 예외 상황을 처리하기 위한 사용자 정의 예외 클래스를 정의합니다.

## 목적

`RuntimeException`을 상속하여, 예측 가능한 비즈니스 규칙 위반 상황(예: 잘못된 입력, 권한 없음)을 명시적으로 표현하는 데 사용됩니다. 이 예외는 `GlobalExceptionHandler`에 의해 처리되어 클라이언트에게 일관된 형식의 오류 응답을 반환합니다.

## 구조

`BusinessException`은 `CommonCode` 열거형을 멤버 변수로 가집니다. `CommonCode`는 각 예외 상황에 맞는 HTTP 상태 코드와 오류 메시지를 정의하고 있습니다.

> src: Test_BE@4f502763:common-service/src/main/java/com/checkit/common/exception/BusinessException.java#L10-L13

> src: Test_BE@4f502763:common-service/src/main/java/com/checkit/common/exception/CommonCode.java#L8-L16

## 관련

- [코딩 컨벤션](../../../conventions.md)
- [Test_BE 개요](../../../overview.md)

## 변경 이력

- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [Test_BE 코딩 컨벤션](../../../../../../../../../conventions.md)
<!-- piki:backlinks-end -->
