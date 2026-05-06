# EVALMATE — Investor Package · Milestone 1

**Giải pháp AI viết Nhận Xét Học Bạ cho Giáo viên Tiểu học**
**Tạ Thị Thùy Dương - 2A202600287

---
`Day18-AI-Product-Finance-Model.xlsx` (Tab 1 Assumptions + Tab 2 Unit Economics) và `Product_Requirements_Document.docx`. Các sai lệch so với bản nháp trước được ghi chú rõ ở từng mục.

---

## Trang 1 · Bìa & Twitter Pitch

**Tên dự án:** EvalMate — Giải pháp AI viết nhận xét học bạ cho giáo viên tiểu học


### Twitter Pitch (280 ký tự)

> Mỗi kỳ, GV tiểu học VN mất **~13 giờ** viết **378 nhận xét TT27** theo kiểu copy-paste (9 loại × 42 HS × 2 phút). **EvalMate** tạo draft chuẩn 9 trường, bám sát JSON tiêu chí từng khối lớp. Review batch xong trong **< 3 giờ**, DAR đạt 70% (sửa < 5p). LTV/CAC **10×**. Gọi 500M VND seed: Q2 đạt 70%+ DAR, Q3 build export VnEdu, Q4 50 trường trả tiền.

---

## Trang 2–3 · Pitch Memo & Phân Tích Thị Trường

### 1. Bản Ghi Nhớ Giới Thiệu (Pitch Memo)

**Vấn đề**
Giáo viên tiểu học bị quá tải với **1.440 nhận xét định tính/năm** theo Thông tư 27 (9 loại nhận xét × 40 HS × 4 định kỳ = 1.440), tương đương **48 giờ/năm** — dẫn đến tình trạng copy-paste đối phó và làm mất giá trị theo dõi sự tiến bộ của trẻ.


**Insight cốt lõi**
Ngưỡng chấp nhận AI không nằm ở chất lượng văn bản tốt nhất mà ở **tốc độ chỉnh sửa**. Giáo viên sẽ dùng AI nếu 70%+ bản nháp chỉ cần sửa dưới 5 phút để hoàn thành.

**Giải pháp**
EvalMate dùng GPT-4o để tạo bản nháp 9 trường TT27 từ dữ liệu Excel, cho phép review hàng loạt và export chuẩn VnEdu/SMAS.

**Lợi thế cạnh tranh (Moat)**
Vòng lặp học tập từ hành vi chỉnh sửa của giáo viên *(Domain-learning flywheel)* giúp AI ngày càng viết đúng văn phong sư phạm Việt Nam.

---

### 2. Phân Tích Thị Trường

| Thị trường | Quy mô ước tính | Cơ sở |
|---|---|---|
| **TAM** — Tổng thể | 12M – 20M USD/năm | ~390.000 GV tiểu học tại Việt Nam |
| **SAM** — Mục tiêu | 4M – 6M USD/năm | ~200.000 GV khu vực đô thị có tiếp cận công nghệ |
| **SOM** — Thực tế (12–24 tháng) | 150K – 300K USD/năm | 5.000 – 10.000 người dùng sớm tại HN & HCM |


---

## Trang 4–5 · PRD & Tính Năng MVP

### 3. Tóm Tắt Yêu Cầu Sản Phẩm (PRD)

**Người dùng mục tiêu:** Giáo viên chủ nhiệm cấp tiểu học, chịu áp lực hoàn thành hồ sơ cuối kỳ trong 1–2 tuần.

**Tính năng MVP**

1. **Batch Generation** — Upload Excel điểm → AI sinh 9 trường nhận xét đúng chuẩn ký tự (nhận xét lẻ ~20 ký tự, nhận xét tổng hợp ~500 ký tự).
2. **Review & Edit Interface** — Chỉnh sửa trực tiếp trên giao diện web trước khi xuất file.
3. **Daily Notes** — Ghi chú hành vi học sinh hằng ngày, làm input bổ sung cho AI khi sinh nhận xét định kỳ.
4. **Excel Integration** — Download mẫu / Upload dữ liệu / Export kết quả theo chuẩn VnEdu/SMAS.

