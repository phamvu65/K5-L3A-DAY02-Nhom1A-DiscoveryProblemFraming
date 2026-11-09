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
