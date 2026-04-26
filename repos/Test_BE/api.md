---
repo: Test_BE
last_synced_commit: 4f502763b133e8785567a61bb7b050fb7ddadb7d
---
# Test_BE API

이 문서는 `Test_BE` 리포지토리, 특히 `community-service` 모듈에서 제공하는 외부 API 엔드포인트를 설명합니다.

모든 API 응답은 표준화된 포맷을 따릅니다. 자세한 내용은 [ApiResponse](./files/common-service/src/main/java/com/checkit/common/dto/ApiResponse.java.md) 문서를 참조하세요.

## Inquiry API

문의사항(Inquiry)과 관련된 CRUD 작업을 처리합니다.

- **Controller**: `InquiryController`
- **Base Path**: `/api/inquiries`
- **세부 정보**: [InquiryController.java](./files/community-service/src/main/java/com/checkit/communityservice/inquiry/controller/InquiryController.java.md)

## Inquiry Comment API

문의사항에 대한 댓글(Comment)을 관리합니다.

- **Controller**: `InquiryCommentController`
- **Base Path**: `/api/inquiries/{inquiryId}/comments`
- **세부 정보**: [InquiryCommentController.java](./files/community-service/src/main/java/com/checkit/communityservice/inquiry/controller/InquiryCommentController.java.md)

## 변경 이력

- 2026-04-26: 최초 생성