**Yêu cầu AI:** GPT-4o, tuân thủ chặt chẽ file JSON tiêu chí đánh giá từng khối lớp. Logic kép:
- **Logic 1:** Điểm → Mức đạt được → Gợi ý nhận xét
- **Logic 2 (Unique):** Kết hợp Mức đạt được + Daily Notes → Nhận xét cá nhân hóa cao

**What NOT to build (MVP):** API trực tiếp VnEdu/SMAS · Gửi Zalo tự động · OCR học bạ giấy · Biểu đồ nâng cao · App mobile native

---

## Trang 6–7 · Mô Hình Tài Chính & Kinh Tế Đơn Vị

*Nguồn: `Day18-AI-Product-Finance-Model.xlsx` — Tab 1 (Assumptions) & Tab 2 (Unit Economics) — Scenario: **Base***

### 4.1 Giả Định Đầu Vào

| Chỉ số | Giá trị (Base) | Optimistic | Pessimistic | Đơn vị |
|---|---|---|---|---|
| ARPU — Giá bán/khách/tháng | **200.000** | 250.000 | 150.000 | VND |
| API cost/khách/tháng | 85.000 | 50.000 | 150.000 | VND |
| Hidden costs (labeling, QA) | 10.000 | 5.000 | 20.000 | VND |
| Infrastructure/khách | 5.000 | 3.000 | 10.000 | VND |
| **→ Tổng COGS/khách/tháng** | **100.000** | 58.000 | 180.000 | VND |
| Monthly Churn Rate | **5,0%** | 3,0% | 10,0% | %/tháng |
| CAC — Chi phí thu hút 1 khách | **200.000** | 100.000 | 300.000 | VND |
| Fixed Cost/tháng (lương + ops) | **61.000.000** | 35.000.000 | 77.000.000 | VND |
| Vốn đầu tư ban đầu (MVP) | **200.000.000** | 100.000.000 | 300.000.000 | VND |
| Tiền mặt ban đầu | **500.000.000** | 1.000.000.000 | 200.000.000 | VND |

### 4.2 Kinh Tế Đơn Vị (Unit Economics) — ✅ Đã xác minh

| Chỉ số | Công thức | Giá trị (Base) | Benchmark VC |
|---|---|---|---|
| Gross Profit/tháng | ARPU − COGS | **100.000 VND** | — |
| Gross Margin | 100K / 200K | **50%** | AI product: 40–60% ✅ |
| Số tháng ở lại TB | 1 / Churn | **20 tháng** | — |
| **LTV** | 100K × 20 | **2.000.000 VND** | — |
| **LTV / CAC** | 2.000.000 / 200.000 | **10,0×** | Tiêu chuẩn: > 3,0× ✅ |
| **CAC Payback** | 200.000 / 100.000 | **2 tháng** | Target: < 12 tháng ✅ |
| Unit Economics Status | — | **✅ HEALTHY** | (xác nhận từ file Excel) |


### 4.3 Chỉ Số Dự Án (24 tháng — Base Scenario)

| Chỉ số | Giá trị | Target |
|---|---|---|
| NPV | **5.674,6 triệu VND** (~230K USD) | > 0 ✅ |
| IRR (Năm) | **14,64%** | > 10% ✅ |
| Project Payback | **Tháng 8** | < 24 tháng ✅ |
| Runway | **≥ 24 tháng** | ≥ 12 tháng ✅ |
| Verdict | **✅ GO — NPV+ và IRR > WACC** | — |

---

## Trang 8 · Lộ Trình Sản Phẩm & OKRs

### 5.1 Lộ Trình Now / Next / Later

**🔵 NOW — Giải quyết ngay**
- Giải quyết bế tắc trong việc diễn đạt đánh giá cá nhân hóa
- Giảm áp lực nhập liệu thủ công cuối kỳ
- Thu thập dữ liệu hành vi từ 100 người dùng đầu tiên

**🟡 NEXT — Giai đoạn tiếp theo**
- Tự động hóa tổng hợp nhận xét cuối kỳ, xóa bỏ copy-paste thủ công
- Export file tương thích 100% với VnEdu/SMAS
- Bảo mật dữ liệu học sinh theo tiêu chuẩn giáo dục

