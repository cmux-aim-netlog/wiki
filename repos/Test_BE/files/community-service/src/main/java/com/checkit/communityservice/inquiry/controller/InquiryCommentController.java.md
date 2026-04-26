---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
--- 
# InquiryCommentController.java

이 파일은 문의사항(Inquiry)에 대한 댓글(Comment) 관련 HTTP 요청을 처리하는 REST 컨트롤러입니다.

## 엔드포인트

- **Base Path**: `/api/inquiries/{inquiryId}/comments`

> src: Test_BE@4f502763:community-service/src/main/java/com/checkit/communityservice/inquiry/controller/InquiryCommentController.java#L14-L15

- `POST /`: 새 댓글 등록
- `PATCH /{commentId}`: 특정 댓글 수정
- `DELETE /{commentId}`: 특정 댓글 삭제

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
