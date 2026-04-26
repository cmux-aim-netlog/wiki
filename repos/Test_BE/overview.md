---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
---
# Test_BE 개요

`Test_BE`는 CheckIt 서비스의 백엔드 애플리케이션입니다. Java와 Spring Boot 프레임워크를 기반으로 구축되었습니다.

## 아키텍처

이 저장소는 Gradle 멀티 모듈 프로젝트로 구성되어 있습니다.

- **`common-service`**: 여러 서비스 모듈 간에 공유되는 공통 코드를 포함합니다. 여기에는 DTO, 엔티티, 공통 예외 처리 및 데이터베이스 스키마 정의가 포함됩니다.
- **`community-service`**: 커뮤니티 관련 기능(예: 문의사항)을 담당하는 마이크로서비스입니다.

주요 기술 스택은 다음과 같습니다:
- Java & Spring Boot
- Gradle
- JPA (Hibernate) & QueryDSL
- PostgreSQL

## 주요 페이지

- **[API 문서](./api.md)**: `community-service`가 노출하는 API 엔드포인트 목록입니다.
- **[코딩 컨벤션](./conventions.md)**: 프로젝트 전반에 걸쳐 사용되는 주요 설계 패턴과 규칙입니다.
- **[Gotchas](./gotchas.md)**: 개발 시 주의해야 할 사항이나 잠재적인 문제입니다.
- **[DB 스키마](../Test_BE/files/common-service/src/main/resources/db/checkmate_postgres_ddl.sql.md)**: 데이터베이스 테이블 구조 정의 파일입니다.

## 변경 이력

- 2026-04-26: 최초 생성
