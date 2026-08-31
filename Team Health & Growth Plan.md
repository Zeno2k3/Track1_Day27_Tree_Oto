''' Competency Framework (khung năng lực) trong slide gồm L1 — AI Literate, L2 — AI Practitioner và L3 — AI Builder. Trong Lab, team dùng khung này để xác định mức hiện tại và năng lực cần nâng tiếp theo; không cần mất thời gian tranh luận chính xác về số tháng kinh nghiệm.'''

---

## Tự chấm Team Health (5')

Mỗi thành viên team Tree (dự án Oto) tự chấm điểm từ 1–5 cho 4 khía cạnh dưới đây, dựa trên tiến độ thực tế của sprint MVP hiện tại (chuẩn hóa dữ liệu, xây dựng, kiểm thử — theo RACI Matrix).

### Trần Minh Quân — AI Product / Founder

| Khía cạnh | Điểm 1–5 |
| :--- | :--- |
| Chất lượng AI | 3 |
| Tiến độ | 3 |
| Tinh thần team | 4 |
| Tốc độ ra sản phẩm | 2 |

### Nguyễn Đức Anh — AI Engineer

| Khía cạnh | Điểm 1–5 |
| :--- | :--- |
| Chất lượng AI | 3 |
| Tiến độ | 3 |
| Tinh thần team | 4 |
| Tốc độ ra sản phẩm | 3 |

### Trần Thị Hường — Data / QA / UX

| Khía cạnh | Điểm 1–5 |
| :--- | :--- |
| Chất lượng AI | 3 |
| Tiến độ | 2 |
| Tinh thần team | 3 |
| Tốc độ ra sản phẩm | 2 |

**Điểm trung bình team:** Chất lượng AI 3.0 · Tiến độ 2.7 · Tinh thần team 3.7 · Tốc độ ra sản phẩm 2.3

*Căn cứ ước lượng: MVP hiện chủ yếu là CRUD + quét mã (chưa có tính năng AI sâu) → Chất lượng AI ở mức trung bình; chưa có link demo/sản phẩm (README mục "Link sản phẩm/demo" còn trống) và 2/4 stakeholder trọng tâm (IT, Thủ thư) chưa ủng hộ → Tiến độ và Tốc độ ra sản phẩm thấp hơn; RACI đã phân vai rõ ràng nhưng Hường đang kiêm 3 vai trò (Data/QA/UX) → điểm của Hường ở Tiến độ/Tốc độ ra sản phẩm thấp nhất team.*

**Cách đọc kết quả:**
- Điểm trung bình mỗi khía cạnh **≤ 3** → cần thảo luận nguyên nhân ngay trong buổi retro (vd. Hường đang kiêm 3 vai trò Data/QA/UX nên "Tốc độ ra sản phẩm" hoặc "Tiến độ" có thể thấp).
- Chênh lệch lớn giữa các thành viên ở cùng một khía cạnh → dấu hiệu thiếu đồng bộ thông tin, cần đối chiếu lại kỳ vọng.

---

## Chọn Competency cần nâng cấp (5')

**Role:** AI Product / Founder (Trần Minh Quân)

**Level hiện tại (gần nhất):** L1 — AI Literate
→ Biết dùng AI để tra cứu, soạn nháp tài liệu (pitch, RACI, phân tích stakeholder trong `README.md`), nhưng chưa có quy trình chuẩn hóa để tự vận hành AI phục vụ ra quyết định sản phẩm — vẫn phụ thuộc AI Engineer khi cần đào sâu kỹ thuật.

**Competency cần nâng tiếp theo:** Structured prompting / Context engineering cho spec & requirement
→ Vì: Founder đang là người viết pitch, phân tích stakeholder và định hướng MVP (RACI hàng 1, 5) — nếu tự viết được prompt có cấu trúc (bối cảnh, ràng buộc, tiêu chí chấp nhận) để AI hỗ trợ soạn PRD/spec tính năng, sẽ giảm vòng lặp qua lại với AI Engineer và tăng tốc độ ra quyết định.

**Action trong 30 ngày:**
Mỗi tuần tự dùng AI viết 1 bản spec ngắn (1 trang, theo template cố định: Mục tiêu – Đối tượng dùng – Luồng chính – Tiêu chí chấp nhận) cho 1 tính năng MVP sắp làm (vd. mượn/trả, nhắc hạn, báo cáo 1-click), review cùng AI Engineer trước khi triển khai. Lặp lại 4 lần trong 30 ngày để chuẩn hóa thành thói quen viết spec có AI hỗ trợ, đo bằng số lần AI Engineer phải hỏi lại yêu cầu (mục tiêu: giảm dần qua từng tuần).

---

## Growth Plan 30 ngày (8')

| Vấn đề | Hành động 30 ngày | Owner | Deadline | Dấu hiệu hoàn thành |
| :--- | :--- | :--- | :--- | :--- |
| Chưa ai trong team nắm sâu nghiệp vụ thư viện; Thủ thư chưa ủng hộ (chỉ ở vai trò Consulted) | Shadowing nửa ngày tại thư viện để ghi lại quy trình mượn/trả/phân loại sách thực tế, sau đó demo giao diện quét mã cho Thủ thư | Trần Thị Hường | 2026-09-11 | Có biên bản shadowing (quy trình thực tế bằng văn bản) + Thủ thư xác nhận đồng ý lịch demo tiếp theo bằng tin nhắn/email |
| AI Engineer đang gánh cả kiến trúc lẫn xây UI (Fullstack gap), làm chậm tốc độ ra sản phẩm | Tìm và chốt 1 freelance/fullstack ngắn hạn theo sprint để nhận bàn giao module UI mượn/trả cơ bản | Nguyễn Đức Anh | 2026-09-18 | Có hợp đồng/thỏa thuận sprint đã ký với freelance, hoặc 1 module UI đã được bàn giao và AI Engineer review xong |
| Chưa có link demo/sản phẩm (mục "Link sản phẩm/demo" trong README còn trống), thiếu nhịp cập nhật tiến độ chung | Mỗi thứ Sáu họp review 20 phút với cả team, bắt đầu từ tuần này (2026-09-04), cập nhật link demo/staging vào README ngay khi có bản build đầu tiên | Trần Minh Quân | 2026-09-30 (duy trì 4 buổi liên tiếp) | Có ≥4 biên bản review thứ Sáu được ghi lại + README có link demo/staging trước 2026-09-30 |
