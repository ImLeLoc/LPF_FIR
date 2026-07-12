# LPF_FIR
Đồ án môn học 1.
Thiết kệ bộ lọc thông thấp đáp ứng xung hữu hạn với tần số cắt 150Hz cho mục đích lọc nhiễu cho tín hiệu điện tim ECG.

%% QUY TRÌNH THỰC HIỆN!!!
Phần 1: Mở thư mục Pre-Process và tiến hành tải về sau đó chạy file Python tên WFDB_toolbox_FOR_ECG.py để chạy các mẫu data 16 bit được lưu từ thư viện data của datasheet PTB-XL về. Sau khi đã chạy xong thì sẽ có 1 file txt là file tín hiệu đó nhưng đo ở kênh V4 ở dạng số bù 2 với kiểu dấu chấm tĩnh Q4.12, sau đó lại chạy tiếp file tao_nhieu.py để có được 1 data đã được cộng nhiễu ban đầu. Các code Python này là thuộc thư viện toolbox WFDB của Physionet tạo ra nhằm truy xuất dữ liệu của datasheet.
Phần 2: COde Verilog, ở đây có 2 thư mục là Soucre và Testbench, tiến hành import vào Vivado như thường và chạy toptest để có thể chạy ở Module cao nhất và TB_toptest là testcase cao nhất.
Phần 3: Code Matlab và dùng Simulink để so sánh 2 loại mô phỏng, mở file "kiemtra_sum_test.m" trong thư mục Matlab, tiến hành chạy lần đầu để nạp giá trị vào Simulink qua khối From.workspace và chạy "mophong_1.mat" là workspace có chứa sẵn 21 hệ số của bộ lọc cho khối LPF_Block trong Simulink. tiến hành mở thư mục Simulink và chạy "final_2.slx" để mở mô phỏng, tiến hành chay và sau đó quay về "kiemtra_sum_test.m" để kiểm tra và so sánh 2 dạng mô phỏng.
Phần thư mục Matlab đã bao gồm FilterDesigner được cấu hình sẵn tên là Heso_final.fda
