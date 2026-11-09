# Báo cáo cá nhân — 2A202603436_PhamNguyenVu

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Phạm Nguyên Vũ
- MSSV:2A202603436
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm:Nhom1A
- Link repo nhóm:https://github.com/phamvu65/K5-L3A-DAY02-Nhom1A-DiscoveryProblemFraming.git

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại, tốn thời gian, tổng hợp thông tin | Khi chuẩn bị cho buổi họp tối hằng tuần, tôi muốn rút ngắn thời gian tổng hợp kết quả chạy quảng cáo để kịp chuẩn bị đủ thông tin trình bày. | Tôi, người chạy quảng cáo và lập báo cáo tuần. | Tôi mất khoảng 1–2 giờ mỗi tuần để chuẩn bị toàn bộ báo cáo. Tổng hợp doanh số theo ngày và chi phí từ các tài khoản quảng cáo là bước lâu nhất. Tôi chưa đo riêng bước này. |
| 2 | Tốn thời gian | Khi kết ca, tôi muốn xác định nhanh khoản chênh lệch giữa số tiền thực nhận và tổng tiền trên hóa đơn để chốt ca. | Người đối soát cuối ca ở quán ăn. | Có ca mất thời gian dò lại để tìm khoản chênh lệch. |
| 3 | Pain từ người khác | Khi ghi món khách gọi vào giờ cao điểm, tôi muốn biết món nào đã hết để khách chọn được món quán còn phục vụ. | Nhân viên phục vụ và khách. | Trong giờ cao điểm buổi tối (19h–22h), khi bếp báo hết món chậm, nhân viên phục vụ phải quay lại bàn và mất thêm thời gian để khách chọn món khác. |
| 4 | Cần tổng hợp thông tin | Khi lên lịch chăm sóc một luống, tôi muốn biết lần gần nhất luống đó được tưới hoặc bón phân để lên kế hoạch cho lần tiếp theo. | Người chăm sóc luống. | Có lần phải tra lại sổ, tìm tin nhắn hoặc hỏi người làm cùng để biết thời điểm chăm sóc gần nhất. |
| 5 | Cần tổng hợp thông tin | Khi chuẩn bị đóng một đơn đã được sửa qua chat, tôi muốn xác nhận mẫu, số lượng và địa chỉ mới nhất để giao đúng đơn khách đã chốt. | Người chốt đơn và đóng hàng. | Mất khoảng 3–5 phút dò lại tin nhắn để xác nhận thông tin và tránh đóng nhầm đơn. |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Tạm giữ bốn tình huống ở dòng 2–5 để đối chiếu với trải nghiệm thật. Chúng có bước cần quan sát và chỉ số có thể đo.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Tổng hợp báo cáo quảng cáo hằng tuần | Tôi trực tiếp làm việc này mỗi tuần và có thể bấm giờ ở lần làm tiếp theo. | Chưa biết thao tác nào trong khâu tổng hợp chiếm nhiều thời gian nhất. |
| 2 | Đối soát tiền cuối ca ở quán ăn | Có thể đo thời gian truy khoản lệch. | Card dự kiến, cần xác nhận tình huống thực tế. |
| 3 | Chốt thông tin đơn hàng qua chat | Có thể quan sát bước xác nhận trước khi đóng hàng. | Card dự kiến, cần xác nhận tình huống thực tế. |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi chuẩn bị cho buổi họp tối hằng tuần, tôi muốn rút ngắn thời gian tổng hợp kết quả chạy quảng cáo để có đủ thông tin trình bày. |
| Actor | Tôi, người chạy quảng cáo và lập báo cáo tuần. |
| Thời điểm / bối cảnh | Trước buổi họp tối hằng tuần. |
| Quy trình hiện tại (3–7 bước) | Lấy doanh số từng ngày từ bảng doanh thu → lấy chi phí từ các tài khoản quảng cáo → tổng hợp số liệu thành báo cáo tuần → trình bày trong buổi họp tối. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước lâu nhất là tổng hợp doanh số và chi phí quảng cáo thành báo cáo tuần. Chưa đo riêng bước này. Toàn bộ phần chuẩn bị báo cáo mất khoảng 1–2 giờ. |
| Impact (nếu không giải thì sao) | Tôi phải dành thời gian tổng hợp trước buổi họp mỗi tuần. |
| Success metric (baseline → target) | Baseline ước tính: 60–120 phút mỗi báo cáo. Mục tiêu đề xuất: giảm ít nhất 25% thời gian chuẩn bị so với baseline đo được, vẫn đủ doanh số và chi phí cho buổi họp. Bấm giờ từ lúc bắt đầu lấy số liệu đến khi báo cáo sẵn sàng và ghi riêng thời gian tổng hợp. |
| Phương án không dùng AI | Dùng mẫu báo cáo tuần với danh sách chỉ số và định dạng thống nhất. |
| Giả thuyết về AI (nếu có) | Nếu viết nhận xét là bước nghẽn, có thể thử hỗ trợ soạn nháp từ số liệu đã kiểm tra. |
| Cảm nhận nhanh | Chưa biết. Cần đo bước nghẽn trước khi chọn mức can thiệp. |

