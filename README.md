# Track1_Day27_Tree_Oto
# Track 1 - Day 27 — AI Team Lab

- Team: Tree
- Thành viên:
    Trần Minh Quân - 2A202601768
    Nguyễn Đức Anh - 2A202601624
    Trần Thị Hường - 2A202601648
- Tên dự án: Oto
- Link sản phẩm/demo (nếu có):

- Mô tả dự án: Xây dựng app cho quản lý thư viện cho nhà trường.

- Stakeholder: 
    Thủ thư trường học,
    Sinh viên,
    Hiệu trưởng,
    Thư ký Hiệu Trưởng
    Nhân viên IT (quản trị kỹ thuật),
    Ban quản lý tài sản (sách, thiết bị).

| Ủng hộ | Trung lập | Chưa ủng hộ |
| :--- | :--- | :--- |
| Hiệu trưởng | Thủ thư trường học | Nhân viên IT (quản trị kỹ thuật) |
| Bộ phận đào tạo | Sinh viên | Ban quản lý tài sản (sách, thiết bị) |

- **2 stakeholder đang ủng hộ mạnh:**
    + Sinh viên
    + Hiệu trưởng
- **2 stakeholder chưa ủng hộ / có rủi ro cản trở để ưu tiên thuyết phục:**
    + Nhân viên IT (quản trị kỹ thuật)
    + Thủ thư trường học

---

### Bảng phân tích chi tiết 4 Stakeholder trọng tâm

| Stakeholder | Phân loại | Họ quan tâm điều gì? | Họ có thể giúp / cản trở thế nào? | Hành động cụ thể của team (1–2 tuần tới) |
| :--- | :--- | :--- | :--- | :--- |
| **Sinh viên** | Ủng hộ mạnh | • Tra cứu sách/vị trí kệ nhanh chóng, kiểm tra tình trạng còn/hết.<br>• Mượn/trả/gia hạn online tiện lợi, nhận thông báo hạn trả sách tự động. | • **Giúp:** Lực lượng người dùng đông đảo, tham gia thử nghiệm (Beta test), đưa feedback thực tế và lan tỏa sản phẩm.<br>• **Cản trở:** Dễ bỏ dùng nếu app nhiều lỗi hoặc trải nghiệm phức tạp. | • Tạo khảo sát (Google Form) lấy ý kiến 30–50 sinh viên về nhu cầu mượn/trả.<br>• Phỏng vấn sâu 3–5 sinh viên với bản mockup/wireframe để test UX. |
| **Hiệu trưởng** | Ủng hộ mạnh | • Thúc đẩy chuyển đổi số học đường, nâng cao văn hóa đọc và chất lượng học tập.<br>• Tối ưu chi phí, đảm bảo an toàn dữ liệu, tiến độ triển khai đúng hạn. | • **Giúp:** Người phê duyệt cao nhất (Sponsor), cấp ngân sách và chỉ đạo các phòng ban (IT, Đào tạo, Thư viện) phối hợp.<br>• **Cản trở:** Ngưng phê duyệt/chuyển nguồn lực nếu dự án không chứng minh được tính khả thi. | • Soạn bản tóm tắt dự án (1-page Executive Summary) gồm mục tiêu, lộ trình và lợi ích.<br>• Đặt lịch báo cáo ngắn (10–15 phút) qua Thư ký Hiệu trưởng để xin định hướng. |
| **Nhân viên IT** *(Quản trị kỹ thuật)* | Chưa ủng hộ / Rủi ro cản trở | • Bảo mật dữ liệu nhà trường/sinh viên.<br>• Khả năng tích hợp với hệ thống hiện tại (SSO, Cổng Đào tạo).<br>• Gánh nặng bảo trì và quản trị hạ tầng server. | • **Giúp:** Cấp hạ tầng, hỗ trợ API đồng bộ tài khoản, phê duyệt kỹ thuật.<br>• **Cản trở:** Từ chối cấp quyền truy cập API/DB, kéo dài thời gian thẩm định kỹ thuật, đánh giá không an toàn. | • Soạn tài liệu kiến trúc kỹ thuật (System Architecture, Tech Stack, Security & Data Flow).<br>• Họp trực tiếp với Trưởng nhóm IT để thống nhất phương án tích hợp và cam kết hỗ trợ vận hành. |
| **Thủ thư trường học** | Chưa ủng hộ / Rủi ro cản trở | • Sợ phần mềm phức tạp, làm xáo trộn thói quen làm việc cũ.<br>• Ngại tốn công sức nhập liệu danh mục sách thủ công.<br>• Lo lắng rủi ro thất thoát sách hoặc sai lệch dữ liệu. | • **Giúp:** Cung cấp nghiệp vụ mượn/trả thực tế chuẩn xác, trực tiếp hướng dẫn sinh viên dùng app.<br>• **Cản trở:** Không cập nhật dữ liệu trên app, tiếp tục dùng sổ sách/Excel cũ, báo cáo phản ánh tiêu cực. | • Đến thư viện quan sát thực tế quy trình (Shadowing) nửa ngày để nắm rõ khó khăn.<br>• Demo giao diện quản trị (quét mã vạch nhanh, xuất báo cáo 1-click) và cam kết đào tạo, hỗ trợ nhập liệu. |



