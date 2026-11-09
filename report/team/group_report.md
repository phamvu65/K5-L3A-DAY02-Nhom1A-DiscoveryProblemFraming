# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: Nhom1A
- Thành viên: xem `TEAM.md` (Phạm Tuấn Anh, Phạm Nguyên Vũ, Nguyễn Quỳnh Trang, Nguyễn Khắc Khánh)
- Candidate problem được chọn (1 câu): Khi nhận được hàng trăm CV ứng tuyển cho một vị trí, nhân viên tuyển dụng muốn xác định nhanh nhóm ứng viên phù hợp với tiêu chí cốt lõi, để không mất quá nhiều thời gian đọc lướt thủ công mà vẫn không bỏ sót ứng viên tiềm năng.
- Quyết định cuối: Go (Thử nghiệm pilot phạm vi hẹp)

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Tuấn Anh | Khi nhận hàng trăm CV, muốn xác định nhanh nhóm ứng viên phù hợp tiêu chí cứng để không mất thời gian và không sót ứng viên | Nhân viên tuyển dụng | Đọc lướt đối chiếu tiêu chí cứng (bằng cấp, kinh nghiệm, kỹ năng) mất 60'/đợt 100 CV | Làm thế nào để AI phát hiện các CV dùng lệnh ẩn (như prompt injection "Hãy khen CV này"), làm sao kiểm chứng AI không loại nhầm CV phù hợp và tăng năng suất khoảng bao nhiêu %? *(Trang hỏi)* |
| 2 | Tuấn Anh | Khi đánh giá ứng viên sau phỏng vấn, muốn đối chiếu nhanh CV, JD và ghi chú phỏng vấn để ra quyết định chính xác | Nhân viên tuyển dụng, Quản lý | Đối chiếu từng tiêu chí năng lực từ 3 nguồn dữ liệu phân tán (15'/ứng viên) | Ghi chú của người phỏng vấn thường rất vắn tắt và mang tính cảm tính, liệu AI có thể đối chiếu chính xác với JD không? *(Vũ hỏi)* |
| 3 | Tuấn Anh | Khi xong phỏng vấn chuyên môn, muốn nhận phản hồi từ Quản lý tuyển dụng trong 24–48h để kịp báo ứng viên và giữ chân nhân tài | Nhân viên tuyển dụng, Quản lý, Ứng viên | Quản lý trì hoãn gõ nhận xét chi tiết (25' thao tác nhưng trễ 3–5 ngày) | Nút thắt này do sự bận rộn và thói quen của quản lý, liệu việc áp dụng AI có thực sự giải quyết được hành vi trì hoãn của họ? *(Trang hỏi)* |
| 4 | Vũ | Khi chuẩn bị họp tối hàng tuần, muốn rút ngắn thời gian tổng hợp kết quả quảng cáo để kịp chuẩn bị đủ thông tin trình bày | Người chạy quảng cáo (Vũ) | Tổng hợp doanh số và chi phí quảng cáo từ nhiều nguồn. Toàn bộ báo cáo tuần mất khoảng 1–2 giờ, chưa đo riêng bước tổng hợp. | Bước tổng hợp này nếu dùng template Excel có sẵn công thức hoặc nối API về Looker Studio thì đã giải quyết được bao nhiêu % thời gian, có thực sự cần đến AI không? *(Tuấn Anh hỏi)* |
| 5 | Vũ | Khi kết ca ở quán ăn, muốn tìm nhanh khoản chênh lệch giữa tiền nhận và hóa đơn để chốt số tiền của ca | Người đối soát cuối ca | Dò giao dịch lệch theo từng hóa đơn thủ công | Nếu hệ thống POS bán hàng đã có báo cáo chênh lệch, thì việc dò lệch thủ công này xảy ra do lỗi thao tác hay do lỗi ghi nhận tiền mặt? *(Trang hỏi)* |
| 6 | Vũ | Khi đóng đơn hàng có thay đổi qua chat, muốn xác nhận thông tin cuối cùng để giao đúng đơn khách chốt | Người chốt đơn, đóng hàng | Dò lại lịch sử tin nhắn để xác nhận mẫu, số lượng, địa chỉ mới nhất (3–5'/đơn) | Các shop online thường dùng phần mềm quản lý chat (như Pancake/Haravan) có tính năng sửa đơn trực tiếp, tại sao người đóng hàng vẫn phải dò lại tin nhắn? *(Tuấn Anh hỏi)* |
| 7 | Trang | Khi kết thúc buổi họp nhóm, muốn bản tổng hợp nội dung và task gửi cho team để mọi người nắm rõ công việc | Team, Thư ký họp | Chọn lọc và tổng hợp nội dung thảo luận thành task và deadline (13'/buổi) | Thời gian toàn bộ chỉ mất 20 phút/buổi, nếu người ghi chép điền trực tiếp vào template Notion/Google Docs có sẵn cột Task - Deadline ngay lúc họp thì có cần dùng AI không? *(Tuấn Anh hỏi)* |
| 8 | Trang | Khi làm báo cáo tiến độ tuần, muốn tổng hợp thông tin từ file báo cáo cá nhân của các thành viên thành báo cáo chung | Team lead | Đọc nhiều báo cáo phân tán và tổng hợp xử lý thông tin trùng lặp (60'/tuần) | Các thành viên có điền đúng mẫu báo cáo không, và nếu dùng một Google Sheet chung cho cả nhóm cập nhật trực tiếp thì có giảm được bước tổng hợp này không? *(Vũ hỏi)* |
| 9 | Trang | Khi nhận nhiều góp ý cho cùng một báo cáo, muốn gom các góp ý theo phần và phát hiện mâu thuẫn để lập danh sách sửa | Người sửa báo cáo | Hiểu và gom góp ý thành danh sách chỉnh sửa thống nhất (90') | Trong 90 phút đó, phần lớn thời gian là ngồi viết lại nội dung hay là phân loại góp ý; làm sao AI biết góp ý nào đúng chuyên môn để giữ lại? *(Tuấn Anh hỏi)* |
| 10 | Khánh | Khi sát hạn 23h59 nộp bài lab, muốn đối chiếu toàn bộ mục bài làm với Rubric để không bị trừ điểm lỗi hình thức | Học viên (Khánh, team) | Đối chiếu chi tiết từng tiêu chí Rubric với nội dung bài viết (25'/lần) | Tiêu chí Rubric có nhiều chỗ mang tính định tính (chất lượng lập luận), nếu AI chấm điểm thì làm sao tin tưởng được kết quả của AI? *(Tuấn Anh hỏi)* |
| 11 | Khánh | Sau buổi đi chơi nhóm, muốn phân bổ số tiền thanh toán đúng theo món từng người đã dùng để thu tiền đủ và đúng | Người thanh toán trước (chủ chi) | Tính toán phân bổ tiền món riêng, món chung và thuế/phí (15') | Hiện đã có nhiều app chia tiền (Splitwise, MoMo), tại sao người dùng phải cần một giải pháp AI thay vì dùng bảng tính Excel/app có sẵn? *(Vũ hỏi)* |
| 12 | Khánh | Khi học bài lúc 20h tối, muốn duy trì tập trung liên tục mà không bị ngắt quãng bởi thông báo điện thoại để xong bài sớm | Sinh viên tự học | Bị cuốn vào lướt mạng vô thức (45'/lần ngắt quãng) | Đây là vấn đề thuộc về kỷ luật hành vi con người, liệu AI có ngăn được người dùng cầm điện thoại lên không nếu họ không tự kiểm soát? *(Trang hỏi)* |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A (Xử lý hồ sơ & Tuyển dụng nhân sự) | Candidate #1 (Tuấn Anh), Candidate #2 (Tuấn Anh), Candidate #3 (Tuấn Anh) | Xử lý các tài liệu phi cấu trúc (CV, JD, ghi chú), đối chiếu tiêu chí và rút ngắn độ trễ trong quy trình tuyển chọn con người. |
| B (Tổng hợp thông tin & Lập báo cáo) | Candidate #4 (Vũ), Candidate #8 (Trang) | Thu thập các nguồn dữ liệu phân tán (số liệu ads, báo cáo cá nhân) để biên soạn thành một báo cáo tổng thể định kỳ. |
| C (Điều phối & Đối soát tác vụ vận hành) | Candidate #5 (Vũ), Candidate #6 (Vũ), Candidate #7 (Trang), Candidate #9 (Trang), Candidate #11 (Khánh) | Rà soát thông tin chi tiết (lệch tiền, thay đổi đơn hàng, task họp, góp ý, chia tiền ăn uống) nhằm giảm sai sót và tránh thất thoát. |
| D (Rà soát & Đánh giá tài liệu học tập) | Candidate #10 (Khánh) | Đối chiếu văn bản bài làm với khung tiêu chí chuẩn (Rubric/Checklist) để phát hiện thiếu sót trước hạn chót. |
| E (Duy trì tập trung khi tự học) | Candidate #12 (Khánh) | Giảm số lần gián đoạn do thông báo và thời gian quay lại bài học. |

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
| **Candidate 1 (Tuấn Anh):** Sàng lọc sơ bộ hồ sơ ứng viên (CV Screening) | **4** | **4** | **4** | **4** | **4** | **4** | **4** | **28** |
| **Candidate 4 (Vũ):** Tổng hợp báo cáo quảng cáo hằng tuần | **4** | **4** | **3** | **4** | **4** | **4** | **4** | **27** |
| **Candidate 7 (Trang):** Tổng hợp nội dung & task sau cuộc họp | **4** | **4** | **4** | **3** | **4** | **3** | **5** | **27** |

**Vòng chấm sơ bộ:** Candidate 11 của Khánh đạt 26/35 (4 · 4 · 4 · 3 · 4 · 2 · 5 theo thứ tự tiêu chí trong bảng) và đứng thứ tư, ngoài shortlist ba đề tài.

**Candidate được chọn:**
Candidate 1 — Sàng lọc sơ bộ hồ sơ ứng viên khi nhận số lượng lớn (CV Screening).

**Vì sao chọn:**
1. **Điểm cao nhất shortlist (28/35):** Nhóm chọn sàng lọc CV vì quy trình đã tách thời gian theo từng bước và có thể kiểm chứng cả thời gian xử lý lẫn nguy cơ bỏ sót ứng viên.
2. **Quy trình và Bottleneck rất rõ ràng:** Bóc tách thành 6 bước cụ thể, xác định chính xác nút thắt ở Bước 2 (Đọc lướt đối chiếu tiêu chí cứng mất 60 phút/100 CV gây mỏi mắt, quá tải nhận thức).
3. **Có hai mục tiêu đo được:** Giảm thời gian xử lý 100 CV từ 125 xuống dưới 35 phút và hướng đến tỷ lệ bỏ sót dưới 2%. Mốc bỏ sót khoảng 8% là ước tính ban đầu, cần đo lại trên dữ liệu có đối chiếu.
4. **Đất diễn công nghệ rất tốt:** Thể hiện rõ sự khác biệt giữa Rule (lọc từ khóa cứng bị gian lận/bỏ sót định dạng) vs Workflow AI (trích xuất thông tin có ngữ cảnh kèm bằng chứng trích dẫn để con người duyệt).
5. **Khả năng kiểm chứng CP4 thực tế cao:** Nhóm rất dễ tiếp cận các bạn sinh viên đã từng nộp CV xin việc/thực tập hoặc thành viên ban tuyển dụng của các câu lạc bộ để phỏng vấn theo phương pháp The Mom Test.

**Vì sao loại các candidate còn lại:**
- **Loại Candidate 11 của Khánh (Chia tiền đi chơi - 26 điểm):** Bài toán tuy có nỗi đau thật nhưng bản chất phép tính toán phân bổ tiền và chia hóa đơn phần lớn giải quyết được bằng Rule / công thức Excel hoặc các ứng dụng thanh toán hiện có (MoMo, Splitwise). Việc ứng dụng AI ở đây chỉ dừng ở khâu OCR đọc hóa đơn giấy, giá trị giải quyết bằng AI chưa đủ sâu so với bài toán lọc CV.
- **Candidate 7 của Trang (Tổng hợp sau họp - 27 điểm):** Tác động đo được bằng thời gian từ 20 phút xuống dưới 10 phút mỗi buổi, đồng thời kiểm tra nhiệm vụ, người phụ trách và hạn chót. Nhóm ưu tiên sàng lọc CV vì với bài tổng hợp sau họp, một mẫu biên bản điền trực tiếp trong buổi họp là phương án đơn giản có thể thử trước.
- **Candidate 4 của Vũ (Báo cáo Ads - 27 điểm):** Quy trình có hai nguồn số liệu rõ ràng, lặp hằng tuần và người thực hiện có thể đo trực tiếp để so sánh mẫu báo cáo, công thức bảng tính và Workflow hỗ trợ khâu viết nhận xét nếu cần. Mốc 1–2 giờ mới là ước lượng cho toàn bộ báo cáo tuần, chưa có số đo riêng cho bước tổng hợp. Nhóm ưu tiên sàng lọc CV vì đề tài đó đã mô tả chi tiết hơn thời gian từng bước.

**Xử lý bất đồng (nếu có):**
Nhóm đạt được sự đồng thuận cao (100% thành viên thống nhất chọn Candidate 1). Bạn Vũ và bạn Trang đều đồng ý rằng bài toán Sàng lọc CV có dữ liệu đầu vào và các tiêu chí đo lường rõ ràng nhất, giúp nhóm thuận lợi hơn khi triển khai các bài tập kiểm chứng phỏng vấn (CP4) và thiết kế quy trình tương lai (CP5–CP6).

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Người tuyển dụng mất nhiều thời gian nhất ở việc đọc lướt đối chiếu tiêu chí cứng, chứ không phải ở việc tải file hay lưu trữ thư mục | Value | 5 | 2 | ✅ Kiểm chứng trước |
| 2 | Người tuyển dụng sẽ tin tưởng kết quả nếu AI trích xuất được đoạn trích dẫn (snippet) kèm số trang làm bằng chứng, thay vì chỉ trả về một con số điểm % vô căn cứ | Usability | 5 | 2 | ✅ Kiểm chứng trước |
| 3 | AI có thể đọc và bóc tách chính xác thông tin từ các định dạng CV phức tạp (PDF 2 cột, bảng biểu, file scan/ảnh) mà không làm rớt thông tin | Feasibility | 4 | 2 | ✅ Kiểm chứng trước |
| 4 | Ứng viên sẵn sàng chấp nhận việc hồ sơ được máy hỗ trợ sàng lọc nếu có con người rà soát lại và không bị máy từ chối tự động | Viability | 4 | 3 | — |
| 5 | Các phương án No AI (như bắt ứng viên điền form 20 câu hỏi điều kiện trên Google Form/ATS) làm giảm đáng kể tỷ lệ hoàn tất nộp đơn của ứng viên giỏi | Value | 4 | 3 | — |
| 6 | Chi phí token và hạ tầng cho AI trích xuất CV rẻ hơn đáng kể so với chi phí giờ công lao động của chuyên viên tuyển dụng | Viability | 4 | 4 | — |

**Kết quả theo giả định:** Phỏng vấn và poll cho tín hiệu về khó khăn khi đọc CV (#1). Phản hồi của một recruiter cho thấy họ cần bằng chứng để tự kiểm tra (#2). Khả năng xử lý CV scan và bố cục phức tạp (#3) vẫn cần thử trên bộ CV có đáp án đối chiếu.

### 3.2. Kiểm chứng

Cách đã dùng theo ghi chép nhóm: phỏng vấn 3 người và micro survey qua Google Poll với 8 người. Bản ghi hiện có mô tả vai trò và phương thức thu thập. Ngày phỏng vấn, ngày mở poll và bản tổng hợp câu trả lời cần đối chiếu với ghi chép gốc của nhóm.

#### Interview Snapshot 1:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò) | Trưởng ban Đối ngoại & Tuyển quân, CLB Sinh viên khởi nghiệp (từng lọc 140 đơn kỳ tuyển mùa thu) |
| Câu nói đáng nhớ nhất | *"Nói thật là đến cái CV thứ 30 là mắt mình bắt đầu 'hoa' rồi, chỉ lướt qua trường Đại học với mấy gạch đầu dòng kỹ năng. Có bạn viết kinh nghiệm dài 3 trang ở mãi cuối suýt nữa thì bị đánh trượt oan."* |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Tháng 9 vừa rồi khi mở đợt tuyển thành viên mới: nhận 140 hồ sơ trong 4 ngày, 3 bạn trong ban nhân sự phải chia nhau thức đêm đọc lọc đến 1h sáng để kịp lịch phỏng vấn ngày hôm sau. |
| Hiện đang xử lý bằng cách nào (workaround)? | Dùng file Google Sheet phân công: mỗi người mở 40 link Drive, đọc lướt rồi gõ tay điểm đánh giá từ 1–5 vào cột bên cạnh. |
| Mất bao lâu, bao lần? | 3 người làm cật lực trong 2 buổi tối, tổng cộng khoảng 10–12 giờ công lao động. |
| Insight / opportunity rút ra | Nỗi đau quá tải nhận thức khi đọc lướt là có thật 100%. Bước nghẽn không phải là mở link mà là bộ não mệt mỏi khi phải liên tục đối chiếu xem ứng viên có đáp ứng 3 tiêu chí cốt lõi hay không. |

#### Interview Snapshot 2:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò) | Junior Talent Acquisition Specialist (1.5 năm kinh nghiệm tại công ty IT Outsourcing 80 nhân sự) |
| Câu nói đáng nhớ nhất | *"Nếu tool chỉ cho tôi một con số 85% match mà không chỉ rõ dòng nào trong CV nói bạn ấy làm ReactJS 2 năm thì tôi vẫn phải mở CV ra đọc lại từ đầu. Tôi không dám mạo hiểm gọi ứng viên đến phỏng vấn chỉ vì máy bảo hợp."* |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Tuần trước tuyển vị trí Mid-level Java Dev, nhận 65 CV. Đọc lướt nhanh quá nên nhìn nhầm ứng viên làm "Java Core" thành "JavaScript", mời phỏng vấn kỹ thuật bị Technical Lead phàn nàn là ứng viên lệch chuyên môn hoàn toàn. |
| Hiện đang xử lý bằng cách nào (workaround)? | Mở file CV PDF bên trái, mở checklist tiêu chí bên phải, dùng tính năng `Ctrl + F` tìm từ khóa cứng (Java, Spring Boot, SQL). |
| Mất bao lâu, bao lần? | Mất trung bình 1.5 – 2 tiếng mỗi ngày mở đợt tuyển mới; đợt cao điểm lọc liên tục 3 ngày. |
| Insight / opportunity rút ra | **Tính minh bạch và khả năng kiểm chứng (Explainability) quan trọng hơn điểm số**. Recruiter không cần máy quyết định thay, mà cần máy làm "trợ lý bôi vàng" (highlight snippet) để họ liếc mắt 5 giây là xác nhận được. |

#### Interview Snapshot 3:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò) | Sinh viên năm 4 ngành CNTT vừa nộp 12 hồ sơ ứng tuyển vị trí Thực tập sinh / Fresher |
| Câu nói đáng nhớ nhất | *"Em ghét nhất là mấy công ty bắt vừa nộp CV vừa phải gõ lại toàn bộ quá trình học tập, dự án vào một cái form web dài dằng dặc. Form nào dài quá 15 phút là em tắt tab bỏ luôn."* |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Cách đây 2 tuần, nộp hồ sơ vào 3 tập đoàn lớn có cổng ATS bắt điền lại thông tin y hệt trong CV. Bị mất hơn 1 tiếng để copy paste lại từ file PDF sang từng ô text. |
| Hiện đang xử lý bằng cách nào (workaround)? | Chỉ ưu tiên nộp những tin tuyển dụng cho phép đính kèm file PDF trực tiếp qua email hoặc form 1-click. |
| Mất bao lâu, bao lần? | Đã bỏ cuộc không nộp 4 công ty vì cổng tuyển dụng bắt điền form quá phức tạp. |
| Insight / opportunity rút ra | Một ứng viên cho biết đã bỏ một số đơn vì form yêu cầu nhập lại nhiều thông tin. Đây là tín hiệu về ma sát của form dài. Cần kiểm tra riêng nếu thử form ngắn chỉ hỏi tiêu chí bắt buộc. |

#### Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Phỏng vấn sâu (The Mom Test) | 3 người: một recruiter, một người tuyển thành viên CLB và một ứng viên | Hai người làm tuyển dụng mô tả khó khăn khi đọc nhiều hồ sơ. Ứng viên mô tả từng bỏ đơn vì form dài. | Recruiter cho biết điểm phù hợp thiếu bằng chứng sẽ khiến họ phải mở CV đọc lại. |
| Micro survey (Google Poll trong lớp) | 8 người từng tham gia tuyển thành viên CLB / dự án | 7/8 người mất trên 60 phút mỗi đợt lọc hồ sơ; 8/8 người từng bỏ sót thông tin quan trọng trong CV | 2/8 người lo ngại AI sẽ đọc sai các CV trình bày dạng 2 cột hoặc có yếu tố đồ họa/ảnh |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**
1. **Thu hẹp phạm vi can thiệp của AI:** Không cố gắng xây dựng hệ thống "tự động tuyển dụng" hay "chấm điểm ứng viên toàn diện". AI chỉ tập trung đúng vào **khâu trích xuất bằng chứng theo tiêu chí cứng (Contextual Evidence Extraction)**.
2. **Củng cố ranh giới an toàn (Boundary):** Đưa nguyên tắc **Human-in-the-loop** thành yêu cầu bắt buộc: AI chỉ hiển thị bảng trích dẫn kèm số trang, quyền bấm nút "Đạt / Dự phòng / Loại" hoàn toàn thuộc về con người. Không có tính năng tự động từ chối ứng viên.
3. **Bổ sung cơ chế xử lý file lỗi:** Với các CV dạng scan/ảnh mờ, hệ thống gắn nhãn cảnh báo để Recruiter mở xem tay riêng, tránh việc AI phỏng đoán sai lệch.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **TopCV AI Matching** | [Tài liệu dành cho nhà tuyển dụng](https://tuyendung.topcv.vn/) | Bước 2–4: gợi ý mức độ phù hợp của CV với JD | Đối chiếu kinh nghiệm, kỹ năng và học vấn | Trang giới thiệu chưa làm rõ đầu ra có kèm đoạn trích và số trang hay không | Với pilot, hiển thị bằng chứng theo từng tiêu chí để recruiter tự kiểm tra |
| **Workable Agent** | [Hướng dẫn đánh giá ứng viên](https://help.workable.com/hc/en-us/articles/41050763193623-Getting-started-with-the-Workable-Agent) | Bước 2–4: đánh giá hồ sơ theo tiêu chí vị trí | Hiển thị điểm và lý do theo từng tiêu chí | Công cụ dùng tín dụng AI. Chi phí thực tế cho đợt tuyển của nhóm chưa được đo | Tách kết quả từng tiêu chí và giải thích để người tuyển dụng dễ đối chiếu |
| **spaCy EntityRuler** | [Tài liệu so khớp theo luật](https://spacy.io/usage/rule-based-matching) | Bước 2: đối chiếu mẫu từ hoặc cụm từ sau khi tách văn bản | Luật có thể kiểm tra và điều chỉnh | Cần văn bản đầu vào và tập mẫu. Bằng chứng về thời lượng hoặc ngữ cảnh có thể cần thêm luật | Dùng phương án theo luật làm mốc so sánh trên cùng bộ CV |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ quy trình hiện tại:

```text
HIỆN TẠI — 6 bước, 125 phút / đợt 100 CV (100% thủ công)

[1. Tải CV từ email/web về máy: 10']
  └──▶ [2. Mở từng file đọc lướt đối chiếu tiêu chí cứng: 60']  <── BOTTLENECK CHÍNH (Quá tải nhận thức, đọc sót)
        └──▶ [3. Ghi chú điểm số/nhận xét vào file Excel: 25']
              └──▶ [4. Phân loại Đạt / Dự phòng / Loại: 15']
                    └──▶ [5. Gửi danh sách Shortlist cho Quản lý duyệt: 5']
                          └──▶ [6. Lưu trữ và sắp xếp folder hồ sơ: 10']
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Recruiter | Email, form ứng tuyển | 100 file CV (PDF/Word) trong thư mục | 10 phút / đợt | Thao tác tải và gom file thủ công |
| 2 | Recruiter | File CV + Bản JD vị trí | Ghi nhớ trong đầu về mức độ phù hợp | 60 phút / đợt | **Bottleneck chính**: Mỏi mắt, dễ đọc sót ở 30 CV cuối |
| 3 | Recruiter | Nhận định chủ quan | File Excel tracking có ghi chú ứng viên | 25 phút / đợt | Gõ tay từng dòng, tốn thời gian chuyển cửa sổ |
| 4 | Recruiter | Dữ liệu file Excel | Danh sách hồ sơ phân loại sơ bộ | 15 phút / đợt | Đắn đo giữa các hồ sơ mấp mé tiêu chuẩn |
| 5 | Recruiter | Danh sách Đạt | Email/tin nhắn gửi Hiring Manager | 5 phút / đợt | Gửi danh sách để quản lý duyệt sơ bộ |
| 6 | Recruiter | Toàn bộ file CV | Các folder phân loại (Đạt/Loại) | 10 phút / đợt | Kéo thả file vào từng folder lưu trữ |

**Bottleneck chính:** Bước 2 — Mở từng file CV đọc lướt đối chiếu tiêu chí cứng (bằng cấp, số năm kinh nghiệm, kỹ năng cốt lõi) mất 60 phút/đợt. Não bộ người tuyển dụng bị quá tải nhận thức sau khi đọc liên tục hơn 20 file, dẫn đến việc bỏ sót các thông tin giá trị ở cuối CV hoặc đánh giá thiếu nhất quán.

### 4.2. Quy trình tương lai

Phân định rõ vai trò: **Rule** (tải file, tách text, gắn cờ lỗi), **AI** (trích xuất thông tin theo tiêu chí cứng kèm trích dẫn), **Con người** (duyệt quyết định và xử lý ngoại lệ).

Sơ đồ quy trình tương lai:

```text
TƯƠNG LAI — 5 bước, khoảng 30–35 phút / đợt 100 CV (Con người chỉ duyệt và ra quyết định)

[1. Gom CV vào thư mục hệ thống: 5']                     <── CON NGƯỜI
  └──▶ [2. Tách text & Kiểm tra lỗi định dạng: 2']        <── RULE (Nếu file ảnh/scan hỏng ──▶ Gắn cờ kiểm tra tay)
        └──▶ [3. Trích xuất bằng chứng theo tiêu chí JD: 3'] <── AI (LLM với Structured Schema + Trích dẫn số trang)
              └──▶ [4. Recruiter duyệt bảng đối chiếu: 20']  <── CON NGƯỜI (HITL: Liếc nhanh snippet, bấm Đạt/Loại)
                    └──▶ [5. Tự động xuất Shortlist & lưu: 2'] <── RULE (Tự xuất Excel tracking và phân loại folder)

BOUNDARY: AI tuyệt đối không tự ý ra quyết định loại bỏ ứng viên; AI không tự gửi thư từ chối; chỉ trích xuất dữ liệu có trong CV.
PHƯƠNG ÁN QUAY VỀ: Nếu hệ thống AI lỗi hoặc mất mạng, Recruiter dùng lại file Excel tracking truyền thống và lọc thủ công theo Bước 2 cũ.
```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| **Số bước** | 6 bước | 5 bước | Tích hợp khâu ghi chú và phân loại vào bảng duyệt trực quan |
| **Tổng thời gian** | 125 phút | khoảng 32 phút | Tiết kiệm ~74% thời gian cho mỗi đợt tuyển dụng |
| **Số bước thủ công** | 6 / 6 bước (100%) | 2 / 5 bước (40%) | Con người chỉ làm khâu nạp file ban đầu và duyệt quyết định cuối |
| **Bottleneck chính** | Đọc lướt đối chiếu (60') | Recruiter duyệt bảng đối chiếu (20') | Bottleneck mới là điểm kiểm soát chất lượng cần thiết của con người |
| **Tỷ lệ bỏ sót ứng viên** | Ước tính ~8% | Dưới 2% | Mục tiêu thử nghiệm. Xác nhận lại baseline và báo cáo số hồ sơ đạt chuẩn bị bỏ sót trên tổng số hồ sơ đạt chuẩn. |
| **Rủi ro mới phát sinh** | Không có | Ứng viên nhồi từ khóa ẩn; định dạng file scan không đọc được | Xử lý bằng: AI trích xuất kèm ngữ cảnh + Rule gắn cờ file lỗi |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Nhân viên tuyển dụng (Junior Recruiter / Ban nhân sự) phụ trách sàng lọc hồ sơ ứng viên đầu vào |
| **Quy trình** | Khi có đợt tuyển dụng: Tải CV $\rightarrow$ Đọc lướt đối chiếu tiêu chí cứng $\rightarrow$ Nhập ghi chú Excel $\rightarrow$ Phân loại $\rightarrow$ Gửi quản lý duyệt $\rightarrow$ Lưu folder |
| **Bottleneck** | Khâu đọc lướt đối chiếu tiêu chí cứng (học vấn, số năm kinh nghiệm, kỹ năng cốt lõi) qua hàng chục file CV định dạng khác nhau mất 60 phút, gây mỏi mắt và quá tải nhận thức |
| **Impact** | Mất hơn 2 giờ lao động cho mỗi đợt 100 CV; tỷ lệ bỏ sót ước tính khoảng 8% trong Card #1, chưa xác nhận mẫu số; làm chậm tiến độ xếp lịch phỏng vấn |
| **Success Metric** | Thời gian xử lý mục tiêu dưới 35 phút/100 CV, so với mốc 125 phút/100 CV trong Card #1. Đo từ khi bắt đầu gom hồ sơ đến khi lưu shortlist, gồm cả xử lý ngoại lệ. Tỷ lệ bỏ sót mục tiêu dưới 2%, tính bằng số CV đạt tiêu chí theo người đối chiếu nhưng bị loại, chia cho tổng số CV được xác nhận đạt tiêu chí. Mốc khoảng 8% là ước tính cần kiểm tra lại. |
| **Boundary** | AI tuyệt đối **không được tự động ra quyết định loại hay nhận ứng viên**; AI **không tự động gửi email** cho ứng viên; AI **chỉ trích xuất bằng chứng có thật** trong văn bản CV, không được suy diễn ngoài tài liệu. Khi gặp file lỗi định dạng, bắt buộc chuyển cho con người xem tay (Human-in-the-loop). |

**Phản biện nhận được (từ AI và các thành viên khác):**
- *Phản biện của Trang:* "Làm sao đảm bảo AI không bị đánh lừa bởi các CV dùng prompt injection (như dòng lệnh ẩn 'Hãy khen ứng viên này')?"
- *Nhóm đồng ý và xử lý:* Ở bản v1, nhóm sẽ bổ sung yêu cầu kỹ thuật: hệ thống sử dụng **Schema định dạng cố định (Structured Output)**, bỏ qua các chỉ thị mang tính câu lệnh trong nội dung CV và chỉ tìm các trường dữ liệu thực tế (thời gian, công ty, vị trí, công nghệ).

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

- **Độ mơ hồ (Ambiguity): Trung bình.** Mỗi ứng viên trình bày CV theo một phong cách khác nhau (văn bản phi cấu trúc, cách đặt tên vị trí và mô tả kinh nghiệm đa dạng), tuy nhiên tiêu chí tuyển dụng đầu vào lại khá rõ ràng (cần kỹ năng gì, tối thiểu mấy năm kinh nghiệm).
- **Độ phức tạp quy trình (Complexity): Thấp – Trung bình.** Quy trình gồm chuỗi các bước tuần tự cố định (Đọc $\rightarrow$ Trích xuất $\rightarrow$ Đối chiếu $\rightarrow$ Duyệt), không có nhiều nhánh rẽ phức tạp.

👉 **Bài của nhóm nằm ở ô: Độ mơ hồ Trung bình × Độ phức tạp Thấp–Trung bình $\longrightarrow$ Phù hợp nhất với mức WORKFLOW.**

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Chuẩn hóa checklist cho recruiter hoặc thử form ngắn gồm các câu hỏi về tiêu chí bắt buộc | Đủ khi tiêu chí ổn định và khâu đọc thủ công đã nằm trong mức chấp nhận được | Form dài có thể làm ứng viên bỏ dở. Tác động của form ngắn chưa được đo | Dùng checklist làm đối chứng |
| **Rule** | Dùng script Regex / Python tìm kiếm từ khóa cứng (keywords) trong file text | Đủ khi CV theo đúng một mẫu chuẩn và từ khóa viết chính xác 100% | Bị đánh lừa bởi từ khóa ẩn (keyword stuffing); bỏ sót từ đồng nghĩa; không đọc được ngữ cảnh kinh nghiệm | Không chọn làm giải pháp chính |
| **Workflow** | **Rule tách text $\rightarrow$ AI trích xuất thông tin có cấu trúc kèm trích dẫn ngữ cảnh $\rightarrow$ Hiển thị giao diện đối chiếu để Recruiter duyệt** | **Đủ khi các bước quy trình cố định, AI đảm nhận khâu đọc hiểu văn bản phi cấu trúc, con người ra quyết định** | AI trích xuất sót thông tin nếu CV scan quá mờ (xử lý bằng cờ cảnh báo lỗi định dạng) | **CHỌN** ✅ |
| **Agent** | Agent tự đọc CV, tự suy luận, tự tìm thêm thông tin mạng xã hội/GitHub của ứng viên, tự gửi thư phỏng vấn hoặc thư từ chối | Khi quy trình đòi hỏi tương tác đa bước không đoán trước được | Chi phí rất cao, rủi ro ảo giác (hallucination), vi phạm quyền riêng tư và thiếu sự kiểm soát của con người | Không chọn |

**Mức chọn:** **Workflow** (Quy trình bán tự động có con người duyệt).

**Vì sao không chọn mức đơn giản hơn:** 
- Phương án **No AI** với checklist chuẩn hóa là đối chứng cho pilot. Trải nghiệm CP4 cho thấy form dài có thể tạo thêm việc cho ứng viên. Nhóm cần đo trước khi kết luận về form ngắn.
- Phương án **Rule** (lọc từ khóa Regex) không thể hiểu được ngữ cảnh (ví dụ: ứng viên ghi "từng tham gia khóa học Java 1 tuần" thì Rule vẫn đếm là có từ khóa "Java", dẫn đến kết quả sai lệch nghiêm trọng). Do đó, cần khả năng đọc hiểu ngữ nghĩa của AI ở khâu trích xuất.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** | Bản tóm tắt có cấu trúc: (1) Số năm kinh nghiệm liên quan, (2) Danh sách kỹ năng khớp tiêu chí, (3) Đoạn văn bản trích dẫn làm bằng chứng kèm số trang tương ứng trong CV. |
| **Judgment** | Chuyên viên tuyển dụng (Recruiter) cân nhắc: Bằng chứng trích xuất có đủ uy tín không? Ứng viên có xứng đáng vào vòng phỏng vấn sơ bộ không? |
| **Action** | Recruiter bấm nút chọn phân loại: **Đạt (Shortlist)** / **Dự phòng** / **Loại**; hệ thống tự động lưu trạng thái vào bảng theo dõi. |
| **Outcome** | Thời gian sàng lọc giảm từ 125 phút xuống dưới 35 phút; tỷ lệ bỏ sót ứng viên đạt chuẩn dưới 2%; không có khiếu nại về thiên vị hay lỗi kỹ thuật. |
| **Input** | File CV của ứng viên (PDF/Word) + Tiêu chí cứng từ Job Description (danh sách tiêu chí dạng bullet points). Dữ liệu hoàn toàn có sẵn trong mỗi đợt tuyển dụng. |
| **Feedback** | Thao tác chỉnh sửa của Recruiter: nếu Recruiter sửa trạng thái từ "Không đạt" thành "Đạt" và ghi chú lý do, hệ thống ghi nhận log để tinh chỉnh prompt/schema cho đợt sau. |

### 6.4. Hai câu hỏi của Google PAIR

- **Người dùng muốn được hỗ trợ (augment) hay giao hẳn việc (automate)?**
  - **Trả lời: Được hỗ trợ (Augment).**
  - *Bằng chứng:* 100% người được phỏng vấn ở CP4 (cả chuyên viên HR lẫn trưởng ban tuyển dụng CLB) đều khẳng định họ cần giữ quyền kiểm soát quyết định tuyển người. Họ chỉ muốn AI giải phóng đôi mắt khỏi việc đọc lướt nhàm chán bằng cách bôi vàng sẵn bằng chứng, chứ không bao giờ tin tưởng giao toàn quyền cho máy tự loại ứng viên.
- **AI sai kiểu nào tệ hơn, báo nhầm (False Positive) hay bỏ sót (False Negative)?**
  - **Trả lời: Bỏ sót (False Negative - loại nhầm ứng viên tốt) tệ hơn rất nhiều so với báo nhầm.**
  - *Vì sao & Thiết kế xử lý:* Nếu báo nhầm (chọn nhầm một hồ sơ yếu vào shortlist), Recruiter chỉ mất thêm 30 giây liếc mắt là loại được ngay. Nhưng nếu bỏ sót (đánh trượt một nhân tài chỉ vì viết CV khác chuẩn), công ty mất cơ hội tuyển dụng và lãng phí chi phí tìm kiếm.
  - *Xử lý trong thiết kế:* Hệ thống được tinh chỉnh theo hướng **khoan dung (high recall)**: khi độ phù hợp nằm ở ranh giới nghi vấn, AI luôn xếp vào nhóm "Cần con người xem xét thêm" chứ không bao giờ tự ý gạt bỏ.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Chuyên viên tuyển dụng (Recruiter) tại các doanh nghiệp vừa và nhỏ hoặc người phụ trách nhân sự tại các đội nhóm/CLB |
| **Quy trình** | Tải CV $\rightarrow$ Rule kiểm tra định dạng $\rightarrow$ AI trích xuất bằng chứng theo tiêu chí JD $\rightarrow$ Recruiter duyệt bảng đối chiếu trực quan $\rightarrow$ Tự động lưu trữ danh sách Shortlist |
| **Bottleneck** | Não bộ bị quá tải nhận thức khi đọc lướt đối chiếu tiêu chí cứng trên hàng chục CV định dạng phi cấu trúc |
| **Impact** | Tốn hơn 2 giờ/đợt 100 CV; tỷ lệ bỏ sót ước tính khoảng 8% trong Card #1, chưa xác nhận mẫu số; nguy cơ tuyển hụt người giỏi |
| **Success Metric** | (1) Dưới 35 phút/100 CV, so với mốc tham chiếu 125 phút/100 CV. So quy trình thủ công và Workflow trên các lô tương đương bằng cùng mốc đo, gồm thời gian xem tay ngoại lệ. (2) Tỷ lệ bỏ sót hồ sơ đạt tiêu chí dưới 2%, đo theo đối chiếu độc lập ở mục 8.2. (3) Mục tiêu dưới 10% hồ sơ cần mở lại để đọc toàn bộ, tính trên mọi hồ sơ trong nhánh Workflow. |
| **Boundary** | AI tuyệt đối không tự quyết định loại bỏ ứng viên; không tự gửi thư từ chối; chỉ trích xuất dữ liệu có trong văn bản, không suy diễn; mọi file lỗi định dạng phải chuyển cho con người xem tay |
| **AI intervention point** | Tại khâu trích xuất thông tin: ngay sau khi Rule đọc xong văn bản thô từ file CV và trước khi đưa lên màn hình cho Recruiter duyệt |
| **Mức chọn** | **Workflow** (Quy trình chuẩn hóa có AI hỗ trợ trích xuất, con người duyệt cuối) |
| **Rủi ro & người kiểm tra** | Rủi ro nhồi từ khóa ẩn, AI đọc sót do layout lạ $\rightarrow$ Recruiter là người kiểm tra trực tiếp thông qua đoạn trích dẫn bằng chứng (snippet) và số trang |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| **Actor** | Nhân viên tuyển dụng nói chung | Bổ sung: Chuyên viên tại SME hoặc phụ trách nhân sự đội nhóm/CLB | Phỏng vấn CP4 cho thấy các nhóm quy mô này có nỗi đau lớn nhất vì không có ngân sách mua các hệ thống ATS đắt tiền |
| **Success Metric** | Chỉ đo thời gian (125' $\rightarrow$ 35') và tỷ lệ sót (<2%) | Bổ sung: Tỷ lệ Recruiter phải mở lại file gốc để đọc dưới 10% | Phản biện CP5: đo lường xem giải pháp trích xuất bằng chứng có thực sự giúp người dùng không phải mở lại file đọc thủ công hay không |
| **Ranh giới & Điểm can thiệp** | Chỉ ghi cấm AI tự loại hồ sơ | Xác định rõ điểm can thiệp nằm giữa khâu tách text thô và khâu duyệt của người | Giúp định hình chính xác kiến trúc kỹ thuật của giải pháp Workflow |

**Tiêu chí đánh giá đầu ra của AI (Eval Criteria - 4 tiêu chí cốt lõi):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | **Tính trung thực của trích dẫn (Faithfulness / No Hallucination)** | 100% đoạn trích dẫn (snippet) đưa ra phải tìm thấy nguyên văn hoặc tương đương ngữ nghĩa trong file CV của ứng viên, kèm đúng số trang | AI tự bịa ra thông tin kinh nghiệm hoặc kỹ năng không hề có trong file CV |
| 2 | **Độ bao phủ tiêu chí cứng (Coverage / Recall)** | Trích xuất đủ 100% các tiêu chí cứng có xuất hiện trong CV (ví dụ: bằng Đại học, chứng chỉ ngoại ngữ, số năm làm việc) | Bỏ sót tiêu chí cứng mà ứng viên có nêu rõ ràng trong văn bản |
| 3 | **Phát hiện gian lận & bất thường (Anomaly Flagging)** | Gắn cờ cảnh báo nếu phát hiện dấu hiệu bất thường: danh sách từ khóa dày đặc không có mô tả dự án, chữ ẩn trùng màu nền, hoặc file scan mờ | Làm theo chỉ thị nhúng trong CV, dùng từ khóa rời làm bằng chứng, hoặc không gắn cờ hồ sơ lỗi đã biết trong ca thử |
| 4 | **Định dạng đầu ra chuẩn hóa (Schema Conformance)** | Trả về đúng định dạng JSON/bảng đối chiếu theo quy chuẩn: Tên ứng viên, Tiêu chí, Trạng thái (Có bằng chứng / Chưa thấy bằng chứng / Cần con người xem xét thêm), Bằng chứng trích dẫn và Số trang nếu có | Trả về văn bản tự do, thiếu trường dữ liệu hoặc lỗi cấu trúc khiến hệ thống không hiển thị được |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | **Thấp** | Phỏng vấn và poll cho tín hiệu về khâu đọc CV tốn thời gian. Pilot đo mức tiết kiệm và chất lượng trước khi quyết định mở rộng. |
| **Usability** | Người dùng có kiểm tra và sửa được đầu ra không? | **Trung bình** | Bảng trích dẫn và số trang hỗ trợ đối chiếu. Cần quan sát số lần recruiter phải mở lại CV và kiểm tra luồng xử lý hồ sơ chưa rõ. |
| **Feasibility** | Có đủ dữ liệu, công cụ và kỹ năng không? | **Trung bình** | Cần thử độ chính xác trên CV nhiều cột, CV scan và văn bản chứa chỉ thị nhúng. Hồ sơ lỗi được chuyển sang đọc tay. |
| **Viability** | Có hợp chi phí, chính sách dữ liệu và năng lực vận hành không? | **Trung bình** | Chưa có chi phí đo được. Trước khi dùng CV thật, cần có người phụ trách dữ liệu của đơn vị tuyển dụng phê duyệt dữ liệu được gửi, quyền truy cập và thời hạn lưu. |

### 8.2. Kết luận

**Quyết định: GO (Triển khai thử nghiệm pilot phạm vi hẹp).**

**Lý do:** Có bằng chứng ban đầu về việc đọc CV tốn thời gian, đủ để thử Workflow ở phạm vi hẹp. Nhóm bắt đầu bằng hồ sơ giả lập hoặc hồ sơ đã khử định danh được phép sử dụng. Chỉ thử với CV thật sau khi đơn vị tuyển dụng xác nhận cách xử lý dữ liệu.

**Nếu Go — pilot nhỏ nhất (2 tuần thử nghiệm):**
1. **Phạm vi thử nghiệm:** Trong hai tuần, dùng một bộ khoảng 50–80 CV cho cùng một vị trí. Chạy ở chế độ đối chiếu, không dùng kết quả thử để gửi thư hoặc tự chuyển vòng ứng viên.
2. **Cách làm thực nghiệm:** So sánh checklist thủ công với Workflow trên các lô tương đương và đổi thứ tự giữa người duyệt để giảm hiệu ứng quen hồ sơ. Dùng cùng bộ tiêu chí, ghi thời gian từ lúc gom hồ sơ đến lúc lưu shortlist. Ghi tổng thời gian, phút/CV, thời gian đọc tay ngoại lệ và chi phí thực tế trên mỗi CV.
3. **Đối chiếu chất lượng:** Một người tuyển dụng đọc CV gốc theo checklist mà không xem đầu ra AI để xác định hồ sơ đạt tiêu chí. Báo cáo số hồ sơ đạt chuẩn bị loại và tổng số hồ sơ đạt chuẩn, cùng tỷ lệ phải mở lại CV. Nếu mẫu nhỏ, ghi số đếm và xem kết quả là tín hiệu pilot trước khi kết luận mục tiêu dưới 2% đã đạt.

**Ngưỡng dừng (Stop condition):**
- Dừng nhánh thử và rà lỗi ngay nếu phát hiện một hồ sơ đạt chuẩn bị loại do đầu ra Workflow hoặc hệ thống làm theo chỉ thị nhúng trong CV. Quay về checklist thủ công trong lúc sửa.
- Sau hai tuần, quay về checklist thủ công nếu trên 15% CV có lỗi trích xuất ảnh hưởng đến việc duyệt, hoặc chi phí thực tế vượt ngưỡng đề xuất 5.000 VNĐ/CV. Báo cáo số liệu cho nhóm trước khi quyết định thử lại.

---

## 9. Hạn chế và hướng tiếp theo

- **Hạn chế hiện tại:** Bộ dữ liệu kiểm chứng mới dừng ở quy mô phỏng vấn sâu 3 người và khảo sát 8 người trong môi trường sinh viên/SME; cần mở rộng dữ liệu đo lường ở các tập đoàn lớn có cổng ATS chuyên dụng.
- **Hướng tiếp theo:** 
  1. Thử nghiệm các mô hình OCR mã nguồn mở chuyên sâu về xử lý bảng biểu và layout phức tạp để nâng cao độ chính xác ở bước trích xuất văn bản.
  2. Xây dựng bộ dataset benchmark gồm 50 CV chuẩn kèm ground-truth đánh giá của các chuyên gia tuyển dụng để chạy automated eval cho hệ thống.

---

## 10. Tài liệu tham khảo

1. Google People + AI Research (PAIR) Guidebook: *Human-Centered AI Patterns & Best Practices* (https://pair.withgoogle.com/).
2. Rob Fitzpatrick: *The Mom Test: How to talk to customers & learn if your business is a good idea when everyone is lying to you* (2013).
3. Teresa Torres: *Continuous Discovery Habits: Discover Products that Create Customer Value and Business Value* (2021) — Framework Opportunity Solution Tree (OST).

