# Learning Progress

> Cập nhật sau mỗi weekly review. Không tự ước lượng completion nếu chưa có bằng chứng.

| Week | Topic | Status | Completion | Evidence / Review |
|---:|---|---|---:|---|
| 01 | Spring IoC, DI, Bean | Completed | 100% | [Review Week 01](03_ASSESSMENTS/WEEKLY_REVIEWS/REVIEW_WEEK_01.md); bài Notification System (`Week01_test.zip`, review trong chat 2026-11-16) |
| 02 | Spring Boot fundamentals, request lifecycle | Completed (foundational) | 100% | [Review Week 02](03_ASSESSMENTS/WEEKLY_REVIEWS/REVIEW_WEEK_02.md); HotelBooking interceptor logging/timing, dev/test profiles và test DB |
| 03 | JPA/Hibernate internals | Not Started | 0% | — |
| 04 | Query và tối ưu truy vấn | Not Started | 0% | — |
| 05 | Database design và transaction | Not Started | 0% | — |
| 06 | DTO và MapStruct nâng cao | Not Started | 0% | — |
| 07 | Validation và exception handling | Not Started | 0% | — |
| 08 | REST API design | Not Started | 0% | — |
| 09 | Spring Security fundamentals | Not Started | 0% | — |
| 10 | JWT authentication | Not Started | 0% | — |
| 11 | Authorization | Not Started | 0% | — |
| 12 | Unit testing | Not Started | 0% | — |
| 13 | Integration testing | Not Started | 0% | — |
| 14 | Architecture và clean code | Not Started | 0% | — |
| 15 | Docker và deployment | Not Started | 0% | — |
| 16 | Portfolio và phỏng vấn | Not Started | 0% | — |

## Milestones

- [x] Complete Spring Core (Week 1–2) — foundational; remaining gaps in reviews
- [ ] Complete JPA and Database (Week 3–5)
- [ ] Complete REST API design (Week 6–8)
- [ ] Complete Spring Security (Week 9–11)
- [ ] Complete Testing (Week 12–13)
- [ ] Complete Architecture and Deployment (Week 14–15)
- [ ] Finish Portfolio (Week 16)

## Weekly Notes

- Week 01 (2026-11-16): Hoàn thành mục tiêu nền tảng IoC/DI, Bean, Scope, Lifecycle, Constructor Injection, Configuration và Component Scanning; tự viết bài Notification System cơ bản. Đánh giá hướng dẫn 8.5/10, không phải điểm kiểm thử tự động. Bản ZIP đã review dùng @Primary và chưa gọi send(); người học báo đã chỉnh @Qualifier và send() nhưng chưa gửi lại để kiểm chứng. Thời lượng thực học chưa xác nhận.

- Week 02 (2026-11-23): Đạt mục tiêu nền tảng, thực hành logging `GET /api/hello`, đo 670/516/502 ms khi `Thread.sleep(500)`, cấu hình dev/test, tạo schema `hotel_test` từ structure-only dump. Chưa có đối chiếu bản ghi cụ thể chứng minh tách dữ liệu; chưa làm REST Category riêng (dùng HotelBooking). Đánh giá mục tiêu 8/10, hiệu quả phương pháp 6/10 (chủ quan). Đổi phương pháp sang Problem → Implementation → Debug → Explanation → Review; review chi tiết trong REVIEW_WEEK_02.md.
