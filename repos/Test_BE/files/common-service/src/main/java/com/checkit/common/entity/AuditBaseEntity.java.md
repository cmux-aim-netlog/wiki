---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
--- 
# AuditBaseEntity.java

이 파일은 데이터베이스 엔티티의 생성 및 수정 시간을 자동으로 기록하기 위한 추상 기본 클래스를 정의합니다.

## 목적

JPA Auditing 기능을 사용하여 `createdAt`과 `updatedAt` 필드를 관리합니다. 이 클래스를 상속하는 모든 엔티티는 데이터가 생성되거나 변경될 때 해당 필드가 자동으로 갱신됩니다.

## 구현

- `@MappedSuperclass`: 이 클래스의 필드들이 상속받는 엔티티의 테이블 컬럼으로 매핑되도록 합니다.
- `@EntityListeners(AuditingEntityListener.class)`: 엔티티의 영속성 이벤트를 감지하여 Auditing 로직을 적용합니다.
- `@CreatedDate`: 엔티티 생성 시 현재 시간이 자동으로 저장됩니다.
- `@LastModifiedDate`: 엔티티 수정 시 현재 시간이 자동으로 저장됩니다.

> src: Test_BE@4f502763:common-service/src/main/java/com/checkit/common/entity/AuditBaseEntity.java#L11-L20

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
