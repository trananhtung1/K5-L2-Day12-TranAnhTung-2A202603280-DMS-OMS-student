# Tự đánh giá — Trần Anh Tùng · G12

| Ảnh | Đối tượng | Loại | Kết quả rà soát | Đã sửa? |
|---|---|---|---|---|
| S01_rgb | frame_meta.light | wrong_class | Ảnh dựng dùng light=unknown. Lượt kiểm đầu đã cảnh báo về trường này. | Đã đổi thành unknown. |
| S02_rgb | frame_meta.light | wrong_class | Cùng lỗi ánh sáng như S01_rgb. | Đã đổi thành unknown. |
| D03 | Mắt phải và bốn điểm mốc | flag | Mặt quay nghiêng, các điểm mắt phải mang cờ outside. Bản gán giữ eye_right=open, người review chọn unknown. | Giữ nhãn, đã giải thích cảnh báo. |
| D06 | frame_meta | missing | Bản gửi review thiếu tag toàn ảnh. Đối tác có đủ tag. | Đã thêm tag và kiểm lại bản v2. |

## Lỗi lặp lại và cách tránh

Ở lần kiểm phần S, bảy ảnh RGB có light khác unknown. Giá trị này cần theo nguồn ảnh dựng ngay cả khi khung có vẻ sáng. Ở lượt gán tiếp theo, đặt và kiểm ba thuộc tính của frame_meta trước khi vẽ khung đầu tiên. Kiểm ngay sau hai cảnh đầu sẽ giúp phát hiện lỗi trước khi nó lặp lại.

## Điều rút ra từ review

Ở D06, ba dòng khác nhau về modality, light và camera_blocked cùng xuất phát từ một tag bị thiếu trong ZIP gửi review. Đối tác đúng ở mục này. Sau khi sửa, cần kiểm lại chính ZIP sẽ nộp để bảo đảm báo cáo khớp với phiên bản export.
