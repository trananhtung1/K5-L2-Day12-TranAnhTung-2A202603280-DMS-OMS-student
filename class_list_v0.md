# Danh sách lớp v0 — Trần Anh Tùng · G12

## Giám sát tài xế (DMS)

| Lớp hoặc thuộc tính | Giá trị trong bài | Để làm gì | Điều kiện quan sát trên IR |
|---|---|---|---|
| Trạng thái từng mắt | open, closed, unknown | Theo dõi thời gian mắt nhắm qua nhiều khung hình để nhận diện dấu hiệu buồn ngủ. | Phải phân biệt được khe mí của từng mắt. |
| Kính đang đeo | none, clear, sun, unknown | Đánh giá mức tin cậy khi đọc vùng mắt. | Độ sáng tròng kính trên NIR có thể gây nhầm loại kính. |
| Vùng nhìn | road, mirror_l/r/c, cluster, center, lap, other | Phân biệt nhìn đường, kiểm tra gương và nhìn xuống đùi hoặc màn hình. | Cần đủ dấu hiệu từ hướng mắt và đầu. |
| Mốc mặt | face13, gồm 13 điểm | Xác định vị trí mắt, mũi và miệng để theo dõi tư thế đầu. | Mặt rộng từ 60 px; đặt cờ cho từng điểm khuất. |
| Tay chạm vô lăng | hand.on_wheel: yes, no, unknown | Xác định bàn tay nào đang tiếp xúc với vô lăng. | Cần nhìn thấy vùng tiếp xúc. |
| Điện thoại | held, mounted, lap | Phân biệt thiết bị đang cầm và thiết bị đặt trên giá hoặc đùi. | Cần nhận ra cạnh, góc hoặc màn hình. |
| Dây an toàn của tài xế | worn_correct, worn_incorrect, not_worn, unknown | Nhận diện trường hợp cần nhắc thắt hoặc chỉnh dây. | Cần theo dõi được đường dây từ vai xuống hông. |

## Giám sát người và vật trong xe (OMS)

| Lớp hoặc thuộc tính | Giá trị trong bài | Để làm gì | Điều kiện quan sát trên IR |
|---|---|---|---|
| Người theo vị trí ghế | person + seat | Xác định ghế sau nào có người cần được kiểm tra trước khi khóa xe. | Dựa vào hình dáng và vị trí trong xe. |
| Mặt hành khách | face | Định vị vùng mặt của người ngồi trên ghế. | Vùng mặt phải nhìn thấy đủ rõ. |
| Ghế trẻ em | child_seat | Phân biệt ghế chuyên dụng với đồ vật đặt trên ghế xe. | Dựa vào khung và hình dạng ghế. |
| Tình trạng ghế trẻ em | occupied: no, yes, unknown (G12, coach xác nhận) | Xác định khi nào có đủ bằng chứng về tình trạng bên trong ghế. | Chỗ dựa và lòng ghế có thể bị che. |
| Nôi em bé và hướng nôi | infant_seat, facing: rear, front | Ghi nhận nôi ở ghế nào và quay về đầu hay đuôi xe để hỗ trợ kiểm tra cách lắp. | Cần xác định được trục của nôi so với xe. |
| Đồ vật theo ghế | object.type: bag, box, cup, other | Ghi nhận hành lý hoặc vật rời còn trên ghế. | Nhận dạng bằng đường nét, vị trí và kích thước tương đối. |
| Dây an toàn người ngồi sau | seatbelt: not_worn, unknown trong bộ S | Xác định vùng dây đủ rõ để đánh giá tình trạng của người ngồi sau. | Dây có thể khó tách khỏi quần áo trên ảnh đơn sắc. |

## Hai câu hỏi cho người viết guideline

1. **D03.** Khi mặt nghiêng và cả bốn điểm mắt phải đều khuất, cần nhìn thấy bao nhiêu phần khe mí mới đủ căn cứ ghi open? Bản đã gán giữ open và đánh outside cho bốn điểm. Người review chọn unknown. Cần một ví dụ chuẩn cho trường hợp này.
2. **S02_ir và S02_rgb.** Với nôi quay chéo trên ghế, bộ phận nào của nôi nên dùng làm chuẩn khi phân biệt facing=rear và facing=front? Bản đã gán rear trên cả hai ảnh, người review ghi front. Cần thống nhất dấu hiệu hình học trước khi thay nhãn.
