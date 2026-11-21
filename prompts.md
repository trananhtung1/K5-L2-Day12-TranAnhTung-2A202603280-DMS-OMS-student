# Khai báo dùng AI — Trần Anh Tùng · G12

Tôi tự xem và gán nhãn 22 ảnh trên CVAT local. Khi gặp trường hợp khó, tôi hỏi ChatGPT/Codex bằng mã ảnh và mô tả bằng chữ. Tôi dùng phần giải thích để chọn hoặc sửa nhãn trên CVAT. Khi kiểm bài, Codex đọc các bản export XML và chạy script của repo.

| Lượt hỏi trong buổi (gộp các câu nối tiếp cùng việc) | Cách dùng câu trả lời | Căn cứ đối chiếu |
|---|---|---|
| Repo yêu cầu gì, guideline ở đâu, làm bước nào trước và tiếp theo? | Xác định phạm vi 22 ảnh, bằng chứng cần nộp và thứ tự tạo project/task. | README, GUIDE, SUBMISSION |
| Làm ảnh tài xế trước thế nào, camera_blocked nghĩa gì? | Tra quy tắc cho tag toàn ảnh. | GUIDE §4.1–4.3 |
| Làm ảnh S trước, bắt đầu từ IR thế nào, seatbelt nghĩa gì? | Theo dõi thao tác và các giá trị thuộc tính trong CVAT. | GUIDE §4.3, §4.7 |
| Ghế trẻ em, infant_seat và mặt trẻ xử lý ra sao? | Phân biệt các nhãn và xác định khi nào phải hỏi coach. | GUIDE §3, §4.2, §4.8 |
| Bàn tay ngửa/úp có vẽ không, face và face13 dùng cho ai? | Áp dụng đúng phạm vi của nhãn ở OMS và DMS. | GUIDE §4.2, §4.5–4.7 |
| Thứ tự checkpoint và cách xuất ZIP? | Chọn CVAT for images 1.1 và kiểm theo phạm vi. | CHECKPOINTS, ZIP chỉ có annotations.xml |
| Đã làm hết S, nhờ chạy A, giải thích hai lỗi, kiểm lại sau các lần sửa. | Codex chạy script và chỉ ra các khung bị báo. Tôi mở các khung đó trên CVAT để rà lại occupied và light. | check_cpA.txt, XML và các lượt chạy cabin_check |
| Cần biết gì khi gán DMS, nhìn trung tâm khác nhìn ra trước thế nào? | Phân biệt center, cluster, road; tra quy ước điểm mắt và tay. | GUIDE §4.5–4.7 |
| Gán xong, đã chạy script chưa, chạy trước hay sau review; giữ các điểm mắt khuất trên mặt nghiêng. | Codex chạy Checkpoint B và kiểm cuối. Tôi quyết định giữ nhãn ở D03, D05 và mô tả phần mắt bị khuất để Codex ghi vào báo cáo. | check_cpB.txt, check_final.txt và các cờ trong export |
| Có thể review chưa, cần gửi ZIP nào và định dạng nào? | Tra quy trình đổi bản export không kèm ảnh. | CHECKPOINTS, RULES |
| Đã nhận ZIP của đối tác, nhờ phân tích và gợi ý nhận xét. | Codex chạy diff trên hai bản XML, điền nhận xét đề xuất, mục guideline và cách xử lý vào log. Tôi dùng kết quả để tìm và sửa tag còn thiếu ở D06. | Hai bản XML, script diff, disagreement_log.csv |
| Đã sửa D06, chuẩn bị bài nộp. | Sau khi tôi sửa D06, Codex xuất và kiểm bản v2, tổng hợp nhật ký IR từ nhãn và mô tả của tôi, soạn danh sách lớp, tóm tắt các lỗi đã sửa và đóng gói hồ sơ. | SUBMISSION, XML, log trước/sau và kiểm ZIP |
| Chốt exit ticket và kiểm hồ sơ trước khi push GitHub. | Tôi tự chọn và gửi ba đáp án. Codex điền các đáp án đó vào tệp, định dạng số giây đến hai chữ số thập phân và kiểm gói nộp theo SUBMISSION. | exit_ticket.md, danh sách tệp trong ZIP, check_final_v2.txt |
| Rà lại khai báo dùng AI. | Codex chỉnh các câu thiếu chủ ngữ để ghi rõ việc tôi làm trên CVAT và phần hỗ trợ xử lý tệp, soạn báo cáo. | Lịch sử trao đổi và RULES §3 |
