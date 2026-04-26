---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
---
# Test_BE 코딩 컨벤션

이 문서는 `Test_BE` 프로젝트에서 따르는 주요 코딩 컨벤션 및 설계 패턴을 설명합니다.

## 1. 표준 API 응답 형식

모든 API 응답은 `ApiResponse` DTO로 감싸서 반환합니다. 이를 통해 클라이언트는 일관된 형식으로 응답을 처리할 수 있습니다.

> src: Test_BE@4f502763:common-service/src/main/java/com/checkit/common/dto/ApiResponse.java#L8-L13

- **관련 문서**: [ApiResponse.java](./files/common-service/src/main/java/com/checkit/common/dto/ApiResponse.java.md)

## 2. 사용자 정의 예외 처리

비즈니스 로직 상의 예외는 `BusinessException`을 사용하여 처리합니다. 이 예외는 에러 코드와 메시지를 포함하는 `CommonCode` 열거형과 함께 사용됩니다.

> src: Test_BE@4f502763:common-service/src/main/java/com/checkit/common/exception/BusinessException.java#L10-L13

- **관련 문서**: [BusinessException.java](./files/common-service/src/main/java/com/checkit/common/exception/BusinessException.java.md)

## 3. 엔티티 생성/수정 시간 자동화

데이터베이스 엔티티는 `AuditBaseEntity`를 상속하여 생성 시간(`createdAt`)과 수정 시간(`updatedAt`)을 자동으로 기록합니다. 이는 JPA의 Auditing 기능을 통해 구현됩니다.

> src: Test_BE@4f502763:common-service/src/main/java/com/checkit/common/entity/AuditBaseEntity.java#L11-L20

- **관련 문서**: [AuditBaseEntity.java](./files/common-service/src/main/java/com/checkit/common/entity/AuditBaseEntity.java.md)

## 4. QueryDSL 사용

컴파일 시점에 타입 체크가 가능한 동적 쿼리를 생성하기 위해 QueryDSL을 사용합니다. `common-service/src/main/generated` 디렉토리에서 생성된 Q-Type 클래스들을 확인할 수 있습니다.

> src: Test_BE@4f502763:common-service/src/main/generated/com/checkit/common/entity/QAuditBaseEntity.java#L1-L26

## 변경 이력

- 2026-04-26: 최초 생성