Quy trình nháp hiện tại:

```text
Lấy doanh số từ bảng doanh thu → Lấy chi phí từ các tài khoản quảng cáo → Tổng hợp báo cáo tuần [bước nghẽn] → Trình bày trong buổi họp tối
```

### Problem Card #2

**Đối soát tiền cuối ca ở quán ăn · giả thuyết cần xác nhận**

| Trường | Nội dung |
|---|---|
| Job Story | Khi kết ca, tôi muốn tìm nhanh khoản chênh giữa tiền nhận và hóa đơn để chốt số tiền của ca. |
| Actor | Người đối soát cuối ca. |
| Thời điểm / bối cảnh | Cuối ca bán hàng. |
| Quy trình hiện tại (3–7 bước) | Giả định: Lấy tổng hóa đơn → cộng tiền mặt và chuyển khoản → so tổng → dò khoản lệch → chốt ca. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Dò giao dịch lệch theo từng hóa đơn. Chưa đo thời lượng. |
| Impact (nếu không giải thì sao) | Có thể kéo dài thời gian chốt ca. |
| Success metric (baseline → target) | Baseline chưa đo. Mục tiêu đề xuất: giảm ít nhất 25% thời gian đối soát ở các ca có khối lượng giao dịch tương đương, với mọi khoản lệch vẫn được ghi nhận. Bấm giờ từ lúc bắt đầu lấy tổng hóa đơn đến khi chốt ca. |
| Phương án không dùng AI | Dùng bảng đối chiếu theo mã hóa đơn và phương thức thanh toán. |
| Giả thuyết về AI (nếu có) | Chưa đặt giả thuyết. |
| Cảm nhận nhanh | Chưa biết. Cần xác nhận quy trình và bước nghẽn. |

Quy trình nháp hiện tại:

```text
Lấy tổng hóa đơn → cộng tiền mặt và chuyển khoản → so tổng → dò khoản lệch → chốt ca.
```

### Problem Card #3

**Chốt thông tin đơn hàng qua chat · giả thuyết cần xác nhận**

| Trường | Nội dung |
|---|---|
| Job Story | Khi đóng một đơn đã được khách sửa qua chat, tôi muốn xác nhận thông tin cuối cùng để giao đúng đơn khách chốt. |
| Actor | Người chốt đơn hoặc đóng hàng. |
| Thời điểm / bối cảnh | Trước khi đóng một đơn có thay đổi qua chat. |
| Quy trình hiện tại (3–7 bước) | Giả định: Mở hội thoại → dò các thay đổi → xác nhận thông tin cuối → đóng hàng. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Dò tin nhắn để xác nhận mẫu, số lượng và địa chỉ mới nhất, ước tính khoảng 3–5 phút cho một đơn có thay đổi theo ghi nhận ở CP1. |
| Impact (nếu không giải thì sao) | Có thể chậm đóng hàng hoặc đóng sai đơn. |
| Success metric (baseline → target) | Baseline ước tính cho bước dò tin nhắn: 3–5 phút mỗi đơn có thay đổi. Mục tiêu đề xuất: xác nhận được thông tin cuối cùng trong tối đa 2 phút mỗi đơn mà số đơn đóng nhầm không tăng. Bấm giờ từ lúc bắt đầu kiểm tra thay đổi đến khi xác nhận đủ mẫu, số lượng và địa chỉ. |
| Phương án không dùng AI | Gửi một bản tóm tắt đơn cuối cho khách xác nhận rồi dùng bản đó để đóng hàng. |
| Giả thuyết về AI (nếu có) | Chưa đặt giả thuyết. |
| Cảm nhận nhanh | Chưa biết. Cần xác nhận quy trình và bước nghẽn. |

