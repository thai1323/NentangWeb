**Câu A1 — Input Types**
**Danh sách 10 HTML5 Input Types**
1. type="email" → Ô nhập text, tự kiểm tra định dạng @ → Dùng cho form đăng ký tài khoản.

2. type="password" → Ô nhập ẩn ký tự (dấu chấm) → Dùng để nhập mật khẩu thanh toán.

3. type="number" → Ô nhập số có nút tăng/giảm → Dùng để chọn số lượng sản phẩm trong giỏ hàng.

4. type="tel" → Ô nhập text, hiện bàn phím số trên di động → Dùng nhập số điện thoại nhận hàng.

5. type="date" → Hiển thị bảng chọn ngày (calendar) → Dùng chọn ngày sinh nhận quà thành viên.

6. type="range" → Thanh trượt kéo chọn giá trị → Dùng làm bộ lọc (filter) khoảng giá sản phẩm.

7. type="color" → Bảng chọn màu sắc hệ thống → Dùng chọn màu sắc biến thể (áo, giày) trong Admin.

8. type="file" → Nút bấm chọn tệp từ máy tính → Dùng để tải ảnh đánh giá sản phẩm (Review).

9. type="search" → Ô nhập text có nút xóa nhanh "x" → Dùng cho thanh tìm kiếm trên Header.

10. type="checkbox" → Ô tích chọn (vuông) → Dùng để đồng ý với Điều khoản dịch vụ khi đặt hàng.
**Câu A4 — Media**
1. Thuộc tính loading="lazy"
Cải thiện: Trì hoãn tải ảnh cho đến khi người dùng cuộn tới. Giúp trang load nhanh hơn và tiết kiệm 4G cho khách.

KHÔNG dùng khi: Ảnh nằm ở đầu trang (vừa mở web đã thấy). Nếu dùng ở đây sẽ gây cảm giác ảnh bị hiện ra chậm (giật lag).

2. Thẻ <video> & Format
Tại sao nhiều <source>? Để đa dạng khả năng hiển thị. Trình duyệt này không đọc được file này thì nó nhảy sang file khác, đảm bảo khách nào cũng xem được.

3 format phổ biến: MP4 (tương thích cao), WebM (nhẹ, chất lượng tốt), Ogg (dự phòng).

3. Thuộc tính alt (Mô tả ảnh)
Dùng để: Giúp Google hiểu ảnh, hỗ trợ người khiếm thị đọc nội dung và hiện chữ nếu ảnh bị lỗi.

Ví dụ tốt:

iPhone 16: alt="iPhone 16 màu xanh lưu ly, mặt lưng nhám" (Mô tả chi tiết để bán hàng).

Ảnh trang trí: alt="" (Để trống hoàn toàn để trình đọc máy bỏ qua).

Biểu đồ Q1/2026: alt="Biểu đồ doanh thu Q1/2026 tăng 15%, đạt mốc 50 tỷ"