# Weekly Review – Week 02

- Topic: Spring Boot fundamentals và request lifecycle
- Date: 2026-11-23
- Actual study hours: Chưa xác nhận
- Status: Completed — foundational level
- Assessment: 8/10 về mục tiêu tuần; 6/10 về hiệu quả phương pháp học (đánh giá định tính từ hội thoại)

## 1. Planned Objectives

- Spring Framework vs Spring Boot; Starter Dependencies; Auto Configuration.
- application.properties và profiles dev/test.
- HTTP request lifecycle (Tomcat, DispatcherServlet, HandlerMapping, HandlerAdapter).
- Filter và Interceptor cơ bản.
- Practical target: REST Category API, profile dev/test, interceptor logging, giải thích luồng request.

## 2. Completed Work and Evidence

- Giải thích đúng Maven resolve dependencies, Spring Boot áp dụng Auto Configuration có điều kiện.
- Đọc Conditions Evaluation Report từ project: XADataSourceAutoConfiguration matched classpath nhưng did not match vì thiếu XADataSourceWrapper Bean; hiểu vì sao config bị bỏ qua.
- Giải thích đúng HandlerMapping tìm getHotel() và HandlerAdapter hỗ trợ lời gọi.
- Trên project HotelBooking, tự chạy RequestLoggingInterceptor: console `GET /api/hello`.
- Mở rộng interceptor để đo thời gian xử lý, thử `Thread.sleep(500)`: console `GET /api/hello - 670 ms`, `516 ms`, `502 ms`. Đây là minh chứng thực hành, không phải benchmark hiệu năng.
- Chạy ứng dụng với Active profiles `dev` và `test` qua IntelliJ; người học xác nhận cả hai chạy được.
- Dùng Workbench export Structure Only từ schema thực tế `hotelmanagersystem` (4 bảng booking, customer, hotel, room); chỉnh dump để tạo schema `hotel_test`, xác nhận "done".
- Chưa nhận được bằng chứng query đối chiếu record đã POST giữa hai database. Chưa có bài REST Category riêng: dùng lại HotelBooking cho tính thực tiễn. Không xác nhận profile prod, YAML hay Filter tự triển khai.

## 3. Knowledge Evaluation

| Concept | Level | Evidence / Notes |
|---|---|---|
| Starter Dependencies | Good (foundations) | Phân biệt Maven và Boot |
| Auto Configuration | Basic-to-Good | Nắm điều kiện và có thực hành đọc report |
| Components configured by Boot | Basic | Chưa hiểu sâu công dụng của nhiều auto config |
| HTTP lifecycle | Basic | Biết DispatcherServlet, HandlerMapping, HandlerAdapter; chưa debug end-to-end |
| Filter vs Interceptor | Basic | Hiểu khác biệt ở tầng xử lý; Filter chưa thực hành |
| HandlerInterceptor | Good (task scope) | Logging và timing chạy thực tế |
| Spring Profiles | Good (task scope) | Chạy dev/test, database test được tạo; chưa kiểm chứng cách ly record |

## 4. Strengths

- Chuyển được kiến thức thành code logging/timing và cấu hình nhiều môi trường trên project sẵn có.
- Biết nhìn log để tìm điều kiện khiến Auto Configuration bị bỏ qua.
- Chủ động xác định khi nào kiến thức đang học chưa đem lại giá trị, đề xuất chỉnh phương pháp.

## 5. Weaknesses / Limits

- Nhiều khái niệm trừu tượng được giới thiệu quá sớm; bài học ít gắn lỗi thật ban đầu.
- Chưa debug trực tiếp toàn bộ HTTP lifecycle.
- Chưa tự triển khai Filter, chưa có thử nghiệm xác minh record ghi chỉ vào DB test.
- Actual study hours chưa xác nhận.

## 6. Unresolved Knowledge Gaps

- KG-007: HTTP request lifecycle end-to-end khi debug.
- KG-008: Vai trò của Auto Configuration components khi dự án phát sinh vấn đề.
- KG-009: Kiểm chứng cách ly dữ liệu giữa hotel_test và hotelmanagersystem.
- KG-002 (từ Week 01): JPA transaction là nội dung trọng tâm tuần kế.

## 7. Practical Assessment

- Task delivered: HotelBooking Interceptor (logging, timing) và profiles dev/test + test schema.
- Result: Có output console đo 670/516/502ms với sleep 500ms; người học xác nhận hai profile hoạt động và tạo test DB thành công.
- Evaluation: Đạt mục tiêu nền tảng Week 02; không nâng thành mastered.
- What required help: Hướng dẫn UI IntelliJ Active profiles, tạo/import schema từ dump, giải thích vai trò Filter/Interceptor.

## 8. Learning Reflection — User Feedback

Người học cảm nhận Week 02 **chưa thật sự năng suất**: quá nhiều lý thuyết mới, trừu tượng trước khi có tình huống sử dụng rõ ràng. Kiến thức vẫn có giá trị nền tảng và có thể đào sâu sau nếu gặp case tương ứng. Muốn thay đổi cách học theo hướng code và vấn đề thực tế.

### New Method from Week 03

**Problem → Implementation → Debug → Explanation → Review**

1. Bắt đầu với một vấn đề có thể tái hiện trên HotelBooking.
2. Trình bày rõ dùng khi nào, áp dụng ở class/file nào, kết quả mong đợi là gì.
3. Người học tự viết/chạy code và gửi output, mentor review.
4. Giải thích internals vừa đủ để hiểu kết quả hoặc xử lý lỗi; không hỏi suy luận về thuật ngữ hoàn toàn mới.
5. Review bằng khả năng triển khai, debug và giải thích code; không chạy theo checklist annotation.

Phân bổ định hướng 12–15 giờ/tuần: ~60% thực hành/debug, 25% lý thuyết gắn case, 15% review.

## 9. Decision

- [x] Move to Week 03
- [x] Adjust teaching method, retain selected knowledge gaps for case-based review
- [ ] Claim full Spring MVC/Auto Configuration mastery

Reason: Đã đạt những mục tiêu cốt lõi với evidence trong project; bài Category và Filter riêng không được thực hiện, ghi rõ giới hạn.

## 10. Next Week Priorities

1. JPA/Hibernate trên HotelBooking: sửa Entity trong và ngoài @Transactional, quan sát UPDATE.
2. Persistence Context, Entity lifecycle, Dirty Checking, Flush vs Commit qua log SQL.
3. Tự phân tích nguyên nhân và sửa một case JPA, giữ test DB riêng để thử nghiệm.

## 11. State Updates Required

- [x] CURRENT_STATE.md
- [x] PROGRESS.md
- [x] AI_CONTEXT.md (teaching method)
- [x] KNOWLEDGE_GAPS.md
- [ ] MISTAKES_LOG.md (không có lỗi code mới cần tách riêng)
