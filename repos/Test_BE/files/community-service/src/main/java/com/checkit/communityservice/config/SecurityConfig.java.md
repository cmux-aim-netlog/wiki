---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
--- 
# SecurityConfig.java

이 파일은 `community-service` 모듈의 Spring Security 설정을 담당합니다.

## 주요 설정

- **HTTP 보안**: `http.authorizeHttpRequests()`를 통해 HTTP 요청에 대한 인가 규칙을 설정합니다.
- **CSRF 비활성화**: `http.csrf(AbstractHttpConfigurer::disable)`를 통해 CSRF(Cross-Site Request Forgery) 보호 기능을 비활성화합니다. 이는 주로 Stateless한 REST API 환경에서 사용됩니다.
- **세션 관리**: `http.sessionManagement(session -> session.sessionCreationPolicy(SessionCreationPolicy.STATELESS))`를 통해 세션을 사용하지 않는 Stateless 방식으로 서버를 운영하도록 설정합니다. 이는 JWT와 같은 토큰 기반 인증에 적합합니다.

현재 설정에서는 모든 요청(`anyRequest()`)에 대해 접근을 허용(`permitAll()`)하고 있습니다. 이는 개발 초기 단계의 설정일 수 있으며, 프로덕션 환경에서는 보다 엄격한 규칙이 필요할 수 있습니다.

> src: Test_BE@4f502763:community-service/src/main/java/com/checkit/communityservice/config/SecurityConfig.java#L17-L24

## 관련

- [Test_BE 개요](../../../../../overview.md)

## 변경 이력

- 2026-04-26: 최초 생성
