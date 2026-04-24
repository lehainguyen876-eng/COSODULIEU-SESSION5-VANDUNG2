# COSODULIEU-SESSION5-VANDUNG2
## [Vận dụng cơ bản] Vá lỗi "Top Quán Ăn Mới Nổi" trên Trang chủ


### Phân tích lỗi:
- **Lỗi:** Sử dụng `LIMIT` mà không có `ORDER BY`.
- **Nguyên nhân:** Trong SQL, dữ liệu không có thứ tự mặc định bền vững. `LIMIT 5` mà không có `ORDER BY` sẽ khiến DBMS trả về 5 bản ghi bất kỳ, dẫn đến dữ liệu bị hiển thị ngẫu nhiên và không đúng yêu cầu "mới nhất".

### Giải pháp:
Thêm mệnh đề `ORDER BY created_at DESC` để xác định rõ tiêu chí sắp xếp theo thời gian giảm dần trước khi lấy 5 bản ghi đầu tiên.
