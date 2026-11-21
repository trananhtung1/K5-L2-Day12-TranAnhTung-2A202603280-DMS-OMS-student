# Khai báo dùng AI — Trần Anh Tùng · G12

Công cụ sử dụng trong buổi là ChatGPT/Codex. Nguồn đối chiếu gồm tài liệu trong repo, dữ liệu nhãn XML do CVAT xuất và kết quả của cabin_check. Ảnh cabin được gán trên CVAT local.

| Lượt hỏi trong buổi (gộp các câu nối tiếp cùng việc) | Cách dùng câu trả lời | Căn cứ đối chiếu |
|---|---|---|
| Repo yêu cầu gì, guideline ở đâu, làm bước nào trước và tiếp theo? | Xác định phạm vi 22 ảnh, bằng chứng cần nộp và thứ tự tạo project/task. | README, GUIDE, SUBMISSION |
| Làm ảnh tài xế trước thế nào, camera_blocked nghĩa gì? | Tra quy tắc cho tag toàn ảnh. | GUIDE §4.1–4.3 |
| Làm ảnh S trước, bắt đầu từ IR thế nào, seatbelt nghĩa gì? | Theo dõi thao tác và các giá trị thuộc tính trong CVAT. | GUIDE §4.3, §4.7 |
| Ghế trẻ em, infant_seat và mặt trẻ xử lý ra sao? | Phân biệt các nhãn và xác định khi nào phải hỏi coach. | GUIDE §3, §4.2, §4.8 |
| Bàn tay ngửa/úp có vẽ không, face và face13 dùng cho ai? | Áp dụng đúng phạm vi của nhãn ở OMS và DMS. | GUIDE §4.2, §4.5–4.7 |
| Thứ tự checkpoint và cách xuất ZIP? | Chọn CVAT for images 1.1 và kiểm theo phạm vi. | CHECKPOINTS, ZIP chỉ có annotations.xml |
| Đã làm hết S, nhờ chạy A, giải thích hai lỗi, kiểm lại sau các lần sửa. | Chạy script trên bản lưu và xem lại occupied, light cùng các khung bị báo. | check_cpA.txt, XML và các lượt chạy cabin_check |
| Cần biết gì khi gán DMS, nhìn trung tâm khác nhìn ra trước thế nào? | Phân biệt center, cluster, road; tra quy ước điểm mắt và tay. | GUIDE §4.5–4.7 |
| Gán xong, đã chạy script chưa, chạy trước hay sau review; giữ các điểm mắt khuất trên mặt nghiêng. | Chạy B và kiểm cuối, ghi nguyên quyết định giữ nhãn cho D03, D05. | check_cpB.txt, check_final.txt và các cờ trong export |
| Có thể review chưa, cần gửi ZIP nào và định dạng nào? | Tra quy trình đổi bản export không kèm ảnh. | CHECKPOINTS, RULES |
| Đã nhận ZIP của đối tác, nhờ phân tích và gợi ý nhận xét. | Chạy diff, hỗ trợ soạn nội dung log, tách lỗi cấu trúc D06 khỏi các bất đồng cần xem ảnh. | Hai bản XML, script diff, disagreement_log.csv |
| Đã sửa D06, chuẩn bị bài nộp. | Xuất và kiểm v2; hỗ trợ tổng hợp nhật ký IR từ nhãn, soạn danh sách lớp, tóm tắt lỗi đã sửa và đóng gói. | SUBMISSION, XML, log trước/sau và kiểm ZIP |
| Chốt exit ticket và kiểm hồ sơ trước khi push GitHub. | Điền lại ba đáp án cá nhân đã cung cấp, đối chiếu tệp trong ZIP với SUBMISSION và kiểm lại bản v2. | exit_ticket.md, danh sách tệp trong ZIP, check_final_v2.txt |
