**CẤU HÌNH HỆ THỐNG THI B1B2 TNUT**

**Bước 1: Cài đặt các phần mềm cần thiết cho hệ thống thi B1B2**
   - Cài đặt IIS trên windows
   - Cài đặt Mariadb, nhớ pw của tài khoản root
   - Download dữ liệu gốc, Khôi phục dữ liệu bằng phần mềm HeidiSQL, sẽ được CSDL trên Mariadb
   - Download và cài đặt PHP7.3.0, cấu hình để chạy được thư viện mysqli
   - Download và cấu hình code Moodle để nhận csdl (root+pw)
   - Cấu hình IIS: để nhận thư mục code Moodle, cấu hình chạy đc index.php, cấu hình php-cgi.exe mudule
   - Đọc và làm theo các bước trong file : Qui trình cài đặt hệ thống thi B1B2 TNUT (easy).pdf
     
**Bước 2: Tạo user là các thí sinh sẽ dự thi**
   - Tạo file ds thí sinh từ ds dự thi gốc (excel)
   - Chuẩn hóa dữ liệu với 4 cột: firstname, lastname, username, password
   - Chú ý: firstname chứa họ và tên đệm, lastname chứa tên, username là dữ liệu số báo danh, password là 4 số ngẫu nhiên
   - Xuất ra file csv (chú ý đảm bảo ko mất tiếng việt)
   - Trộn mail (trên word) để tạo file pdf có các thông tin: SBD, Mật khẩu đăng nhập, MASV, Hoten, ngày sinh, Phòng thi. Khi print file pdf chọn: paper per sheet=4 để tiết kiệm giấy
   - Làm theo các bước trong file : tạo ds thí sinh dự thi
     
**Bước 3: Chuẩn hóa dữ liệu ngân hàng câu hỏi và nhập vào hệ thống**
   - Chuẩn hóa dữ liệu từ ban đề (nhận file word, đã đánh dấu đâu là đáp án đúng: tô vàng, tận cùng là @#)
   - Dùng phần mềm MakeExam v2.8.exe để chuyển đổi cú pháp từ word sang kiểu của moodle hiểu được
   - Lưu vào trong hệ thống moodle => tạo được ngân hàng câu hỏi
   - Các bước làm theo file: Qui trình chuẩn hóa và nhập đề vào hệ thống.pdf
     
**Bước 4: Tạo các ca thi, cấu hình thời gian thi, gán sv sẽ thi vào từng ca thi, setup mạng**
   - Tạo các ca thi theo kế hoạch, đặt thời gian đúng theo lịch, chỉ cho thi 1 lần, khống chế ko cho xem kết quả sau khi làm bài, chỉ cho xem tổng điểm.
   - Gán các sinh viên được phép thi theo đúng ca thi. Làm chậm+kỹ tránh sót, đảm bảo đủ số lượng, đúng sinh viên. vì SBD có thứ tự: lọc theo SBD sẽ rất nhanh
   - Gán ngân hàng đề thi vào ca thi: gán theo bốc thăm ngẫu nhiên của ban đề.
   - Tạo thêm vài user test để kiểm tra xem các cài đặt trước đã ok chưa, clone 1 ca thi, gán user test, cho user này login, thi thử.
   - Cấu hình mạng : cách ly internet, kiểm tra kết nối đảm bảo các máy dự thi ko truy cập được internet, vẫn vào được phần mềm thi qua trình duyệt.
   - Các bước làm theo file: Cấu hình ca thi.pdf
     
**Bước 5: Vận hành hệ thống khi thi**
   - Chạy máy tính đã cài đặt moodle, kết nối LAN, đảm bảo các máy dự thi truy cập được
   - SV làm bài theo khả năng, tích trên máy tính, submit , hệ thống tự ghi nhận kết quả
   - Tại máy đã cài đặt moodle: Login tài khoản admin, vào ca thi, xuất danh sách điểm
   - Sử dụng phần mềm MakeExam v2.8 để ghép danh sách dự thi, 2 file điểm phần Nghe và Đọc -> Print 2 bản đưa sv ký
   - Xuất file excel lưu trữ. Mỗi ca thi thường có 3 phòng thi, cần có 3 file điểm xuất từ phần mềm MakeExam và 2 file excel xuất điểm từ moodle.
   - Cuối buổi: Xuất dữ liệu trong csdl từ phần mềm HeidiSQL thành file .sql để backup.
   - Lưu trữ các file excel đã backup, và file .sql đã backup vào USB hoặc ổ cứng di động => Niêm phong
   - Sao lưu dữ liệu nghe bên thi nói vào máy tính => Copy vào USB hoặc ổ cứng di động => Niêm phong
   - Sao lưu dữ liệu camera các phòng thi vào máy tính => Copy vào USB hoặc ổ cứng di động => Niêm phong


Đỗ Duy Cốp
4/2024
that easy!
