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
| 1 | Lặp lại, tốn thời gian, tổng hợp thông tin | Khi chuẩn bị cho buổi họp tối hằng tuần, tôi muốn rút ngắn thời gian tổng hợp kết quả chạy quảng cáo để có đủ thông tin trình bày trong cuộc họp. | Tôi, người chạy quảng cáo và lập báo cáo tuần. | Tôi làm báo cáo mỗi tuần và thấy khâu tổng hợp mất nhiều thời gian. Chưa đo số phút. |
| 2 | Tốn thời gian | Khi kết ca, tôi muốn tìm nhanh khoản chênh giữa tiền nhận và hóa đơn để chốt số tiền của ca. | Người đối soát cuối ca ở quán ăn. | Gợi ý cần xác nhận: thời gian dò chênh lệch trong một ca cụ thể. |
| 3 | Pain từ người khác | Khi nhận order giờ cao điểm, tôi muốn biết món nào đã hết để khách chọn được món còn phục vụ. | Nhân viên phục vụ và khách. | Gợi ý cần xác nhận: số đơn phải đổi và thời gian khách chờ thêm. |
| 4 | Cần tổng hợp thông tin | Khi chuẩn bị chăm sóc một luống, tôi muốn biết lần gần nhất đã tưới hoặc bón phân khi nào để lên lịch lần tiếp theo. | Người chăm sóc luống. | Gợi ý cần xác nhận: một lần phải tìm lại sổ, tin nhắn hoặc hỏi người làm cùng. |
| 5 | Cần tổng hợp thông tin | Khi chuẩn bị đóng một đơn đã thay đổi qua chat, tôi muốn xác nhận mẫu, số lượng và địa chỉ cuối cùng để giao đúng đơn khách đã chốt. | Người chốt đơn hoặc đóng hàng. | Gợi ý cần xác nhận: thời gian dò tin nhắn hoặc một trường hợp đóng nhầm. |

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
| Quy trình hiện tại (3–7 bước) | Nháp: xem kết quả chạy quảng cáo → tổng hợp thông tin thành báo cáo tuần → trình bày trong buổi họp. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Khâu tổng hợp báo cáo. Cần đo riêng thời gian lấy số liệu, đối chiếu và viết nhận xét nếu các thao tác này có trong quy trình thực tế. |
| Impact (nếu không giải thì sao) | Tôi phải dành thời gian tổng hợp trước buổi họp mỗi tuần. |
| Success metric (baseline → target) | Số phút từ lúc bắt đầu xem kết quả đến khi báo cáo sẵn sàng. Đo baseline ở lần làm báo cáo tiếp theo, rồi đặt target và kiểm tra báo cáo vẫn đủ thông tin cho cuộc họp. |
| Phương án không dùng AI | Dùng mẫu báo cáo tuần với danh sách chỉ số và định dạng thống nhất. |
| Giả thuyết về AI (nếu có) | Nếu viết nhận xét là bước nghẽn, có thể thử hỗ trợ soạn nháp từ số liệu đã kiểm tra. |
| Cảm nhận nhanh | Chưa biết. Cần đo bước nghẽn trước khi chọn mức can thiệp. |

Quy trình nháp hiện tại:

```text
Xem kết quả quảng cáo → Tổng hợp báo cáo tuần [bước nghẽn dự kiến] → Trình bày trong buổi họp
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
| Success metric (baseline → target) | Số phút đối soát mỗi ca. Đo baseline trước khi đặt target. |
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
| Bottleneck (bước nào, mất bao nhiêu phút) | Dò tin nhắn để biết mẫu, số lượng và địa chỉ nào còn hiệu lực. Chưa đo thời lượng. |
| Impact (nếu không giải thì sao) | Có thể chậm đóng hàng hoặc đóng sai đơn. |
| Success metric (baseline → target) | Số phút xác nhận mỗi đơn có thay đổi và số đơn đóng nhầm. Đo baseline trước khi đặt target. |
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
| “Tổng hợp” còn quá rộng và chưa có thời lượng từng bước. | Chờ tôi đối chiếu với lần làm báo cáo gần nhất. | Bản nháp đã tách các thao tác cần kiểm tra và ghi cách đo baseline. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý chủ đề ở nhà hàng, làm nông và bán hàng qua chat. | Có thêm tình huống để đối chiếu với trải nghiệm. | Gợi ý chung chưa có bằng chứng cho trường hợp của tôi. | Giữ báo cáo quảng cáo hằng tuần là vấn đề đã xác nhận. |
| CP2 Problem Card | Phản biện cách mô tả bước nghẽn và chỉ số. | Chỉ ra cần đo riêng từng thao tác trong khâu tổng hợp. | Các bước chi tiết vẫn cần kiểm tra với quy trình thực tế. | Xác nhận tần suất báo cáo là hằng tuần. |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
