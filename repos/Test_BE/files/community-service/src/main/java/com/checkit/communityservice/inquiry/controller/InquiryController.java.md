---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
--- 
# InquiryController.java

이 파일은 문의사항(Inquiry) 관련 HTTP 요청을 처리하는 REST 컨트롤러입니다.

## 엔드포인트

- **Base Path**: `/api/inquiries`

> src: Test_BE@4f502763:community-service/src/main/java/com/checkit/communityservice/inquiry/controller/InquiryController.java#L16-L17

- `GET /`: 모든 문의사항 목록 조회
- `POST /`: 새 문의사항 등록
- `GET /{inquiryId}`: 특정 문의사항 상세 조회
- `PATCH /{inquiryId}`: 특정 문의사항 수정
- `DELETE /{inquiryId}`: 특정 문의사항 삭제

모든 응답은 [ApiResponse](../../../../../../common-service/src/main/java/com/checkit/common/dto/ApiResponse.java.md) 객체로 래핑되어 반환됩니다.

## 관련

- [API 문서](../../../../../../api.md)

## 변경 이력

- 2026-04-26: 최초 생성

<!-- piki:backlinks-start -->
## Backlinks
_Pages that link to this one (auto-generated)._

- [Test_BE API](../../../../../../../../../../api.md)
<!-- piki:backlinks-end -->
