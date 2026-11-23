# Knowledge Gaps

> Theo dõi những khái niệm chưa hiểu hoặc chưa áp dụng độc lập được.

| ID | Topic | Gap / Symptom | Priority | Status | Next Action | Evidence to Resolve |
|---|---|---|---|---|---|---|
| KG-001 | Spring Bean Lifecycle | Đã giải thích đúng callback Singleton/Prototype và viết code minh họa; chưa kiểm chứng console và lifecycle nhiều dependency | Medium | Needs Review | Thực chạy demo và giải thích constructor, @PostConstruct, @PreDestroy, context.close() | Console + giải thích đúng cả singleton/prototype và mối quan hệ dependency |
| KG-002 | JPA Transaction | Cần xác minh độ sâu | High | Open | Ôn khi đến tuần 3 | Giải thích commit/rollback và thực hành |
| KG-003 | MapStruct nested mapping | Cần thêm thực hành | Medium | Open | Thực hành tuần 6 | Mapping DTO lồng nhau và update entity |
| KG-004 | Singleton Initialization vs getBean() | Từng nhầm thời điểm tạo Bean với getBean() | Medium | Needs Review | Dự đoán/log quá trình startup và getBean() khi gặp case phù hợp | Giải thích và chứng minh Singleton eager mặc định, trường hợp @Lazy |
| KG-005 | @Qualifier với nhiều implementation | Sử dụng @Primary trong ZIP, ít dùng @Qualifier; báo đã sửa nhưng chưa gửi lại | Low | Needs Review | Thực hành chọn Email/SMS bằng @Qualifier trong Week 02 | Code chạy đúng khi có hai Bean cùng interface, giải thích @Qualifier và @Primary |
| KG-006 | Prototype injected into singleton | Hiểu qua ví dụ lý thuyết, chưa thực hành dependency phức tạp | Low | Open | Kiểm chứng trong bài demo Scope | Giải thích và demo đối tượng được inject một lần với prototype |
| KG-007 | Spring MVC request lifecycle | Biết vai trò Tomcat, DispatcherServlet, HandlerMapping, HandlerAdapter; chưa debug toàn bộ luồng | Low | Needs Review | Khi có lỗi HTTP mapping/binding, debug ngay trên endpoint HotelBooking | Giải thích nguồn lỗi và chỉ được tầng xử lý qua log/debugger |
| KG-008 | Auto Configuration components | Đọc được matched/did-not-match nhưng chưa rõ nhiều thành phần được cấu hình dùng để làm gì | Low | Needs Review | Chỉ khảo sát Auto Configuration liên quan khi project có vấn đề cụ thể | Debug được ít nhất một case thực tế dựa trên Condition Evaluation Report |
| KG-009 | Profile database isolation | Đã tạo hotel_test từ dump, chạy test profile; chưa gửi kết quả đối chiếu bản ghi với DB gốc | Medium | Needs Verification | POST test record và query cả hotel_test/hotelmanagersystem khi phù hợp | Bản ghi test chỉ xuất hiện trong hotel_test và đúng JDBC URL |

## Gap Details

### KG-001
- Current understanding: Giải thích đúng @PostConstruct sau tạo Bean và @PreDestroy khi đóng context cho Singleton; tự viết ví dụ lifecycle.
- What is unclear: Chưa có kết quả chạy thực tế; chưa kiểm chứng nhiều dependency.
- Why it matters: Tránh hiểu nhầm thứ tự khởi tạo và hủy Bean.
- Next action: Chạy demo log lifecycle và mô tả thứ tự chính xác.
- Evidence required to resolve: Log và giải thích đúng.
- Resolved date: —

### Template
- Current understanding:
- What is unclear:
- Why it matters:
- Next action:
- Evidence required to resolve:
- Resolved date:
