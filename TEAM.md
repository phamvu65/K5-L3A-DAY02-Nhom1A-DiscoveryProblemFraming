# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: Nhom1A
- Candidate problem nhóm chọn (1 câu): Khi nhận được hàng trăm CV ứng tuyển cho một vị trí, nhân viên tuyển dụng muốn xác định nhanh nhóm ứng viên phù hợp với tiêu chí cốt lõi, để không mất quá nhiều thời gian đọc lướt thủ công mà vẫn không bỏ sót ứng viên tiềm năng.
- Quyết định cuối (Go / Not Yet / No-Go): Go (Thử nghiệm pilot phạm vi hẹp)

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Phạm Tuấn Anh | 2A202603503 | Đề xuất bài toán chính, Phản biện | phamtuananhhatay |
| 2 | Phạm Nguyên Vũ | 2A202603436 | Nghiên cứu giải pháp, Kiểm chứng | phamvu65 |
| 3 | Nguyễn Quỳnh Trang | 2A202603477 | Thư ký ghi chép, Vẽ quy trình | Trang-1234567 |
| 4 | Nguyễn Khắc Khánh | 2A202603472 | Phân tích rủi ro, Kiểm chứng | khackhanh1201 |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Phạm Tuấn Anh | Vũ, Trang, Khánh | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Phạm Nguyên Vũ | Nguyễn Khắc Khánh | Assumption map, snapshot hoặc survey |
| CP4 — Research | Nguyễn Quỳnh Trang | Tuấn Anh, Vũ | Bảng research có link |
| CP5 — Quy trình trước/sau | Nguyễn Quỳnh Trang | Phạm Tuấn Anh | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | Phạm Tuấn Anh | Cả nhóm | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Phạm Tuấn Anh | Phạm Nguyên Vũ | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Nguyễn Khắc Khánh | Cả nhóm | 4 rủi ro + Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### PhamTuanAnh-2A202603503

**Phần việc phụ trách:**

- Đề xuất bài toán hạt nhân (CV Screening), điều phối thảo luận hội tụ CP3, chốt Success Metric, thiết kế kiến trúc Workflow có HITL (Human-in-the-loop) và hoàn thiện Problem Statement v0/v1.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đề xuất Card #1 với các chỉ số đo lường thực tế (125' xuống 35', tỷ lệ sót từ ~8% xuống < 2%); bảo vệ thành công bài toán trước các câu hỏi phản biện của nhóm về rủi ro prompt injection và CV dạng ảnh.
- Phân tích và xây dựng ma trận so sánh 4 mức can thiệp (No AI / Rule / Workflow / Agent), chứng minh vì sao mức Workflow là điểm cân bằng tối ưu.
- Thiết lập bộ 4 tiêu chí đánh giá (Eval) cho AI và đề xuất ngưỡng dừng dự án (Stop condition) có thể đo đếm được.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `group_report.md`: Mục 2.1 (Pitch), Mục 2.4 (Chấm điểm shortlist), Mục 4.2 (Quy trình tương lai), Mục 5 (Problem Statement v0), Mục 6.1–6.4 (Mức can thiệp AI), Mục 7 (Problem Statement v1 & Eval), Mục 8 (Quyết định & Ngưỡng dừng).
- File cá nhân `report/individual/2A202603503_PhamTuanAnh.md`: Hoàn thành 100% mục 1–7.

**Điều mình học được từ phần nhóm:**

- Hiểu sâu sắc sự khác biệt giữa Solution trá hình ("cần một chatbot AI") và Problem thật ("quá tải nhận thức khi đọc lướt 100 CV"). Nhận ra rằng giá trị lớn nhất của AI không phải là tự động hóa thay thế con người (Agent), mà là làm trợ lý trích xuất và hiển thị bằng chứng (Workflow) để con người ra quyết định nhanh và chính xác hơn.

### PhamNguyenVu-2A202603436

**Phần việc phụ trách**

- Tham gia pitch, phản biện và chọn đề tài ở CP3. Theo phân công, tôi phụ trách kiểm chứng cùng Khánh, hỗ trợ Trang nghiên cứu giải pháp ở CP4 và hỗ trợ Tuấn Anh rà soát Problem Statement v1, mức can thiệp và tiêu chí đánh giá ở CP6.

**Đóng góp cụ thể**

- Trình bày ba vấn đề gồm báo cáo quảng cáo hằng tuần, đối soát cuối ca và xác nhận đơn hàng qua chat. Đặt câu hỏi cho Tuấn Anh về việc dùng ghi chú phỏng vấn để đối chiếu với JD, cho Trang về việc dùng bảng cập nhật chung và cho Khánh về phương án chia tiền bằng bảng tính hoặc ứng dụng có sẵn. Tham gia thảo luận và đồng ý chọn đề tài sàng lọc CV vì quy trình và tiêu chí đo rõ hơn.
- Khi rà CP4, tôi ghi nhận bảng tổng hợp cần tách phản hồi của ứng viên về form nộp đơn khỏi bằng chứng của người tuyển dụng về việc đọc CV. Tôi cũng ghi nhận các nhận định về công cụ cần dẫn đến nguồn cụ thể.
- Khi rà CP5–CP6, tôi đề xuất thống nhất phạm vi đo thời gian giữa baseline 100 CV và pilot 50–80 CV, tính cả thời gian đọc tay hồ sơ ngoại lệ, làm rõ mẫu số của tỷ lệ bỏ sót khoảng 8% và bổ sung trạng thái “Cần con người xem xét thêm” vào tiêu chí đánh giá.

**Bằng chứng**

- [Báo cáo nhóm](report/team/group_report.md), mục 2.1, dòng #4–#6 ghi các đề tài tôi pitch và dòng #2, #8, #11 ghi các câu hỏi tôi đặt. Mục 2.4 ghi kết quả shortlist.
- [Báo cáo cá nhân của Phạm Nguyên Vũ](report/individual/2A202603436_PhamNguyenVu.md), mục 4–5 ghi nhật ký tham gia và các điểm tôi ghi nhận khi rà CP4–CP6.

**Điều mình học được từ phần nhóm**

- Tôi học được cách tách thời gian của bước nghẽn khỏi thời gian của cả quy trình. Với bài toán sàng lọc CV, tôi thấy việc xác định ai kiểm tra hồ sơ đạt chuẩn và đo tỷ lệ bỏ sót cũng quan trọng như đo thời gian. Bằng chứng trích từ CV giúp người tuyển dụng kiểm tra đầu ra trước khi quyết định phân loại.

### NguyenKhacKhanh-2A202603472

**Phần việc phụ trách:**

