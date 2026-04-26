---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
--- 
# checkmate_postgres_ddl.sql

이 SQL 스크립트는 `Test_BE` 애플리케이션에서 사용하는 PostgreSQL 데이터베이스의 테이블 스키마를 정의합니다.

## 주요 테이블

- `users`: 사용자 정보를 저장하는 테이블.
- `inquiry`: 고객 문의사항 정보를 저장하는 테이블.
- `inquiry_comment`: 문의사항에 대한 댓글 정보를 저장하는 테이블.
- `category`: 카테고리 정보를 관리하는 테이블.

> src: Test_BE@4f502763:common-service/src/main/resources/db/checkmate_postgres_ddl.sql#L1-L60

각 테이블은 `created_at`과 `updated_at` 컬럼을 포함하여 데이터의 생성 및 수정 시점을 추적합니다. 이는 [AuditBaseEntity](../java/com/checkit/common/entity/AuditBaseEntity.java.md)와 연관됩니다.

## 관련

- [Test_BE 개요](../../../../../overview.md)

## 변경 이력

- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [Test_BE 개요](../../../../../../overview.md)
<!-- piki:backlinks-end -->