Họ quan tâm điều gì?
Họ có thể giúp hoặc cản trở dự án thế nào?
Hành động cụ thể của team trong 1–2 tuần tới là gì?


---

## 🧭 RACI Matrix — Dự án Oto (6 công việc trọng tâm, 1–2 tháng tới)

**Quy ước:** **R** = Responsible (người trực tiếp làm) · **A** = Accountable (chịu trách nhiệm cuối cùng, mỗi hàng đúng **1 A**) · **C** = Consulted (hỏi ý kiến trước khi quyết) · **I** = Informed (được thông báo sau khi quyết).

**Vai trò:** Founder/PM = Trần Minh Quân · AI Engineer = Nguyễn Đức Anh · Member khác (Data/QA/UX) = Trần Thị Hường · Stakeholder = Thủ thư (user chính) & Hiệu trưởng (sponsor).

| # | Công việc | Thời gian | Founder/PM<br>(Quân) | AI Engineer<br>(Đức Anh) | Member khác<br>(Hường) | Thủ thư<br>(user chính) | Hiệu trưởng<br>(sponsor) |
| :-: | :--- | :--- | :-: | :-: | :-: | :-: | :-: |
| 1 | **Xác định use case & chốt phạm vi MVP** (khảo sát 30–50 SV, shadowing thư viện nửa ngày) | Tuần 1–2 | **A**, R | C | R | C | I |
| 2 | **Chuẩn bị dữ liệu** (chuẩn hóa + import Excel cũ, dán mã vạch 20% đầu sách hay mượn) | Tuần 2–5 | C | R | **A**, R | C | I |
| 3 | **Xây MVP** (mượn/trả bằng quét mã, nhắc hạn tự động, báo cáo 1-click) | Tuần 3–6 | C | **A**, R | R | C | I |
| 4 | **Kiểm thử** (QA nội bộ + UAT nghiệp vụ với thủ thư) | Tuần 6–7 | I | R | **A**, R | C | I |
| 5 | **Demo/Pilot 1 kệ (hoặc 1 thể loại) trong 2 tuần** | Tuần 7–9 | **A**, R | R | R | C | I |
| 6 | **Quyết định release toàn thư viện** | Tuần 9–10 | R | C | I | C | **A** |

### Giải thích các lựa chọn quan trọng
- **Hàng 2 — A thuộc về Hường, không phải PM:** cam kết trong bản Pitch là *"việc nhập liệu là của team, không phải của thư viện"*, nên phải có 1 người chịu trách nhiệm cuối cùng về chất lượng dữ liệu. Thủ thư chỉ ở mức **C** (duyệt lại danh mục sau khi team nhập xong).
- **Hàng 3 — A thuộc về AI Engineer:** người duy nhất chịu trách nhiệm cuối về kiến trúc và chất lượng kỹ thuật của MVP; PM là **C** để chốt thứ tự ưu tiên tính năng, tránh phình phạm vi.
- **Hàng 4 — người xây không tự nghiệm thu:** Hường (**A**) sở hữu bộ test case và biên bản UAT, Đức Anh (**R**) sửa lỗi → giữ được tính khách quan.
- **Hàng 6 — A thuộc về Hiệu trưởng:** đây là quyết định về ngân sách và phạm vi toàn trường, vượt thẩm quyền của team; PM chỉ **R** (làm báo cáo kết quả pilot và đề xuất). Thủ thư là **C** vì có quyền phủ quyết thực tế theo cam kết *"sau 2 tuần thấy việc nặng hơn thì team dừng ngay"*.
- **Nhân viên IT** là **C** ở hàng 3 (thống nhất phương án tích hợp SSO/API, bảo mật) và hàng 6 (xác nhận sẵn sàng hạ tầng vận hành); **I** ở các hàng còn lại.
- **Sinh viên** là **C** ở hàng 1 (khảo sát nhu cầu) và hàng 5 (feedback khi pilot); **I** ở các hàng còn lại.

### Kiểm tra quy tắc
- ✅ Mỗi hàng có **đúng 1 chữ A**.
- ✅ **A được phân tán** (PM: 2 · AI Engineer: 1 · Member khác: 2 · Hiệu trưởng: 1) — không dồn hết trách nhiệm lên PM.
- ✅ Mỗi hàng đều có ít nhất 1 **R** để công việc thực sự có người làm.
