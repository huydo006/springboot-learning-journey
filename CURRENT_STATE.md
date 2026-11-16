# Current Learning State

> Cập nhật sau mỗi weekly review. Đây là nguồn sự thật về trình độ hiện tại.

## Vị trí hiện tại

- Roadmap: 16 tuần
- Current Week: 02 (sắp bắt đầu; chưa học)
- Current Phase: Spring Core
- Current Topic: Spring Boot fundamentals, request lifecycle (tiếp theo)
- Completed Sessions: 1 learning/review cycle recorded (buổi thực tế không được đếm chi tiết)
- Last Updated: 2026-11-16
- Overall Status: Week 01 Completed; Week 02 Not Started

## Hồ sơ năng lực

| Năng lực | Mức hiện tại | Trạng thái | Bằng chứng / ghi chú |
|---|---|---|---|
| Java Core, OOP, Collections | Khá ổn | Stable | Tự viết được OOP và xử lý logic |
| Spring IoC/DI | Khá ở mức cơ bản | Practiced | Giải thích bằng lời, viết Constructor Injection và Notification System; cần luyện tình huống nhiều dependency |
| Spring Bean / Scope | Khá | Practiced | Phân biệt Bean và object, Singleton/Prototype, lifecycle; ví dụ EmailService prototype |
| Spring Configuration | Khá | Practiced | Tự viết @Configuration + @Bean cho PaymentClient và SmsSender |
| Component Scanning | Khá (lý thuyết) | Explained | Xác định đúng phạm vi quét package và @Bean tạo từ AppConfig |
| @Primary / @Qualifier | Cơ bản | Needs Practice | @Primary trong ZIP; người học báo đã tự sửa @Qualifier, chưa review code mới |
| Controller-Service-Repository | Cơ bản | Practiced | Đã làm CRUD |
| REST API | Cơ bản | Practiced | Đã xây dựng API CRUD |
| Spring Data JPA | Cơ bản | Needs Review | Đã học quan hệ entity, cascade, LAZY/EAGER |
| DTO | Cơ bản | Practiced | Hiểu DTO không cần giống Entity |
| MapStruct | Nhập môn | Needs Review | Đã thực hành mapping Hotel/Room |
| Validation | Đã tiếp xúc | Needs Assessment | Cần thực hành có hệ thống |
| Exception Handling | Chưa đánh giá | Not Assessed | — |
| Spring Security | Chưa học bài bản | Not Started | — |
| Testing | Chưa học bài bản | Not Started | — |
| Docker/Deployment | Chưa học bài bản | Not Started | — |

## Điểm mạnh hiện tại

- Có nền tảng Java OOP và Collections, đã triển khai CRUD bằng Spring Boot.
- Giải thích được IoC/DI, Singleton/Prototype, @Bean/@Component và Component Scanning bằng lời của mình.
- Tự viết ví dụ Constructor Injection, @Bean PaymentClient và code lifecycle.
- Có bài thực hành Notification System với interface, hai implementation, @Component, @Bean, @Primary và callback lifecycle.

## Điểm yếu / điều cần xác minh

- Phân biệt chính xác Spring khởi tạo Singleton lúc startup với việc lấy Bean qua getBean().
- Dùng @Qualifier thường xuyên trong bài thực hành; phiên bản sửa sau review chưa được kiểm chứng.
- Cần luyện scope/lifecycle với nhiều Bean phụ thuộc nhau; chưa xác nhận output console của các demo.
- Hiểu biết thực tế về persistence context, transaction và SQL do Hibernate sinh ra.
- Khả năng thiết kế business logic độc lập, viết test và giải thích kiến trúc.

## Ưu tiên tiếp theo

1. Week 02: Spring Boot fundamentals và request lifecycle theo roadmap.
2. Khi làm Week 02, lồng bài tập nhiều implementation (@Qualifier, @Primary) và kiểm tra khởi tạo Bean.
3. Sau này kiểm tra transaction/JPA, test và thiết kế business logic theo đúng tuần.

## Quy tắc cập nhật

- Chỉ nâng mức năng lực khi có bằng chứng: bài tập, code, giải thích hoặc assessment.
- Phân biệt `đã học` với `đã làm được độc lập`.
- Mỗi điểm yếu phải có next action cụ thể.
