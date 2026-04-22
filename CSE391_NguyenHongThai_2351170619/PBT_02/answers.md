**PHẦN A — KIỂM TRA ĐỌC HIỂU**
**Câu A1 — Input Types**
- Danh sách 10 HTML5 Input Types:
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

**Câu A3 — Accessibility**
1. <label for="email"> quan trọng cho người dùng screen reader vì:
- Kết nối trực tiếp: Nó liên kết văn bản mô tả với ô nhập liệu qua thuộc tính id.
- Thông báo ngữ cảnh: Khi người khiếm thị di chuyển tiêu điểm (focus) vào ô nhập, máy sẽ đọc ngay "Email" để họ biết cần nhập gì. Nếu không có, máy chỉ đọc chung chung là "Edit text", rất dễ gây nhầm lẫn.

2. 
- Khi nào dùng <fieldset> + <legend>: Dùng để nhóm các thẻ input có liên quan mật thiết với nhau về mặt logic.
- Ví dụ: Một nhóm chọn phương thức thanh toán.
<fieldset> bao quanh các nút Radio (Ví mã, Thẻ tín dụng, COD).
<legend> ghi tiêu đề: "Phương thức thanh toán".

3. 
- aria-label dùng khi: giao diện không có chữ hiển thị trên màn hình nhưng vẫn cần mô tả cho máy đọc
- Không nên dùng chung với <label>: Vì gây dư thừa. Khi có cả hai, trình duyệt thường ưu tiên aria-label, có thể làm ghi đè nội dung của thẻ <label> vốn đã được thiết kế chuẩn xác, gây rối cho người dùng screen reader.

**Câu A4 — Media**
1. Thuộc tính loading="lazy"
- Cải thiện: Trì hoãn tải ảnh cho đến khi người dùng cuộn tới. Giúp trang load nhanh hơn và tiết kiệm 4G cho khách.
- KHÔNG dùng khi: Ảnh nằm ở đầu trang (vừa mở web đã thấy). Nếu dùng ở đây sẽ gây cảm giác ảnh bị hiện ra chậm (giật lag).

2. Thẻ <video> & Format
- Tại sao cần nhiều <source> vì để đa dạng khả năng hiển thị. Trình duyệt này không đọc được file này thì nó nhảy sang file khác, đảm bảo khách nào cũng xem được.
- 3 format phổ biến: MP4 (tương thích cao), WebM (nhẹ, chất lượng tốt), Ogg (dự phòng).

3. Thuộc tính alt (Mô tả ảnh)
- Dùng để: Giúp Google hiểu ảnh, hỗ trợ người khiếm thị đọc nội dung và hiện chữ nếu ảnh bị lỗi.

- 3 ví dụ tốt về <alt>:
+ iPhone 16: alt="iPhone 16 màu xanh lưu ly, mặt lưng nhám" (Mô tả chi tiết để bán hàng).
+ Ảnh trang trí: alt="" (Để trống hoàn toàn để trình đọc máy bỏ qua).
+ Biểu đồ Q1/2026: alt="Biểu đồ doanh thu Q1/2026 tăng 15%, đạt mốc 50 tỷ".

**Câu A5 — Media**
So sánh Cách 1 (Dùng <img>) và Cách 2 (Dùng <figure>) khi nào dùng:
Cách 1: 
- Khi ảnh là một phần của nội dung văn bản: Ảnh bổ trợ trực tiếp cho câu văn xung quanh, nếu tách ra thì đoạn văn sẽ mất ý nghĩa.
- Khi không cần chú thích hiển thị: Ảnh chỉ cần mô tả qua thuộc tính alt cho máy đọc, không cần dòng chữ giải thích bên dưới cho người dùng bình thường.
- Ví dụ thực tế: Avatar người dùng, Icon tiện ích.
Cách 2:
- Khi ảnh là một khối nội dung độc lập: Bạn có thể di chuyển khối này đi chỗ khác (sang trang khác hoặc phụ lục) mà không làm hỏng mạch văn của nội dung chính.
- Khi cần chú thích rõ ràng: Cần một dòng tiêu đề hoặc mô tả hiển thị ngay dưới ảnh để người xem hiểu rõ nội dung đó là gì.
- Ví dụ thực tế: Ảnh chi tiết sản phẩm, Sơ đồ/Bản đồ.

