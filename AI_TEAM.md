# Trang 3 — AI Team Design
# AI Team Architecture — Dự án Oto

## Squad Goal

> **"Team/Squad của chúng tôi sở hữu toàn bộ hệ thống quản lý mượn/trả sách của thư viện trường (Oto) và chịu trách nhiệm đưa nghiệp vụ thư viện từ hiện trạng ghi chép thủ công, tra cứu thủ công, dễ thất thoát sách đến trạng thái số hóa toàn diện — mượn/trả bằng quét mã, nhắc hạn tự động, báo cáo 1-click cho toàn trường."**

## Lựa chọn: **Centralized**

Team Oto hiện chỉ có 3 thành viên (Founder/PM, AI Engineer, Member khác phụ trách Data/QA/UX) đang cùng làm 1 sản phẩm MVP duy nhất trong 1–2 tháng (theo RACI Matrix), nên một team AI/kỹ thuật tập trung, dùng chung là phù hợp nhất — quy mô quá nhỏ để tách người "embedded" vào từng phòng ban (Thư viện, Đào tạo, IT) hay chạy mô hình Hybrid, vốn cần nhiều nhóm sản phẩm song song để phân bổ nguồn lực.

Mô hình Centralized còn giúp AI Engineer (Đức Anh) giữ quyền Accountable xuyên suốt cho kiến trúc & chất lượng kỹ thuật MVP (RACI hàng 3), dễ đảm bảo tính nhất quán giữa các khâu chuẩn bị dữ liệu, xây dựng và kiểm thử — thay vì phân tán quyết định kỹ thuật cho nhiều nhóm embedded riêng lẻ ở giai đoạn pilot còn nhiều rủi ro (chưa số hóa dữ liệu, chưa có sự ủng hộ đầy đủ từ Thủ thư và IT).

Khi sản phẩm qua giai đoạn pilot và mở rộng ra toàn trường (RACI hàng 6, do Hiệu trưởng quyết định), có thể cân nhắc chuyển dần sang Hybrid — giữ 1 lõi kỹ thuật trung tâm nhưng cử người hỗ trợ trực tiếp (embedded) tại thư viện trong giai đoạn vận hành thực tế.

---

## Core Roles & Capability Gap

### Core — cần ngay

| Vai trò | Người đảm nhiệm | Tình trạng |
| :--- | :--- | :--- |
| **AI Product / Founder** | Trần Minh Quân | ✅ Có (kiêm PM — RACI: A hàng 1, 5) |
| **AI Engineer** | Nguyễn Đức Anh | ✅ Có (A hàng 3 — kiến trúc & MVP) |
| **Data / Backend** | Trần Thị Hường | ⚠️ Có nhưng kiêm nhiệm (A hàng 2 — chuẩn hóa/import dữ liệu, đồng thời QA/UX) |
| **Fullstack** | — | ❌ **Gap** — chưa có người chuyên xây UI + tích hợp backend hoàn chỉnh; hiện dồn vào AI Engineer |
| **UX** | Trần Thị Hường (kiêm) | ⚠️ **Gap một phần** — chỉ kiêm nhiệm, chưa có thời gian test UX sâu (phỏng vấn 3–5 SV mới ở mức đề xuất) |
| **Domain Expert** | — (chỉ ở vai trò Stakeholder/Consulted) | ❌ **Gap** — Thủ thư mới chỉ là **C** (Consulted) trong RACI, chưa có ai trong team nắm nghiệp vụ thư viện đủ sâu để thay mặt quyết định nghiệp vụ hằng ngày |

**Nhận xét:** Team 3 người đang gánh 6 vai trò core → Hường bị quá tải (Data + QA + UX), và thiếu hẳn Fullstack riêng + Domain Expert nội bộ. Rủi ro lớn nhất ngắn hạn: không ai "sống" trong nghiệp vụ thư viện hằng ngày để phản biện nhanh các quyết định sản phẩm.

**Giảm nhẹ gap trong 1–2 tháng tới (không cần tuyển thêm ngay):**
- Fullstack: AI Engineer đảm nhiệm luôn phần backend/API, Hường hỗ trợ phần UI đơn giản (MVP nhỏ, chưa cần tách riêng).
- Domain Expert: duy trì lịch shadowing định kỳ tại thư viện (RACI hàng 1) để "mượn" tri thức nghiệp vụ từ Thủ thư thay vì tuyển người mới.

