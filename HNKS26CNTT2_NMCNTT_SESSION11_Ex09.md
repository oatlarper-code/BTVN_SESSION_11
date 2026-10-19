# 5.Yêu cầu đầu ra
> 1. Phân tích bài toán(I/O)
- Lookup_value: là giá trị cần dò tìm, có thể điền giá trị trực tiếp hoặc tham chiếu tới một ô trên bảng tính.
- Table_array: là bảng giới hạn để dò tìm.
- Col_index_num: là số thứ tự của cột lấy dữ liệu trong bảng cần dò tìm, tính từ trái qua phải.
- Range_lookup: là tìm kiếm chính xác hay tìm kiếm tương đối với bảng giới hạn, nếu bỏ qua thì mặc định là 1. (Range_lookup được chia làm 2 phần TRUE hoặc FALSE. TRUE đại diện cho số 1 để truy ra kết quả tương đối còn FALSE đại diện cho số 0 để truy ra kết quả chính xác tối ưu nhất từ bảng)

||Lookup_value|Table_array|Col_index_number
|-|-|-|:-:|
Cột D: Tên tác giả|Mã TG ở Cột C2|`$A$2:$E$81`|2
Cột E: Phòng trình bày|Mã TG ở Cột C2|`$A$2:$E$81`|4
Cột F: Thù lao|Mã TG ở Cột C2|`$A$2:$E$81`|5

> 2. Đề xuất giải pháp
- Giải pháp bẫy thứ nhất: Dùng hàm TRIM(`C2`) bọc quanh lookup_value tự động loại bỏ khoảng trắng thừa trước và sau mã của tác giả
- Giải pháp bấy thứ hai: Dùng hàm IFFEROR(`$A$1:$E$81`, `"chưa cập nhật"`) bọc toàn bộ Vlookup khi trả về lỗi #N/A thì sẽ chuyển sang dạng chưa cập nhật
- Giải pháp bẫy thứ ba: Sử dụng dấu "$" cố định hàm để không bị trôi số liệu dồn xuống dưới theo thứ tự ví dụ: =VLookup(`C2,$A$1:$E$81,5,0`)
> 3. Thiết kế thực hiện
- Bước 1. Chọn ô D2 trong bảng DanhMucTacGia
- Bước 2. Viết hàm IFFEROR lồng các hàm VLOOKUP, TRIM nối tiếp vừa loại bỏ khoảng trắng cố định hàm và bẫy lỗi
- Bước 3. Truy xuất kết quả tại ô D2
- Bước 4. Chọn ô D2 và chuyển công thức sang với E2, F2 sau đó sửa lại tham số lần lượt 4, 5
- Bước 5. Bôi đen ô E2:F2 và kéo xuống dòng 81

> Phần II. Triển khai và chống lỗi
- Công thức hoàn chỉnh cho ô D2(Tên tác giả): `=IFFEROR(VLOOKUP(TRIM(C2),$A$2:$E$81,2,0), "Chưa cập nhật")`
- Công thức Phòng trình bày:`=IFFEROR(VLOOKUP(TRIM(C2),$A$2:$E$81,4,0), "Chưa cập nhật")`
- Công thức Thù Lao: `=IFFEROR(VLOOKUP(TRIM(C2),$A$2:$E$81,5,0), "Chưa cập nhật")`
- Vì các mục đều có nội dung cụ thể nên mới phải thay thế phần col_index_num 
- Khi bỏ dấu "$" vùng tra cứu sẽ dịch chuyển tương ứng theo từng dòng mà công thức được sao chép xuống
- Ví dụ: Tại ô D2 công thức (A2:E81) thì khi xuống ô D3 thì công thức sẽ bị dồn xuống theo dòng (A3:E82) bỏ sót thông tin đầu và cứ thế trôi xuống D5 (A5:E85) và sẽ báo lỗi "chưa cập nhật"