**PHẦN C — PHÂN TÍCH & SUY LUẬN**
**Câu C1 — Debug Form**
1. Lỗi 1: Input "Tên" không có <label for="...">
Sửa: <label for="fullname">Tên:</label> <input type="text" id="fullname" name="fullname" required> (Giúp trình đọc màn hình nhận diện và tăng diện tích click).

2. Lỗi 2: Input Email chỉ dùng placeholder mà không có label
Sửa: <label for="email">Email:</label> <input type="email" id="email" name="email" placeholder="Email của bạn" required> (Placeholder biến mất khi nhập chữ, không thể thay thế label).

3. Lỗi 3: Hai ô mật khẩu không có label và không có cơ chế bắt buộc định dạng
Sửa: <label for="pw">Mật khẩu:</label> <input type="password" id="pw" name="password" required> (Tương tự cho ô nhập lại mật khẩu).

4. Lỗi 4: Input "Phone" dùng type="text" thay vì type="tel"
Sửa: <label for="phone">Phone:</label> <input type="tel" id="phone" name="phone" value="0901234567"> (Sử dụng đúng ngữ nghĩa để hỗ trợ bàn phím số trên di động).

5. Lỗi 5: Thẻ <select> thiếu thuộc tính name và label
Sửa: <label for="city">Thành phố:</label> <select name="city" id="city">...</select> (Thiếu name thì dữ liệu sẽ không được gửi lên server khi submit).

6. Lỗi 6: Các thẻ <option> trong Select thiếu thuộc tính value
Sửa: <option value="hanoi">Hà Nội</option> (Nội dung hiển thị là cho người dùng, còn value là giá trị thực tế gửi về Database).

7. Lỗi 7: Thẻ <label> cho "Điều khoản" thiếu Input bên trong hoặc thuộc tính for
Sửa: <input type="checkbox" id="terms" name="terms" required> <label for="terms">Tôi đồng ý điều khoản</label> (Người dùng cần checkbox để tích chọn).

8. Lỗi 8: Toàn bộ các input đều thiếu thuộc tính name
Sửa: Thêm thuộc tính name="..." cho tất cả các thẻ input (Đây là lỗi cực kỳ nghiêm trọng vì nếu không có name, Backend sẽ không nhận được bất kỳ dữ liệu nào từ form này).
**Câu C2 — Thiết kế chiến lược Validation**
1. Viết pattern regex cho CMND/CCCD và Số tài khoản:
- CMND/CCCD (12 chữ số): pattern="\d{12}"
- Số tài khoản (10-15 chữ số): pattern="\d{10,15}"
- Mã PIN (6 chữ số, không hiển thị): Dùng type="password" kèm pattern="\d{6}".

2.  HTML5 validation đủ an toàn cho ứng dụng ngân hàng chưa:
- Trả lời: Chưa đủ an toàn.
- Vì: Vì HTML5 validation diễn ra ở phía Client (trình duyệt). Người dùng có hiểu biết về kỹ thuật có thể dễ dàng dùng F12 (Inspect Element) để xóa bỏ thuộc tính required hoặc pattern, từ đó gửi dữ liệu sai lệch về server.

3. 3 loại validation HTML5 KHÔNG THỂ làm được
- Kiểm tra tính duy nhất (Unique): Ví dụ kiểm tra xem Email/Số tài khoản đã tồn tại trong Database hay chưa.
- So khớp dữ liệu giữa 2 ô (Comparison): Ví dụ kiểm tra "Mật khẩu" và "Nhập lại mật khẩu" có trùng khớp nhau không.
- Validation phụ thuộc (Conditional): Ví dụ nếu chọn phương thức "Chuyển khoản" thì mới bắt buộc nhập "Số tài khoản".

4. 2 rủi ro bảo mật nếu chỉ validate trên Frontend:
- Dữ liệu rác/độc hại tấn công Database: Kẻ xấu có thể dùng công cụ như Postman để gửi dữ liệu trực tiếp vào API, gây lỗi hệ thống hoặc thực hiện tấn công SQL Injection nếu Backend không kiểm tra lại.
- Sai lệch logic nghiệp vụ: Người dùng có thể lách luật để nhập số tiền âm, hoặc số tài khoản không hợp lệ, dẫn đến sai sót trong giao dịch và thất thoát tài sản của ngân hàng.