### Extended — có thể cần khi scale

| Vai trò | Khi nào cần | Vì sao |
| :--- | :--- | :--- |
| **Forward Deployed Engineer** | Giai đoạn Pilot / Release toàn trường (RACI hàng 5–6) | Cần người túc trực tại thư viện hỗ trợ kỹ thuật trực tiếp, xử lý sự cố quét mã vạch/nhập liệu thực tế theo đúng cam kết trong Pitch. |
| **MLOps / Evals** | Khi thêm tính năng AI thật sự (vd. OCR nhận diện mã sách cũ, gợi ý sách tự động) | MVP hiện tại chủ yếu là CRUD + quét mã, chưa cần; chỉ phát sinh khi mở rộng sang các tính năng học máy. |
| **Legal / Compliance** | Trước khi release toàn trường | Dữ liệu mượn/trả gắn với thông tin sinh viên — cần rà soát tuân thủ quy định bảo mật dữ liệu cá nhân/học đường trước khi Hiệu trưởng duyệt (RACI hàng 6). |
| **AI Ethics / Governance** | Khi hệ thống bắt đầu tự động hoá quyết định ảnh hưởng người dùng (vd. tự khoá tài khoản trễ hạn, xếp hạng ưu tiên mượn sách) | Chưa cần ở MVP; cần khi có logic tự động tác động trực tiếp đến quyền lợi sinh viên. |
| **Specialist theo domain (Tích hợp IT trường học)** | Giai đoạn tích hợp SSO/API với hệ thống Đào tạo (RACI: IT là C ở hàng 3, 6) | Nhân viên IT nhà trường hiện mới ở vai trò Consulted; nếu tích hợp phức tạp (SSO, đồng bộ dữ liệu SV) có thể cần chuyên gia tích hợp riêng. |

**Nguyên tắc áp dụng:** Không bắt buộc có đủ mọi vai trò — ưu tiên lấp gap Core bằng kiêm nhiệm/quy trình (shadowing, hợp tác chặt với Thủ thư) trước khi tuyển thêm; các vai trò Extended chỉ kích hoạt khi có tín hiệu scale rõ ràng (pilot thành công, mở rộng toàn trường, hoặc bổ sung tính năng AI thật sự).

---

## Ưu tiên bổ sung Capability Gap (Top 3)

**1. Domain expertise nghiệp vụ thư viện**
→ **Partner** với Thủ thư & thư viện trường
→ Vì: Team không cần tuyển full-time ở giai đoạn MVP; Thủ thư đã sẵn có tri thức nghiệp vụ chính xác nhất (quy trình mượn/trả, phân loại sách thực tế) mà không ai trong team có
→ Khi nào cần: **Trước Pilot đầu tiên** (RACI hàng 5, tuần 7–9) — duy trì qua shadowing định kỳ + vai trò Consulted trong RACI hàng 1–5

**2. Fullstack (xây UI + tích hợp MVP)**
→ **Outsource** một phần (thuê dev ngắn hạn/freelance theo sprint)
→ Vì: Team chỉ 3 người, AI Engineer đang gánh cả kiến trúc lẫn xây dựng MVP; dự án ngắn hạn 1–2 tháng không đủ khối lượng công việc để tuyển full-time, nhưng cần thêm sức tay để không trễ tiến độ
→ Khi nào cần: **Trước khi bắt đầu xây MVP** (RACI hàng 3, tuần 3–6)

**3. Legal/Compliance dữ liệu sinh viên**
→ **Partner** với phòng IT/Đào tạo của nhà trường
→ Vì: Nhà trường đã có sẵn quy định bảo mật dữ liệu và quy trình tuân thủ nội bộ; hợp tác tận dụng được kiến thức có sẵn thay vì tốn chi phí thuê luật sư ngoài cho một pilot quy mô nhỏ
→ Khi nào cần: **Trước khi trình Hiệu trưởng quyết định release toàn trường** (RACI hàng 6, tuần 9–10)
