# 5.Yêu cầu
1. Phần I. Hoàn thiện SRS bằng Heading Styles và Auto TOC
> [SRS_ThuVien.docx](https://docs.google.com/document/d/1MZy-mXWBI--rSP4BSRA-2VFTePwStDL9/edit?usp=sharing&ouid=110879828605207156318&rtpof=true&sd=true)
1. Phần II. Chuẩn hóa dữ liệu và AutoFilter

|MSSV|Họ tên|Mã sách|Ngày mượn|Tình trạng
|-|-|-|-|-|
SV001|Nguyễn Văn An|S001|01/10/2026|Đang mượn
SV002|Trần Thị Bình|S002|03/10/2026|Quá hạn
SV003|Lê Văn Cường|S003|10/10/2026|Đã trả
SV004|Phạm Thu Hà|S099|12/10/2026|Đang mượn
Tổng cộng: 4
- Một Record là toàn bộ thông tin của 1 lượt mượn sách cụ thể: Ví dụ `SV001|Nguyễn Văn An|S001|01/10/2026|Đang mượn`
- Một Field là thuộc tính duy nhất của hệ thống: Ví dụ: cột `Tình Trạng`
> Mô tả thao tác bật AutoFiller 
- Bước 1: Chọn ô thuộc vùng dữ liệu
- Bước 2: Nhấn tổ hợp phím Ctrl+Shift+L các nút mũi tên lọc xuất hiện trong tiêu đề
- Bước 3: Nhấn vào mũi tên
- Bước 4: Bỏ chọn, sau đó tính chọn ô quá hạn
- Kết quả: Màn hình chỉ liệt kê ra ô "Quá hạn" còn các ô còn lại sẽ bị ẩn đi
2. Phần III. Nối dữ liệu
- Công thức VLOOKUP tự động lấy Tên Sách từ sheet DanhMucSach dựa theo cột Mã Sách: Ví dụ: `=VLOOKUP(C2,$A$2:$E$10,2,FALSE)`
- Nguyên nhân: giá trị thứ 4 của hàm VLOOKUP là FALSE trong khi giá trị tìm kiếm S099 hoàn toàn không tồn tại trong cột đầu tiên của mã sách
- Công thức có bọc thêm IFERROR để dòng đó hiển thị "Không tìm thấy sách" thay vì lỗi: Ví dụ: `IFFEROR(VLOOKUP(C2,$A$2:$E$10,2,FALSE),"Không tìm thấy sách")`
> [PhieuMuon_ThuVien.xlsx](https://docs.google.com/spreadsheets/d/1amgMrUFsYlEVlDOPJIZDItqvwMkJZVdS/edit?usp=sharing&ouid=110879828605207156318&rtpof=true&sd=true)
3. Phần IV. Slide báo cáo tiến độ
- Thiết kế nội dung gồm 3 phần:
- Assertion Title: Hệ thống ghi nhận 50% phiếu mượn đang hoạt động, phát hiện 25% quá hạn và 1 mã sách lỗi dữ liệu
- Content Area: Nhấn mạnh chỉ số 25% quá hạn cần can thiệp xử lý.
- Biểu đồ Bar chart Highlight: Trực quan hóa tỷ lệ các trạng thái phiếu mượn, trong đó riêng trạng thái Quá hạn được sơn màu Đỏ nổi bật trên nền xám trung tính.
- Áp dụng Rule 10/20/30: 10 phút làm slide, 20 phút trình bày, cỡ chữ tiêu đề tối thiểu 32-40pt, font nội dung chính 18pt-30pt giúp người đọc dễ dàng quan sát từ xa
> [SlideBaoCao.pptx](https://docs.google.com/presentation/d/15FyWGP59VRQ_jDglt15IIjspVFpHIZ-K/edit?usp=sharing&ouid=110879828605207156318&rtpof=true&sd=true)