Quy trình nháp hiện tại:

```text
Mở hội thoại → dò các thay đổi → xác nhận thông tin cuối → đóng hàng.
```

### Card muốn pitch nhất

- Card số: 1.
- Vì sao: Tôi trực tiếp làm báo cáo quảng cáo hằng tuần và có thể theo dõi thời gian từng bước.
- Câu hỏi muốn nhóm phản biện: Nên tách khâu tổng hợp thành những thao tác nào để đo được bước nghẽn?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Card chưa nói rõ tôi lấy số liệu từ đâu và chưa phân biệt thời gian tổng hợp với thời gian chuẩn bị toàn bộ báo cáo. | Đồng ý. Tôi lấy số liệu từ hai nguồn, sau đó mới tổng hợp. Tổng hợp là bước lâu nhất. | Tôi bổ sung bảng doanh thu và các tài khoản quảng cáo vào sơ đồ, đánh dấu bước tổng hợp là bước nghẽn và ghi 1–2 giờ là ước lượng cho toàn bộ phần chuẩn bị. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Tôi trình bày ba vấn đề: tổng hợp báo cáo quảng cáo hằng tuần, đối soát tiền cuối ca ở quán ăn và xác nhận thông tin đơn hàng qua chat. | Ba vấn đề được ghi ở dòng #4–#6 của bảng pitch. Báo cáo quảng cáo vào shortlist và đạt 27/35 điểm sau khi chấm lại. |
| Phản biện bài của bạn khác | Tôi hỏi Tuấn Anh liệu ghi chú phỏng vấn ngắn và cảm tính có đủ để AI đối chiếu chính xác với JD. Tôi hỏi Trang liệu dùng một Google Sheet chung có giảm khâu tổng hợp báo cáo tuần. Tôi hỏi Khánh liệu bảng tính hoặc app chia tiền có đủ để xử lý vấn đề. | Các câu hỏi được ghi ở dòng #2, #8 và #11 của bảng pitch. |
| Nhận phản biện | Tuấn Anh hỏi mẫu Excel có công thức hoặc kết nối dữ liệu vào Looker Studio có thể giảm bao nhiêu thời gian và có cần dùng AI hay không. | Trong Card #1, tôi ghi mẫu báo cáo tuần là phương án không dùng AI. Tôi làm rõ 60–120 phút là ước lượng cho toàn bộ phần chuẩn bị, còn bước tổng hợp chưa được đo riêng. |
| Gom cluster / cây OST | Tôi được phân công hỗ trợ CP3 cùng Trang và Khánh. | Báo cáo quảng cáo vào cụm tổng hợp thông tin và lập báo cáo. Đối soát cuối ca và xác nhận đơn hàng vào cụm điều phối và đối soát tác vụ. |
| Chọn candidate problem | Tôi đồng ý chọn đề tài sàng lọc sơ bộ CV của Tuấn Anh vì quy trình và tiêu chí đo rõ hơn. | Đề tài sàng lọc CV đạt 28/35 điểm. Đề tài báo cáo quảng cáo mới có baseline ước tính và nhóm thấy có thể thử xử lý bằng bảng tính hoặc dashboard. |
| Kiểm chứng / research (CP4) | Tôi được giao phụ trách kiểm chứng cùng Khánh và hỗ trợ Trang nghiên cứu giải pháp hiện có. Báo cáo nhóm ghi kết quả chung, chưa ghi tôi thực hiện buổi phỏng vấn nào hoặc kiểm tra nguồn nào. | Nhóm dùng kết quả CP4 để thu hẹp phạm vi: trích xuất bằng chứng kèm số trang và chuyển CV lỗi định dạng sang đọc thủ công. Xem mục 3 của báo cáo nhóm. |
| Quy trình nhóm (CP5) | Tôi đối chiếu sơ đồ trước và sau khi rà báo cáo nhóm. Trang và Tuấn Anh phụ trách xây dựng sơ đồ theo bảng phân công. | Tôi ghi nhận cần đo cùng phạm vi khi so sánh baseline 125 phút cho 100 CV với pilot dự kiến 50–80 CV, đồng thời tính cả thời gian xử lý CV phải đọc tay. |
| Problem Statement (CP5–CP6) | Tôi được phân công hỗ trợ Tuấn Anh ở CP6. Khi đối chiếu v0 và v1, tôi rà lại cách đo tỷ lệ bỏ sót. | V1 bổ sung chỉ số tỷ lệ recruiter phải mở lại CV gốc. Tôi ghi nhận cần làm rõ cách tính baseline khoảng 8% và cách kiểm tra mục tiêu bỏ sót dưới 2%. |
| Mức can thiệp AI (CP6) | Tôi được phân công hỗ trợ Tuấn Anh so sánh No AI, Rule, Workflow và Agent. | Nhóm chọn Workflow. AI trích xuất bằng chứng theo tiêu chí của vị trí, còn recruiter quyết định phân loại hồ sơ. Khi rà báo cáo, tôi ghi nhận bộ tiêu chí đánh giá cần thể hiện trường hợp “Cần con người xem xét thêm”. |
| Quyết định (CP6) | Tôi rà lại quyết định và ngưỡng dừng trong báo cáo nhóm. Khánh phụ trách tổng hợp phần quyết định theo bảng phân công. | Nhóm chọn Go cho pilot hẹp trong hai tuần. Tôi ghi nhận pilot cần theo dõi riêng việc bỏ sót ứng viên đạt chuẩn vì đây là lỗi nhóm đánh giá nghiêm trọng nhất. |
| Tổng kết cá nhân (CP7) | Tôi cập nhật nhật ký tham gia dựa trên bảng pitch, bảng phân công và báo cáo nhóm. | Nhật ký phân biệt câu hỏi tôi đã đặt, phần tôi được giao và những điểm tôi ghi nhận khi rà soát báo cáo. |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Nhờ AI gợi ý chủ đề ở quán ăn, làm nông và bán hàng qua chat, rồi rà lại cách viết Job Story. | Có thêm tình huống để đối chiếu và diễn đạt vấn đề rõ hơn. | Gợi ý ban đầu còn chung, chưa có dữ kiện thực tế cho từng tình huống. | Tôi bổ sung khung giờ cao điểm 19h–22h ở quán ăn và thời gian dò tin nhắn khoảng 3–5 phút. |
| CP2 Problem Card | Nhờ AI phản biện cách mô tả bước nghẽn của báo cáo quảng cáo hằng tuần. | Giúp tách thời gian của bước tổng hợp khỏi thời gian chuẩn bị toàn bộ báo cáo. | Bản nháp ban đầu chỉ nói chung là xem kết quả và tổng hợp, chưa chỉ ra hai nguồn số liệu. | Tôi xác nhận nguồn là bảng doanh thu và các tài khoản quảng cáo. Tôi ghi rõ 1–2 giờ là ước lượng cho toàn bộ báo cáo tuần, còn bước tổng hợp chưa được đo riêng. |
| CP4 Research | Nhờ AI rà bảng research và đối chiếu phần tổng hợp phỏng vấn, khảo sát với các snapshot trong báo cáo nhóm. | Chỉ ra nhận định 3/3 người xác nhận khó khăn khi đọc CV chưa khớp với snapshot của người tham gia với vai trò ứng viên. AI cũng chỉ ra một số link research còn quá chung. | Lần rà soát chỉ dựa trên tài liệu trong repo. Các nguồn bên ngoài và dữ liệu phỏng vấn, khảo sát chưa được xác minh độc lập. | Tôi ghi nhận cần tách phản hồi của ứng viên về form nộp hồ sơ khỏi bằng chứng của người tuyển dụng về khâu đọc CV. |
| CP5 Quy trình | Nhờ AI đối chiếu sơ đồ trước và sau với kế hoạch pilot. | Chỉ ra baseline tính cho 100 CV, còn pilot dự kiến 50–80 CV. | Báo cáo chưa có số đo thực tế về thời gian xử lý CV lỗi định dạng, nên mức tiết kiệm vẫn là kỳ vọng. | Trong nhật ký cá nhân, tôi ghi rõ cần dùng cùng mốc đo và tính cả thời gian đọc tay hồ sơ ngoại lệ. |
| CP5–6 Problem Statement | Nhờ AI rà tính nhất quán của baseline, mục tiêu và cách đo tỷ lệ bỏ sót. | Chỉ ra rằng kiểm tra 20 hồ sơ bị loại có thể giúp phát hiện lỗi nhưng chưa đủ để kết luận tỷ lệ bỏ sót dưới 2%. | Báo cáo chưa cho biết mẫu số và cách xác nhận hồ sơ đạt chuẩn, nên AI không thể kiểm chứng baseline khoảng 8%. | Tôi ghi lại hai câu hỏi cần làm rõ trong nhật ký: tỷ lệ 8% tính trên nhóm hồ sơ nào và ai xác nhận ứng viên đạt tiêu chí. |
| CP6 Mức can thiệp / quyết định | Nhờ AI đối chiếu phương án Workflow, bộ tiêu chí đánh giá và ngưỡng dừng pilot. | Chỉ ra thiết kế có trạng thái “Cần con người xem xét thêm” nhưng schema đánh giá chỉ có Có/Không. | Rà tài liệu chỉ giúp phát hiện điểm chưa nhất quán. Khả năng xử lý CV lỗi hoặc có chỉ thị ẩn cần được kiểm tra bằng ca thử. | Trong nhật ký, tôi ghi hai điểm cần xem lại: cách biểu diễn hồ sơ cần duyệt thêm và ngưỡng theo dõi việc bỏ sót ứng viên đạt chuẩn. |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

