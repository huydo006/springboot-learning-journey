# GitHub Sync Workflow

Quy trình đồng bộ nhật ký học tập với repository `huydo006/springboot-learning-journey`.

## Nguyên tắc

- ChatGPT chỉ ghi nhận điều đã thực sự diễn ra trong buổi học; không tự suy diễn kết quả hoặc đánh dấu thành thạo.
- Nội dung buổi học được soạn và review trước khi ghi lên GitHub.
- Chỉ cập nhật những file có thay đổi thực tế.
- Không ghi token, mật khẩu, dữ liệu cá nhân hoặc nội dung nhạy cảm vào repository.

## Sau mỗi buổi học

1. Người học nói: **"Tổng kết và đồng bộ repo"**.
2. ChatGPT tổng kết:
   - Nội dung đã học và khả năng giải thích bằng lời của mình.
   - Bài tập/code đã làm, mức độ độc lập và bằng chứng.
   - Điểm mạnh, điểm yếu, lỗi và nguyên nhân.
   - Câu hỏi còn mở và đề xuất buổi tiếp theo.
3. ChatGPT xác định các file cần thay đổi, thường gồm:
   - Tạo file session mới trong `02_SESSIONS/YYYY/WEEK_XX/SESSION_XX.md`.
   - Cập nhật `CURRENT_STATE.md` khi có thay đổi đã được kiểm chứng.
   - Bổ sung `03_ASSESSMENTS/KNOWLEDGE_GAPS.md` nếu phát hiện lỗ hổng mới hoặc có bằng chứng giải quyết gap.
   - Bổ sung `03_ASSESSMENTS/MISTAKES_LOG.md` nếu có lỗi đáng lưu lại.
   - Chỉ cập nhật `PROGRESS.md` hoặc weekly review khi có đủ căn cứ.
4. ChatGPT trình bày bản tóm tắt thay đổi để người học kiểm tra.
5. Sau khi người học xác nhận **"Đồng ý, cập nhật GitHub"**, ChatGPT tạo/cập nhật các file trên repository và báo lại đường dẫn cùng commit.
6. Nếu người học yêu cầu sửa, chỉnh nội dung trước khi ghi.

## Sau mỗi tuần

1. Đánh giá lại các mục tiêu trong `01_WEEKLY_PLANS/WEEK_XX.md`.
2. Tạo/cập nhật `03_ASSESSMENTS/WEEKLY_REVIEWS/REVIEW_WEEK_XX.md`.
3. Cập nhật `CURRENT_STATE.md`, `PROGRESS.md`, `AI_CONTEXT.md` và knowledge gaps khi phù hợp.
4. Chỉ chuyển tuần khi đạt Definition of Done hoặc đã ghi rõ phần cần học bù.

## Quy ước trạng thái

- `Not Started`: Chưa học.
- `In Progress`: Đang học.
- `Needs Review`: Đã tiếp xúc nhưng chưa đạt tiêu chí.
- `Completed`: Có bằng chứng giải thích và áp dụng độc lập.
- `Blocked`: Có trở ngại chưa giải quyết.

## Lệnh hội thoại gợi ý

- `Tổng kết buổi học`: soạn nội dung, chưa ghi GitHub.
- `Tổng kết và đồng bộ repo`: soạn nội dung, trình bày thay đổi và chờ xác nhận.
- `Đồng ý, cập nhật GitHub`: thực hiện các thay đổi đã được duyệt.
- `Review tuần này`: đánh giá tuần và đề xuất cập nhật review.
- `Đọc trạng thái repo`: đọc trạng thái hiện tại từ GitHub trước khi lên bài mới.
