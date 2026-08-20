b1: đọc và phân tích yêu cầu sơ khởi của khách hàng ở giai đoạn 1
- hiểu được business contect : ngữ cảnh nghiệp vụ -> xác định vấn đề nghiệp vụ
Doanh nghiệp: Công ty ABC cung cấp dịch vụ đặt xe trực tuyến.

Sản phẩm/dịch vụ hiện tại:

Khách hàng có thể yêu cầu xe thông qua tổng đài hoặc ứng dụng đơn giản.
Doanh nghiệp có 3 nhóm người dùng chính:
Khách hàng
Tài xế
Nhân viên vận hành

Quy trình nghiệp vụ chính của doanh nghiệp:

Khách hàng tạo yêu cầu đặt xe
→ nhập điểm đón, điểm đến, chọn loại xe
→ hệ thống tìm tài xế phù hợp
→ tài xế nhận/từ chối chuyến
→ nếu từ chối thì tìm tài xế khác
→ tài xế thực hiện chuyến và cập nhật trạng thái
→ tính cước
→ thanh toán
→ thông báo kết quả
→ khách hàng đánh giá tài xế.

....
Vấn đề	Biểu hiện	Hệ quả
Phân công tài xế thủ công	Việc tìm và phân công tài xế chủ yếu do con người thực hiện	Chậm xử lý, khó tối ưu việc tìm tài xế
Khách hàng khó theo dõi chuyến	Không biết rõ đang tìm tài xế nào, tài xế nào nhận, thời gian đến	Trải nghiệm khách hàng chưa tốt
Thanh toán chưa tập trung	Thông tin thanh toán chưa được quản lý tập trung	Khó kiểm soát và tra cứu giao dịch
Khó mở rộng hệ thống	Hệ thống hiện tại có hạn chế khi số lượng khách hàng/tài xế tăng	Khó đáp ứng nhu cầu tăng trưởng
Phụ thuộc nhiều vào xử lý thủ công	Nhiều hoạt động cần nhân viên vận hành theo dõi và xử lý	Tăng khối lượng công việc, dễ xảy ra sai sót
Khó xử lý tình huống ngoại lệ	Chưa xác định rõ cách xử lý từ chối chuyến, mất mạng, thanh toán thất bại...	Quy trình chưa thống nhất



b2: đã hiểu ngữ cảnh nghiệp vụ, xác định vấn đề nghiệp vụ 
 xác định stakeholder(những bên liên quan của hệ thống)
- lập bảng 2 cột: tên của stakeholder và vai trò của họ

| stakeholder | Vai trò |
|---|---|
| Khách hàng | Tạo yêu cầu, theo dõi chuyến, thanh toán và đánh giá tài xế |
| Tài xế | Nhận chuyến, cập nhật trạng thái, thông tin phương tiện và vị trí |
| Nhân viên vận hành | Quản lý khách hàng, tài xế, phương tiện, chuyến đi; theo dõi và xử lý các trường hợp phát sinh |
| Ban giám đốc | Đưa ra định hướng, theo dõi hiệu quả hoạt động và sử dụng các báo cáo về chuyến, doanh thu, tỷ lệ hoàn thành/hủy |
| Nhà cung cấp dịch vụ thanh toán | Cung cấp dịch vụ thanh toán điện tử mà hệ thống CAB sẽ tích hợp |
| Nhà cung cấp dịch vụ thông báo | Hỗ trợ gửi thông báo; doanh nghiệp muốn có khả năng thay đổi hoặc thêm nhà cung cấp trong tương lai |
+ ví dụ khách hàng; đặt xe, thanh toán
- vẽ ma trận stakeholder matric: cho biết tầm ảnh hưởng quan trọng của stakeholder trong hệ thống -> sd công cụ mermaid
.....

quadrantChart ****
    title Stakeholder Matrix - CAB System Project
    x-axis "Low Interest" --> "High Interest"
    y-axis "Low Power" --> "High Power"
    quadrant-1 "Keep Satisfied (Quan tâm đặc biệt)"
    quadrant-2 "Manage Closely (Quản lý chặt chẽ)"
    quadrant-3 "Monitor (Theo dõi)"
    quadrant-4 "Keep Informed "
    "Ban Giang Doc / Ban Lanh Dao": [0.88, 0.92]
    "Khach Hang": [0.85, 0.45]
    "Tai Xe": [0.80, 0.40]
    "Nhan Vien Van Hanh": [0.75, 0.50]
    "Doi Ngu Phat Trien (BA, Dev, QA)": [0.70, 0.60]
    "Nha Cung Cap Thanh Toan Ben Ngoai": [0.35, 0.70]
    "Doi Tac Cung Cap Kenh Thong Bao": [0.30, 0.55]
    "Bo Phan Phap Ly & Compliance": [0.25, 0.65]