### 6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?

Khi nghe Tuấn Anh trình bày về sàng lọc CV, tôi thấy việc tách thời gian theo từng bước giúp cả nhóm dễ phản biện hơn. Card của Tuấn Anh tách riêng thời gian đọc và đối chiếu CV với thời gian xử lý cả đợt. Trong bài báo cáo quảng cáo của tôi, con số 1–2 giờ mới cho biết tổng thời gian chuẩn bị mỗi tuần. Từ đó, tôi thấy mình cần đo riêng bước lấy số liệu và bước tổng hợp để biết nên cải thiện ở đâu.

### 6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?

Khi thảo luận đề tài báo cáo quảng cáo, Tuấn Anh hỏi liệu mẫu Excel có công thức hoặc Looker Studio đã đủ để giảm thời gian chuẩn bị chưa. Câu hỏi đó đưa cuộc thảo luận về quy trình hiện tại: tôi lấy doanh số từ bảng doanh thu, lấy chi phí từ các tài khoản quảng cáo rồi tổng hợp thành báo cáo tuần.

### 6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.

Có. Khi tôi trình bày về việc làm báo cáo quảng cáo hằng tuần, Tuấn Anh hỏi liệu dùng mẫu Excel có công thức hoặc kết nối dữ liệu vào Looker Studio đã đủ để tiết kiệm thời gian chưa. Trước đó, tôi mô tả khâu tổng hợp khá chung và chỉ có con số 1–2 giờ cho cả báo cáo. Sau câu hỏi đó, tôi xem lại quy trình và tách rõ hai việc: lấy doanh số từ bảng doanh thu và chi phí từ các tài khoản quảng cáo, sau đó ghép số liệu thành báo cáo tuần. Tôi vẫn thấy tổng hợp là bước lâu nhất, nhưng chưa đo riêng nên chưa biết một mẫu Excel sẽ giúp được bao nhiêu. Tôi sửa card để ghi rõ phạm vi của con số 1–2 giờ và đưa mẫu báo cáo tuần vào phương án có thể thử. Điều tôi đổi ý là thứ tự làm: tôi sẽ đo từng bước trước khi chọn công cụ.

