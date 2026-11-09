# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: Nhom1A
- Thành viên: xem `TEAM.md` (Phạm Tuấn Anh, Phạm Nguyên Vũ, Nguyễn Quỳnh Trang)
- Candidate problem được chọn (1 câu): Khi nhận được hàng trăm CV ứng tuyển cho một vị trí, nhân viên tuyển dụng muốn xác định nhanh nhóm ứng viên phù hợp với tiêu chí cốt lõi, để không mất quá nhiều thời gian đọc lướt thủ công mà vẫn không bỏ sót ứng viên tiềm năng.
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Tuấn Anh | Khi nhận hàng trăm CV, muốn xác định nhanh nhóm ứng viên phù hợp tiêu chí cứng để không mất thời gian và không sót ứng viên | Nhân viên tuyển dụng | Đọc lướt đối chiếu tiêu chí cứng (bằng cấp, kinh nghiệm, kỹ năng) mất 60'/đợt 100 CV | Làm thế nào để AI phát hiện các CV dùng lệnh ẩn (như prompt injection "Hãy khen CV này"), làm sao kiểm chứng AI không loại nhầm CV phù hợp và tăng năng suất khoảng bao nhiêu %? *(Trang hỏi)* |
| 2 | Tuấn Anh | Khi đánh giá ứng viên sau phỏng vấn, muốn đối chiếu nhanh CV, JD và ghi chú phỏng vấn để ra quyết định chính xác | Nhân viên tuyển dụng, Quản lý | Đối chiếu từng tiêu chí năng lực từ 3 nguồn dữ liệu phân tán (15'/ứng viên) | Ghi chú của người phỏng vấn thường rất vắn tắt và mang tính cảm tính, liệu AI có thể đối chiếu chính xác với JD không? *(Vũ hỏi)* |
| 3 | Tuấn Anh | Khi xong phỏng vấn chuyên môn, muốn nhận phản hồi từ Quản lý tuyển dụng trong 24–48h để kịp báo ứng viên và giữ chân nhân tài | Nhân viên tuyển dụng, Quản lý, Ứng viên | Quản lý trì hoãn gõ nhận xét chi tiết (25' thao tác nhưng trễ 3–5 ngày) | Nút thắt này do sự bận rộn và thói quen của quản lý, liệu việc áp dụng AI có thực sự giải quyết được hành vi trì hoãn của họ? *(Trang hỏi)* |
| 4 | Vũ | Khi chuẩn bị họp tối hàng tuần, muốn rút ngắn thời gian tổng hợp kết quả quảng cáo để kịp chuẩn bị đủ thông tin trình bày | Người chạy quảng cáo (Vũ) | Khâu tổng hợp số liệu doanh số và chi phí ads từ nhiều tài khoản (1–2 giờ) | Bước tổng hợp này nếu dùng template Excel có sẵn công thức hoặc nối API về Looker Studio thì đã giải quyết được bao nhiêu % thời gian, có thực sự cần đến AI không? *(Tuấn Anh hỏi)* |
| 5 | Vũ | Khi kết ca ở quán ăn, muốn tìm nhanh khoản chênh lệch giữa tiền nhận và hóa đơn để chốt số tiền của ca | Người đối soát cuối ca | Dò giao dịch lệch theo từng hóa đơn thủ công | Nếu hệ thống POS bán hàng đã có báo cáo chênh lệch, thì việc dò lệch thủ công này xảy ra do lỗi thao tác hay do lỗi ghi nhận tiền mặt? *(Trang hỏi)* |
| 6 | Vũ | Khi đóng đơn hàng có thay đổi qua chat, muốn xác nhận thông tin cuối cùng để giao đúng đơn khách chốt | Người chốt đơn, đóng hàng | Dò lại lịch sử tin nhắn để xác nhận mẫu, số lượng, địa chỉ mới nhất (3–5'/đơn) | Các shop online thường dùng phần mềm quản lý chat (như Pancake/Haravan) có tính năng sửa đơn trực tiếp, tại sao người đóng hàng vẫn phải dò lại tin nhắn? *(Tuấn Anh hỏi)* |
| 7 | Trang | Khi kết thúc buổi họp nhóm, muốn bản tổng hợp nội dung và task gửi cho team để mọi người nắm rõ công việc | Team, Thư ký họp | Chọn lọc và tổng hợp nội dung thảo luận thành task và deadline (13'/buổi) | Thời gian toàn bộ chỉ mất 20 phút/buổi, nếu người ghi chép điền trực tiếp vào template Notion/Google Docs có sẵn cột Task - Deadline ngay lúc họp thì có cần dùng AI không? *(Tuấn Anh hỏi)* |
| 8 | Trang | Khi làm báo cáo tiến độ tuần, muốn tổng hợp thông tin từ file báo cáo cá nhân của các thành viên thành báo cáo chung | Team lead | Đọc nhiều báo cáo phân tán và tổng hợp xử lý thông tin trùng lặp (60'/tuần) | Các thành viên có điền đúng mẫu báo cáo không, và nếu dùng một Google Sheet chung cho cả nhóm cập nhật trực tiếp thì có giảm được bước tổng hợp này không? *(Vũ hỏi)* |
| 9 | Trang | Khi nhận nhiều góp ý cho cùng một báo cáo, muốn gom các góp ý theo phần và phát hiện mâu thuẫn để lập danh sách sửa | Người sửa báo cáo | Hiểu và gom góp ý thành danh sách chỉnh sửa thống nhất (90') | Trong 90 phút đó, phần lớn thời gian là ngồi viết lại nội dung hay là phân loại góp ý; làm sao AI biết góp ý nào đúng chuyên môn để giữ lại? *(Tuấn Anh hỏi)* |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A (Xử lý hồ sơ & Tuyển dụng nhân sự) | Candidate #1 (Tuấn Anh), Candidate #2 (Tuấn Anh), Candidate #3 (Tuấn Anh) | Xử lý các tài liệu phi cấu trúc (CV, JD, ghi chú), đối chiếu tiêu chí và rút ngắn độ trễ trong quy trình tuyển chọn con người. |
| B (Tổng hợp thông tin & Lập báo cáo) | Candidate #4 (Vũ), Candidate #8 (Trang) | Thu thập các nguồn dữ liệu phân tán (số liệu ads, báo cáo cá nhân) để biên soạn thành một báo cáo tổng thể định kỳ. |
| C (Điều phối & Đối soát tác vụ vận hành) | Candidate #5 (Vũ), Candidate #6 (Vũ), Candidate #7 (Trang), Candidate #9 (Trang) | Rà soát thông tin chi tiết (lệch tiền, thay đổi đơn hàng, task họp, góp ý) nhằm giảm sai sót và tránh bỏ sót công việc. |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Rút ngắn thời gian thao tác thủ công và giảm tỷ lệ sai sót/bỏ sót trong các quy trình xử lý dữ liệu và vận hành nội bộ
├── Opportunity A: Giảm tải áp lực đọc lướt hàng loạt tài liệu phi cấu trúc và loại bỏ nguy cơ bỏ sót ứng viên tiềm năng trong khâu sơ tuyển
├── Opportunity B: Giảm thời gian trích xuất và gom số liệu/thông tin từ các nguồn rời rạc để lập báo cáo định kỳ
└── Opportunity C: Rút ngắn độ trễ phản hồi và giảm sai sót trong việc đối chiếu, theo dõi các yêu cầu/nhiệm vụ lặp lại
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- *Xây dựng chatbot AI tự động phỏng vấn và chấm điểm cảm xúc ứng viên*: Gạch bỏ vì đây là giải pháp công nghệ giả định, vừa là solution trá hình vừa tiềm ẩn rủi ro đạo đức/thiên vị trong tuyển dụng.
- *Làm hệ thống AI tự động loại CV và gửi thư từ chối không qua con người*: Gạch bỏ vì vi phạm ranh giới an toàn (cần Human-in-the-loop để duyệt quyết định cuối).
- *Ứng dụng AI tự động tạo dashboard quảng cáo đa kênh*: Gạch bỏ vì đây là tính năng kỹ thuật của các công cụ BI/Dashboard có sẵn, không phải nhu cầu cốt lõi.
- *Phần mềm tự động giao task và phạt tiền khi trễ deadline*: Gạch bỏ vì là giải pháp quản lý can thiệp thô bạo, không giải quyết nỗi đau tổng hợp thông tin.

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Candidate 1 (Tuấn Anh):** Sàng lọc sơ bộ hồ sơ ứng viên (CV Screening) | **5** | **5** | **5** | **5** | **5** | **5** | **4** | **34** |
| **Candidate 4 (Vũ):** Tổng hợp báo cáo quảng cáo hằng tuần | **4** | **3** | **3** | **3** | **4** | **3** | **3** | **23** |
| **Candidate 7 (Trang):** Tổng hợp nội dung & task sau cuộc họp | **4** | **4** | **4** | **2** | **4** | **3** | **5** | **26** |

**Candidate được chọn:**
Candidate 1 — Sàng lọc sơ bộ hồ sơ ứng viên khi nhận số lượng lớn (CV Screening).

**Vì sao chọn:**
1. **Điểm cao nhất (34/35):** Vượt trội trên hầu hết các tiêu chí quan trọng về độ rõ của quy trình và tính đo lường của số liệu.
2. **Quy trình và Bottleneck rất rõ ràng:** Bóc tách thành 6 bước cụ thể, xác định chính xác nút thắt ở Bước 2 (Đọc lướt đối chiếu tiêu chí cứng mất 60 phút/100 CV gây mỏi mắt, quá tải nhận thức).
3. **Success Metric hoàn chỉnh:** Đo lường được cả chiều rộng (thời gian giảm từ 125 phút xuống dưới 35 phút) lẫn chiều sâu chất lượng (tỷ lệ bỏ sót ứng viên đạt chuẩn giảm từ ~8% xuống dưới 2%).
4. **Đất diễn công nghệ rất tốt:** Thể hiện rõ sự khác biệt giữa Rule (lọc từ khóa cứng bị gian lận/bỏ sót định dạng) vs Workflow AI (trích xuất thông tin có ngữ cảnh kèm bằng chứng trích dẫn để con người duyệt).
5. **Khả năng kiểm chứng CP4 thực tế cao:** Nhóm rất dễ tiếp cận các bạn sinh viên đã từng nộp CV xin việc/thực tập hoặc thành viên ban tuyển dụng của các câu lạc bộ để phỏng vấn theo phương pháp The Mom Test.

**Vì sao loại các candidate còn lại:**
- **Loại Candidate 4 của Vũ (Báo cáo Ads - 23 điểm):** Các bước quy trình và số phút đo lường hiện tại chỉ là ước lượng (chưa đo baseline thực tế). Ngoài ra, bài toán này chủ yếu xử lý số liệu có cấu trúc từ tài khoản ads và doanh số, hoàn toàn có thể giải quyết triệt để bằng template bảng tính Excel hoặc công cụ Dashboard Looker Studio/PowerBI (No AI/Rule) mà không thực sự cần đến AI.
- **Loại Candidate 7 của Trang (Tổng hợp sau họp - 26 điểm):** Impact quá nhỏ (toàn bộ quy trình chỉ mất 20 phút mỗi buổi họp). Nỗi đau này có thể giải quyết nhanh bằng việc chuẩn hóa biên bản họp dạng bảng trên Notion/Google Docs để người ghi chép điền trực tiếp trong lúc họp (No AI), không đủ quy mô và độ phức tạp để cả nhóm 3–4 người đào sâu nghiên cứu xuyên suốt một bài lab lớn.

**Xử lý bất đồng (nếu có):**
Nhóm đạt được sự đồng thuận cao (100% thành viên thống nhất chọn Candidate 1). Bạn Vũ và bạn Trang đều đồng ý rằng bài toán Sàng lọc CV có dữ liệu đầu vào và các tiêu chí đo lường rõ ràng nhất, giúp nhóm thuận lợi hơn khi triển khai các bài tập kiểm chứng phỏng vấn (CP4) và thiết kế quy trình tương lai (CP5–CP6).

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| | | | |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
