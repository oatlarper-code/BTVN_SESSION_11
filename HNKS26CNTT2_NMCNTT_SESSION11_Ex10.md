# 5.Yêu cầu đầu ra
> 1. Phần I. Phân tích và Đề xuất (Đa giải pháp)
- Input: nhóm 8 thành viên soạn thảo, tài liệu 40 trang, có mục lục tự động, phân cấp H1/H2/H3, bảng biểu, và cần được in ra để phát cho ban giám khảo vào ngày hội nghị.
- Output: Sử dụng Word, bảng biểu có thể tùy chỉnh, File in ra không bị lỗi font, vỡ layout khi in A4, 8 người cùng chỉnh sửa, tránh xung đột phiên bản, chuyển đổi định dạng .docx, .pdf để in ấn nộp cho Giảng viên/Ban giám khảo

||Giải pháp A|Giải pháp B|
|-|-|-|
Ưu điểm|Quản lý Section Breaks, Header/Footer, canh lề, ngắt trang và phân cấp Heading cực kỳ chuẩn xác, khi đưa file ".docx" sang máy tính hội nghị, bố cục và font chữ giữ nguyên, hiển thị rõ đoạn văn bản thêm hay bớt, comment phân luồng theo từng dòng,|8 người gõ cùng lúc không giật lag, hiển thị con trỏ của từng người theo màu riêng biệt, không lo xung đột file, chỉ cần trình duyệt web là truy cập được từ mọi máy tính, khôi phục lại bất kỳ thời điểm nào.
Nhược điểm|Cần tài khoản Microsoft 365 và phần mềm Microsoft Word trả phí để dùng bản chính gốc, phiên bản trình duyệt của Word cắt giảm nhiều tính năng định dạng nâng cao (TOC, ngắt trang nâng cao) và đôi khi chậm khi 8 người cùng gõ, nếu dùng Word Desktop đồng bộ qua OneDrive, khi 8 người sửa cùng lúc dễ xảy ra lỗi File Conflict.|Lỗi định dạng khi Export ".docx" khi tải về dạng ".docx" để mở trên MS Word, các bảng biểu, dãn dòng, khoảng cách Heading, và ngắt trang hay bị vỡ layout, kiểm soát in ấn trên Web hạn chế chế độ xem trang của Google Docs đôi khi khác biệt so với trang in thực tế trên driver máy in A4 nội bộ.
> 2. Phần II. So sánh và lựa chọn

||Giải pháp A|Giải pháp B
|-|-|-|
Cộng tác nhóm|⚠️Có thể xung đột nếu chia sẻ một màn hình cho các bạn thành viên khác trong nhóm|✅Ổn định không ảnh hưởng đến thành viên khác
Tính năng văn phòng|✅Chuyên nghiệp hữu dụng|⚠️Không tự động lưu lại có thể bị mất dữ liệu
In ấn và xuất PDF|✅Xuất file ổn định|⚠️Dễ dạng gặp vấn đề khi xuất file
Yêu cầu hạ tầng|❌Phải nộp lệ phí thì mới sử dụng được|✅Miễn phí có thể sử dụng trên trình duyệt
Khả năng nộp cho giảng viên|✅Gửi file|⚠️Trình duyệt yêu cầu mở quyền hoặc tải file bị lỗi font
- Giải pháp bẫy thứ nhất: 8 thành viên cùng làm việc trên Google docs không ai bị ảnh hưởng cả nhóm tận dụng khả năng cộng tác thời gian thực, đặt comment, chỉnh sửa và chốt nội dung thô mà không lo xung đột.
- Giải pháp bẫy thứ hai: Sau khi nội dung được chốt, Trưởng ban Thư ký sẽ tải file về dạng docx mở bằng Microsoft Word. Tiến hành rà soát lại Heading Styles, tạo mục lục tự động, chỉnh lại canh lề khoảng cách bảng biểu. Xuất trực tiếp sang định dạng .pdf trước ngày hội nghị.
- Trưởng Ban Thư Ký chốt dùng Microsoft Word để in file định dạng pdf vì File PDF đảm bảo nguyên vẹn 100% font chữ, căn lề A4, vị trí trang khi chuyển sang máy tính kết nối máy in tại trường, loại bỏ hoàn toàn rủi ro vỡ layout do khác biệt phiên bản Word trên máy in.
> 3. Phần III. Thiết kế và Triển khai 
```
HEADING 1: PHẦN I: TỔNG QUAN HỘI NGHỊ KHOA HỌC 2026
    HEADING 2: 1. Mục đích và Quy mô
          HEADING 3: 1.1. Mục tiêu đào tạo và nghiên cứu
          HEADING 3: 1.2. Dự kiến số lượng đại biểu và bài báo cáo
    HEADING 2: 2. Thời gian và Địa điểm Tổ chức
          HEADING 3: 2.1. Lịch trình chi tiết các phiên toàn thể
          HEADING 3: 2.2. Sơ đồ phân công phòng hội thảo (Khu vực A & B)
HEADING 1: PHẦN II: KẾ HOẠCH TRIỂN KHAI CHI TIẾT
    HEADING 2: 1. Công tác Ban Thư ký & Lễ tân
          HEADING 3: 1.1. Quy trình tiếp đón Ban Giám khảo và Đại biểu
          HEADING 3: 1.2. Mẫu tài liệu, thẻ đeo và Kỷ yếu hội nghị
    HEADING 2: 2. Hậu cần, Kỹ thuật và Trang thiết bị
          HEADING 3: 2.1. Kiểm tra hệ thống âm thanh, máy chiếu tại P.201-A
          HEADING 3: 2.2. Dự phòng sự cố mất điện và kết nối Mạng/Wifi
HEADING 1: PHẦN III: DỰ TRÙ CINH PHÍ VÀ THÙ LAO
    HEADING 2: 1. Chi phí Thù lao Báo cáo viên và Hội đồng
          HEADING 3: 1.1. Định mức thù lao theo quy định
          HEADING 3: 1.2. Danh sách thanh toán chi tiết cho Giảng viên/Tác giả
    EADING 2: 2. Chi phí In ấn và Hậu cần
HEADING 1: PHẦN IV: PHỤ LỤC & DANH SÁCH BÁO CÁO
    HEADING 2: 1. Bảng tổng hợp 80 Báo cáo Khoa học
    HEADING 2: 2. Danh mục Tác giả và Khách mời Trường ngoài
```