### 6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?

Khi đọc phần kiểm chứng, tôi bất ngờ vì một recruiter nói rằng dù công cụ báo CV khớp 85%, họ vẫn phải mở hồ sơ gốc nếu công cụ không chỉ ra đoạn nào chứng minh ứng viên có kinh nghiệm cần thiết. Tôi từng nghĩ có điểm phù hợp sẽ giúp recruiter duyệt nhanh hơn. Qua ví dụ này, tôi nhận ra rằng nếu phải đọc lại CV từ đầu để kiểm tra điểm số, recruiter vẫn phải làm lại phần việc tốn thời gian nhất. Điều đó giúp tôi hiểu vì sao nhóm chọn hiển thị đoạn trích kèm số trang để recruiter tự đối chiếu và quyết định. Khi thử nghiệm, tôi muốn theo dõi thêm số lần recruiter phải mở lại và đọc toàn bộ CV, bên cạnh tổng thời gian sàng lọc.

### 6.5. Điều khó nhất khi viết Problem Statement là gì?

Phần khó nhất với tôi là xác định cách đo tỷ lệ bỏ sót ứng viên đạt tiêu chí. Báo cáo dùng baseline khoảng 8% và đặt mục tiêu dưới 2%, nhưng khi đọc lại tôi vẫn muốn biết tỷ lệ đó tính trên nhóm hồ sơ nào và ai xác nhận một hồ sơ đạt chuẩn. Nếu chưa thống nhất cách kiểm tra, nhóm có thể biết quy trình nhanh hơn mà vẫn chưa đánh giá được chất lượng sàng lọc.