b3: xác định mục tiêu nghiệp vụ:
liệt kê ra
bg01? giảm thời gian tìm tài xế -> hệ thống phải có khả năng tự động tìm tài xế.
bg02? hỗ trợ thanh toán -mđ: cho phép thanh toán bằng tiền mặt và trực tuyến
bg03?
| STT | Mục tiêu nghiệp vụ | Diễn giải |
| :--- | :--- | :--- |
| BG01 | Giảm thời gian tìm tài xế | Hệ thống phải có khả năng tự động tìm và ưu tiên tài xế gần khách hàng dựa trên vị trí và trạng thái sẵn sàng. |
| BG02 | Hỗ trợ thanh toán | Cho phép thanh toán linh hoạt bằng tiền mặt hoặc phương thức điện tử qua nhà cung cấp bên ngoài. |
| BG03 | Giảm thao tác phân công thủ công | Tự động chuyển tiếp tìm tài xế khác nếu tài xế đầu tiên từ chối/không phản hồi mà khách không cần đặt lại. |
| BG04 | Tăng tính minh bạch chuyến đi | Hệ thống phải hiển thị theo dõi trạng thái realtime, vị trí tài xế, thời gian dự kiến đến và lịch sử chuyến đi cho khách hàng. |
| BG05 | Tối ưu hóa vận hành & quản trị | Cung cấp giao diện quản trị giúp theo dõi chuyến đi, hỗ trợ xử lý sự cố, phân quyền thao tác và xuất báo cáo hiệu quả hoạt động. |
| BG06 | Đảm bảo tính liên tục dịch vụ | Kiến trúc hệ thống phải mở rộng độc lập, đảm bảo lỗi ở thanh toán/thông báo không làm ngưng trệ toàn bộ hệ thống đặt xe. |
| BG07 | Tăng cường an toàn & bảo mật | Xác thực người dùng, bảo vệ dữ liệu cá nhân/vị trí, không lưu thông tin thẻ nhạy cảm và lưu vết các thao tác quan trọng. |
| BG08 | Đảm bảo khả năng mở rộng tương lai | Thiết kế kiến trúc linh hoạt để dễ dàng thêm dịch vụ mới, phương thức thanh toán hoặc kênh thông báo mới. |

b4: xác định phạm vi:
- ví dụ: có quản lí khách hàng, tài xế: 
- liệt kê ra các yêu cầu phải làm, các module 
- phạm vị không phải / không nên làm.
.....

b5: xong bước 4 cần gặp khách hàng xác nhận lại -> oke thì bước qua b5:
chuyển yêu cầu thành business requirement(br)
bảng 3 cột (stt br, tên br, diễn giải)
br01? đặt chuyến xe: hệ thống cho phép khách hàng tạo yêu cầu, cung cấp điểm đến và điểm đi của khách hàng.
br02?
br03?
.....

b6: xây dụng business process:
vd : khách hàng muốn đặt chuyến: tạo chuyến đi - xác nhận điểm đón/ điểm đến - hệ thống xác nhận - tìm tài xế được không? nếu không được phải thông báo cho khách hàng - tìm được tài xế -> tài xế chấp nhận không? không thì phải thông báo cho khách hàng.
.....

b7: phân rã yêu cầu nghiệp vụ (fr) (*)
business requirement(br) -> phân rã ? fr
vd :
br01: tìm tài xế
    fr01: xác định vị trí khách hàng
    fr02: chọn những tài xế có trạng thái online trong khu vực
    fr03: chọn loại xe
    fr04: nếu có yêu cầu yêu tiên cho tài xế rating cao: fr-> ưu tiên cho tài xế có đánh giá cao
    fr05: 

br02: đặt chuyến:
    fr01: 
    fr02:

b8: business rule and acception ( những cái luật để khi xảy ra những trường hợp ngoại lệ là xử lí như nào?)
ví dụ:
chỉ những tài xế nào trong trạng thái sẵn sàng thì mới được nhận chuyến --- 
giả sử khách hàng tạo chuyến - chờ tìm tài xế - thời gian lâu quá -> xử lí sao? ( hủy)
giả sử khách hàng tạo chuyến-- tài xế nhận chuyến nhưng quá thời hạn tài xế không chấp nhận - hủy chuyến - chuyển sang tài xế khác ( nhận chuyến và chấp nhận chuyến khác nhau)

b9: data modeling: xây dụng data model: nhìn vô để xác định những thực thể -> vẽ sơ đồ ERD. (sd công cụ mermaid)

b10: xác định những cái non functional requirement:
vd : hệ thống ở giải đoạn mpv: không quan tâm thời gian phản hồi dưới 1ms
     phải thiết kế theo mirco... ( không cần)
     phải thiết kế theo mirco... ( không cần)