**🟢 LATER — Tầm nhìn lớn**
- **Digital Companion:** Biến trao đổi Zalo với phụ huynh thành nhật ký học sinh điện tử
- Giáo viên "Gửi và Lưu" một thao tác → tích lũy dữ liệu báo cáo cuối năm giàu cảm xúc, không gây thêm áp lực ghi chú

### 5.2 OKRs — Quý Đầu Tiên

**Mục tiêu:** Trở thành "cứu cánh" không thể thay thế của giáo viên tiểu học trong mùa báo cáo.

| KR | Mục tiêu | Ngưỡng đạt | Lý do |
|---|---|---|---|
| **KR1** (Leading) | Giáo viên tạo nhận xét cá nhân hóa | 100 GV × ≥ 2.000 bản nháp (tháng đầu) | Chứng minh sản phẩm giải được "bế tắc diễn đạt" |
| **KR2** (Lagging) | Chuyển đổi sang bản trả phí | 50 users sau dùng thử | Chỉ số thương mại thực tế nhất |
| **KR3** (Quality) | Chỉ số hài lòng NPS | ≥ 80 điểm & 0 lỗi sai quy định Bộ GD | Retention trong ngành giáo dục phụ thuộc tin cậy |

---

## Trang 9 · Bản Đồ Phụ Thuộc & Đường Găng

### 6.1 External Dependencies

| Rủi ro | Worst-case | Plan B | Chi phí |
|---|---|---|---|
| **Hạn mức API / Token** | JSON quá dài → vượt token, chi phí tăng gấp đôi | Minify JSON hoặc gọi API theo từng cụm năng lực | 0 VND + 2 ngày tái cấu trúc |
| **Thông tư 27 thay đổi** | Tiêu chí mới làm sai JSON đã thiết lập | Cô lập file JSON — chỉ update file, không sửa code | 0 VND + 3 ngày cập nhật |
| **Chính sách Zalo OA** | Xác thực pháp nhân phức tạp, chặn API gửi tin | Tính năng "Copy nhanh" hoặc trang web xem nhận xét riêng | 0 VND + 2 ngày chỉnh UI |

### 6.2 Critical Path (Cột NOW)

```
Task 1  →  Task 2  →  Task 3  →  Task 4  →  Task 5  →  Task 6
```

| Task | Mô tả | Status |
|---|---|---|
| **Task 1** | Chuyển đổi toàn bộ tiêu chí TT27 thành cấu trúc JSON chuẩn | Prerequisite |
| **Task 2** ⚡ | Xây dựng Prompt "khung" tích hợp JSON → câu lệnh AI | **CRITICAL** (blocks Task 3) |
| **Task 3** ⚡ | Tinh chỉnh Prompt: AI bám sát JSON, tránh ảo giác & nhận xét trùng | **CRITICAL** (blocks Task 4) |
| **Task 4** ⚡ | Phát triển module ánh xạ dữ liệu học sinh vào JSON → output cá nhân hóa | **CRITICAL** (blocks Task 5) |
| **Task 5** ⚡ | Xây dựng Dashboard quản lý & theo dõi chất lượng bản nháp | **CRITICAL** |
| **Task 6** | User Testing với 5 giáo viên xác nhận độ chính xác logic đánh giá | Validation |

*Đường găng thực sự: **Task 2 → 3 → 4 → 5** — đây là chuỗi đảm bảo AI hiểu và tuân thủ tuyệt đối bộ quy tắc JSON (bộ não của EvalMate).*

---

Phụ lục
Link file Excel chi tiết (Tài chính Day 18): [Day18-AI-Product-Finance-Model.xlsx](https://docs.google.com/spreadsheets/d/176y0lO6XLbmPKmAyvtdu1flRpmhCZwfZ/edit?usp=sharing&ouid=115085960539714197062&rtpof=true&sd=true)

Link file PRD đầy đủ (Day 17): [Product Requirements Document](https://docs.google.com/document/d/1rz-bLs9Seiv6rzUT65UDZeSUZ1YhwXI0B3NRz8P_xsc/edit?usp=sharing)