### 6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?

Nếu làm lại, tôi sẽ bấm giờ từng bước của báo cáo quảng cáo trước khi pitch. Với đề tài sàng lọc CV, tôi sẽ hỏi sớm hơn: “Trong một đợt tuyển cụ thể, ai kiểm tra lại hồ sơ bị loại và họ dựa vào tiêu chí nào để xác nhận có bỏ sót?” Câu trả lời sẽ giúp nhóm xác định cách đo chất lượng ngay từ đầu và dùng cùng cách đo khi chạy pilot.

### 6.7. Hiểu bài

Nhóm tôi chọn vấn đề nhân viên tuyển dụng mất nhiều thời gian khi phải sàng lọc nhiều CV cho cùng một vị trí. Trong quy trình hiện tại, recruiter tải hồ sơ, đọc và đối chiếu tiêu chí, ghi chú, phân loại rồi gửi shortlist, trong đó bước đọc và đối chiếu là bước nghẽn. Nhóm đặt mục tiêu giảm thời gian xử lý 100 CV từ 125 phút xuống dưới 35 phút và theo dõi tỷ lệ bỏ sót hồ sơ đạt tiêu chí. AI chỉ trích xuất bằng chứng từ CV, còn recruiter quyết định phân loại và đọc tay những hồ sơ lỗi định dạng. Nhóm chọn Workflow vì các bước xử lý có thể định trước và AI chỉ hỗ trợ khâu trích xuất. Quyết định là Go cho pilot hẹp trong hai tuần để đo thời gian và kiểm tra chất lượng trước khi mở rộng.

---

## 7. Tài liệu tham khảo

- [Báo cáo nhóm Nhóm 1A](../team/group_report.md), mục 2–8.
- [Phân công Nhóm 1A](../../TEAM.md), mục Phân công theo checkpoint.
