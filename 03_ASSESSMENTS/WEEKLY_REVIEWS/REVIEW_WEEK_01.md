# Weekly Review – Week 01

- Topic: Spring IoC và Dependency Injection
- Date: 2026-11-16
- Actual study hours: Chưa xác nhận (không suy diễn từ planned effort)
- Status: Completed — foundational objectives met
- Guided assessment: 8.5/10 (đánh giá hội thoại và code, không phải automated test)

## 1. Planned Objectives

- Hiểu Spring Container, ApplicationContext, IoC và DI.
- Phân biệt Bean, Scope, Lifecycle và Constructor Injection.
- Phân biệt @Component / @Service với @Configuration / @Bean và Component Scanning.
- Tự cấu hình, inject Bean và giải thích cơ chế.

## 2. Completed Work and Evidence

- Trả lời đúng các tình huống IoC/DI, default Singleton, Prototype, @Primary/@Qualifier và Component Scanning sau khi được hướng dẫn.
- Tự viết cấu hình @Bean PaymentClient, Constructor Injection vào PaymentService.
- Tự viết ví dụ EmailService scope prototype với constructor, @PostConstruct, @PreDestroy và ApplicationContext; chưa có console output được gửi để xác minh.
- Viết project Notification System, gửi `Week01_test.zip` (đã review qua hội thoại): NotificationSender, EmailSender, SmsSender, NotificationService và AppConfig; @Component, @Bean, @Primary, lifecycle annotations.
- Trong ZIP ban đầu, NotificationService mới inject nhưng chưa gọi send(), và dùng @Primary thay @Qualifier. Người học báo đã sửa và hiểu; chưa gửi code đã sửa.
- Không ghi nhận số giờ học hoặc kết quả chạy thực tế khi chưa được cung cấp.

## 3. Knowledge Evaluation

| Concept | Before | After | Evidence / Notes |
|---|---|---|---|
| IoC/DI | Basic | Good (fundamentals) | Giải thích Spring cấp dependency, biết chuỗi phụ thuộc khi Bean thiếu |
| Bean và Scope | Basic | Good (fundamentals) | Dự đoán đúng Singleton/Prototype và prototype inject vào Singleton |
| Constructor Injection | Basic | Good | Tự viết PaymentService với final dependency |
| @Configuration / @Bean | Basic | Good | Tự viết AppConfig đăng ký PaymentClient và SmsSender |
| Component Scanning | Not Assessed | Good (theory) | Giải thích đúng package scan và Bean từ method @Bean |
| @Primary / @Qualifier | Not Assessed | Basic | Hiểu cơ chế ưu tiên và chọn Bean; @Qualifier tự báo đã chỉnh |
| Bean Lifecycle | Weak misconception | Basic-to-Good | Sửa hiểu nhầm @PreDestroy, viết demo; chưa quan sát console được xác nhận |

Level guide:
- Good: Giải thích và áp dụng độc lập trong phạm vi đã kiểm chứng.
- Basic: Hiểu ý chính nhưng cần gợi ý hoặc thêm thực hành.
- Weak: Chưa giải thích/áp dụng được.
- Not Assessed: Chưa có đủ bằng chứng.

## 4. Strengths

- Tự diễn giải cơ chế Spring Container, không chỉ học thuộc annotation.
- Chủ động đặt câu hỏi về cách dùng @Bean trong AppConfig.
- Tự viết nhiều ví dụ code và bài Notification System thay vì chỉ xem lời giải.
- Hiểu rằng Bean SmsSender vẫn được tạo theo Singleton mặc định ngay cả khi không được chọn để inject.

## 5. Weaknesses

- Lúc đầu nhầm @PreDestroy với việc Bean không còn được sử dụng.
- Lúc đầu nhầm getBean() với quá trình Spring khởi tạo Singleton.
- Chưa quen dùng @Qualifier; chưa kiểm chứng code cuối sau chỉnh sửa.
- Chưa có output thực tế của bài lifecycle để đối chiếu trình tự.

## 6. Unresolved Knowledge Gaps

- KG-001: Lifecycle cần kiểm chứng output thực tế.
- KG-004: Eager Singleton vs getBean().
- KG-005: @Qualifier với nhiều implementation.
- KG-006: Prototype injected into Singleton ở tình huống phức tạp.

## 7. Practical Assessment

- Task: Notification System với interface, hai implementation, @Component, @Bean, Constructor Injection, Bean lifecycle, @Qualifier và ApplicationContext.
- Result: Bài ZIP ban đầu đáp ứng hầu hết nội dung; dùng @Primary thay @Qualifier, chưa gọi send() trong service/main. Người học đã thông báo tự bổ sung các phần đó.
- Evaluation: Đạt mục tiêu nền tảng Week 01; phiên bản cuối chưa được kiểm chứng.
- What required help: Giải thích @Qualifier, thứ tự khởi tạo Singleton, thời điểm @PreDestroy.

## 8. Decision

- [x] Move to next week
- [x] Repeat selected topics (lồng vào thực hành Week 02)
- [ ] Adjust next week's scope

Reason:
Đạt Definition of Done Week 01 ở mức cơ bản: giải thích được IoC/DI, phân biệt @Bean và @Component, sử dụng Constructor Injection, tự viết @Configuration và project đăng ký/inject Bean. Các chỗ thiếu bằng chứng được giữ như knowledge gaps, không coi là đã thành thạo.

## 9. Next Week Priorities

1. Học Spring Boot fundamentals và request lifecycle theo roadmap.
2. Vận dụng @Qualifier/@Primary và dự đoán thời điểm tạo Singleton trong dự án nhỏ.
3. Quan sát log Bean Lifecycle; tiếp tục practice Controller/Service và dependency.

## 10. State Updates Required

- [x] CURRENT_STATE.md
- [x] PROGRESS.md
- [ ] AI_CONTEXT.md (không cần cập nhật trong lần đồng bộ này)
- [x] KNOWLEDGE_GAPS.md
- [ ] MISTAKES_LOG.md (các lỗi đã ghi rõ trong review và gaps)