- Đảm nhận vai trò chính ở CP6 — Quyết định (phân tích 4 rủi ro Value / Usability / Feasibility / Viability, thiết lập quyết định Go và xây dựng bộ Stop Conditions).
- Phụ trách kiểm chứng ở CP4 cùng Vũ: tham gia xây dựng Assumption Map, tiến hành phỏng vấn sâu theo phương pháp The Mom Test và chạy micro-survey thu thập dữ liệu thực tế.
- Tham gia pitch 3 bài toán cá nhân, phản biện đồng đội ở CP3, hỗ trợ phân loại cụm vấn đề (Cluster) và tham gia chấm điểm shortlist lựa chọn bài toán chung cho nhóm.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- **CP3 (Hội tụ nhóm):** Pitch 3 candidate (#10 Rà soát bài lab theo rubric, #11 Chia tiền sau buổi đi chơi nhóm, #12 Duy trì tập trung khi tự học). Card #11 đạt 26/35 điểm ở vòng chấm sơ bộ. Tiếp thu phản biện của Tuấn Anh và Vũ về việc chia tiền đã có thể giải quyết tốt bằng Rule/Excel hoặc app ngân hàng, từ đó đồng thuận 100% cùng nhóm hội tụ vào Candidate 1 (Sàng lọc CV).
- **CP4 (Kiểm chứng):** Đồng xây dựng Assumption Map đánh giá mức độ rủi ro của 6 giả định; trực tiếp tham gia phỏng vấn The Mom Test (người tuyển quân CLB, sinh viên tìm việc) và micro-survey với 8 người. Thu thập được insight mấu chốt: người tuyển dụng cần đoạn trích bằng chứng (snippet + số trang) để đối chiếu nhanh chứ không chấp nhận AI tự chấm điểm hay tự ý loại hồ sơ.
- **CP6 (Đánh giá 4 rủi ro & Quyết định):** Phụ trách chính nội dung Mục 8 trong báo cáo nhóm:
  + Phân tích ma trận 4 rủi ro (Value: Thấp; Usability: Trung bình; Feasibility: Trung bình; Viability: Trung bình).
  + Lập luận bảo vệ quyết định **GO (Thử nghiệm pilot phạm vi hẹp)** trên tập 50–80 CV cho một vị trí trong 2 tuần, thiết kế thực nghiệm A/B đối chứng với quy trình thủ công.
  + Thiết lập 2 Ngưỡng dừng (Stop condition) cụ thể: Dừng ngay lập tức nếu phát hiện 1 hồ sơ đạt chuẩn bị loại do lỗi trích xuất hoặc hệ thống dính prompt injection; dừng sau 2 tuần nếu tỷ lệ lỗi trích xuất ảnh hưởng việc duyệt > 15% hoặc chi phí xử lý thực tế vượt ngưỡng 5.000 VNĐ/CV.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- [Báo cáo nhóm](report/team/group_report.md):
  + Mục 2.1 (dòng #10, #11, #12): 3 bài toán pitch cá nhân và câu hỏi phản biện nhận được.
  + Mục 2.2 & 2.4: Đóng góp hình thành Cluster C, D và kết quả chấm điểm shortlist Candidate 11 (26/35 điểm).
  + Mục 3.1 & 3.2: Assumption Map (6 giả định) và tổng hợp kết quả kiểm chứng qua phỏng vấn The Mom Test và micro-survey (8 người).
  + Mục 8.1 & 8.2: Trực tiếp xây dựng toàn bộ bảng Bốn rủi ro (Value, Usability, Feasibility, Viability), kết luận Go thử nghiệm pilot 2 tuần và 2 ngưỡng dừng (Stop conditions).
- [Báo cáo cá nhân của Nguyễn Khắc Khánh](report/individual/2A202603472_NguyenKhacKhanh.md): Hoàn thiện 5 Job Stories (CP1), 3 Problem Cards (CP2), và nhật ký hoạt động tham gia cùng nhóm (CP3–CP6).

**Điều mình học được từ phần nhóm:**

- Tôi học được cách tiếp cận bài toán bằng tư duy rủi ro và kiểm chứng giả định thực tế thay vì vội vã tin vào sức mạnh công nghệ. Khi bài toán chia tiền của tôi bị phản biện rằng "Rule/Excel hay app ngân hàng đã giải quyết được 80%", tôi nhận ra ranh giới giữa một vấn đề thực tế cần giải pháp công nghệ đơn giản và một vấn đề phi cấu trúc thực sự cần đến AI.
- Trong khâu kiểm chứng, phương pháp The Mom Test giúp tôi nhận ra rằng nếu hỏi trực diện "bạn có muốn dùng AI không", người dùng sẽ dễ khen xã giao; chỉ khi đào sâu vào hành vi quá khứ và những trải nghiệm thực tế (thức tới 1h sáng, mỏi mắt sau 30 CV, từ chối công cụ nếu không có đoạn trích chứng minh) thì nút thắt và rào cản usability thực sự mới bộc lộ.
- Đặc biệt, khi phụ trách khâu Quyết định (Go/No-Go), tôi hiểu rằng một quyết định "Go" có trách nhiệm không phải là vội vã xây dựng toàn bộ hệ thống, mà là thiết kế một pilot nhỏ có kiểm soát (Human-in-the-loop, AI chỉ trích xuất bằng chứng) cùng các ngưỡng dừng (Stop conditions) định lượng rõ ràng để sẵn sàng dừng lại khi chi phí hoặc độ chính xác không đạt kỳ vọng.

