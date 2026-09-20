# 🛰️ Giáo trình Vệ tinh PTIT-STEM-CUBE

Chào mừng bạn đến với khóa học lập trình và vận hành Vệ tinh nhỏ. Khóa học được thiết kế theo hướng thực hành đi từ các vi điều khiển cơ bản đến một hệ thống vệ tinh hoàn chỉnh chạy Hệ điều hành thời gian thực.

Dưới đây là cấu trúc lộ trình học tập dành cho học viên. Mỗi bài Lab đều được sắp xếp trình tự hợp lý: bắt đầu bằng Video giới thiệu, tiếp nối là các tài liệu đọc và thao tác thực hành xen kẽ. Cuối mỗi Lab sẽ có phần tổng hợp kết quả.

---

## Lab 0: Giới thiệu Tổng quan
**🎯 Mục tiêu:** Giới thiệu tổng quan về cấu trúc phần cứng của vệ tinh. Học viên nắm được chức năng cơ bản của từng phân hệ.

- 🎥 **Video 0.1:** Giới thiệu tổng quan về hệ thống vệ tinh và các phân hệ.
- 📖 **Doc 0.1:** Tổng quan về Vệ tinh nhỏ và kiến trúc hệ thống.
- 🎥 **Video 0.2:** Demo tương tác với mô hình vệ tinh 3D trên Web.
- 💻 **Thực hành:** Khám phá và nhấp vào từng phân hệ trên giao diện Web để đọc thông số kỹ thuật.
- 📝 **Tổng hợp Lab 0:** Nắm vững cấu trúc tổng thể và vai trò của từng phân hệ trên vệ tinh.

---

## Lab 1: Máy tính trên bo mạch (OBC)
**🎯 Mục tiêu:** Làm quen với Web IDE, nạp code cho vi điều khiển chính, giao tiếp máy tính và kết nối mạng WiFi/Internet.

- 🎥 **Video 1.1:** Giới thiệu về vi điều khiển và phân hệ Xử lý trung tâm.
- 📖 **Doc 1.1:** Kiến trúc phần cứng vi điều khiển và các chuẩn giao tiếp.
- 🎥 **Video 1.2:** Cách biên dịch và nạp code lần đầu.
- 📖 **Doc 1.2:** Hướng dẫn sử dụng Web IDE tích hợp.
- 💻 **Thực hành:** 
  - `Lab1-01_Blink_LED`: Nhấp nháy đèn LED để kiểm tra bo mạch.
  - `Lab1-02_Serial_Communication`: Gửi và nhận dữ liệu từ máy tính.
  - `Lab1-03_Serial_Control_LED`: Điều khiển LED bằng lệnh gửi từ máy tính.
- 🎥 **Video 1.3:** Giới thiệu về kết nối WiFi và Máy chủ Web.
- 📖 **Doc 1.3:** Lý thuyết về Máy chủ Web và giao thức truyền tải.
- 💻 **Thực hành:**
  - `Lab1-04_WiFi_Connection`: Kết nối vào mạng WiFi có sẵn.
  - `Lab1-05_WiFi_AP_Mode`: Phát WiFi từ vệ tinh.
  - `Lab1-06_Web_Server_LED`: Dựng máy chủ điều khiển LED qua trình duyệt.
- 📝 **Tổng hợp Lab 1:** Hoàn thiện kỹ năng lập trình cơ bản và kết nối mạng cho vi điều khiển chính.

---

## Lab 2: Phân hệ Năng lượng (EPS)
**🎯 Mục tiêu:** Quản lý năng lượng, đọc điện áp pin, và các chế độ tiết kiệm pin trên không gian.

- 🎥 **Video 2.1:** Giới thiệu về Hệ thống Nguồn trên vệ tinh.
- 📖 **Doc 2.1:** Tổng quan hệ thống Nguồn (Pin, Mạch sạc, Chuyển đổi điện áp).
- 🎥 **Video 2.2:** Cách chuyển đổi giá trị điện áp Analog.
- 💻 **Thực hành:** 
  - `Lab2-01a_Battery_GPIO`: Đọc điện áp pin bằng ADC (Analog).
  - `Lab2-01b_Battery_Library`: Tính toán phần trăm pin vệ tinh (Dùng thư viện PTITCube).
- 📖 **Doc 2.2:** Quản lý rủi ro sụt áp và các chế độ ngủ.
- 💻 **Thực hành:** `Lab2-02_Power_Saving` - Kích hoạt chế độ ngủ sâu tiết kiệm năng lượng.
- 📝 **Tổng hợp Lab 2:** Nắm vững cách quản lý, tối ưu và tiết kiệm điện năng cho vệ tinh.

---

## Lab 3: Xử lý Dữ liệu và Lệnh (C&DH)
**🎯 Mục tiêu:** Giao tiếp với thẻ nhớ để ghi nhận dữ liệu.

- 🎥 **Video 3.1:** Giới thiệu về Hệ thống Lưu trữ dữ liệu dự phòng trên vệ tinh.
- 📖 **Doc 3.1:** Giao thức giao tiếp nối tiếp và kiến trúc hệ thống tập tin.
- 🎥 **Video 3.2:** Thao tác đọc/ghi file an toàn, tránh hỏng thẻ nhớ.
- 💻 **Thực hành:** 
  - `Lab3-01a_MicroSD_SPI`: Giao tiếp thẻ nhớ bằng thư viện SD gốc (SPI thô).
  - `Lab3-01b_MicroSD_Library`: Ghi log dữ liệu tự động (Dùng thư viện PTITCube).
  - `Lab3-02_Linux_FS_Commands`: Xây dựng hệ thống lệnh quản lý file qua máy tính.
- 📝 **Tổng hợp Lab 3:** Cấu hình thành công hộp đen lưu trữ dữ liệu liên tục cho vệ tinh.

---

## Lab 4: Phân hệ Cảm biến (Sensor)
**🎯 Mục tiêu:** Tương tác với hệ sinh thái cảm biến để nhận biết môi trường không gian, tư thế vệ tinh và hình ảnh.

- 🎥 **Video 4.1:** Giới thiệu tổng quan về hệ thống Cảm biến và Máy ảnh trên vệ tinh.
- 📖 **Doc 4.1:** Nguyên lý hoạt động và giao tiếp truyền dữ liệu của các cảm biến qua mạng I2C.
- 🎥 **Video 4.2:** Tương tác với cảm biến nhiệt độ và áp suất.
- 💻 **Thực hành:** 
  - `Lab4-01a_Environment_I2C`: Đọc cảm biến BMP280 bằng giao tiếp I2C.
  - `Lab4-01b_Environment_Library`: Tối ưu hóa đọc dữ liệu cảm biến môi trường.
- 🎥 **Video 4.3:** Tương tác với cảm biến gia tốc và đo góc nghiêng.
- 💻 **Thực hành:** 
  - `Lab4-02a_IMU_I2C`: Đọc thanh ghi thô MPU6050/6500 bằng I2C.
  - `Lab4-02b_IMU_Library`: Tính toán góc nghiêng vệ tinh (Attitude).
- 🎥 **Video 4.4:** Tương tác và lấy dữ liệu tọa độ từ module định vị.
- 📖 **Doc 4.2:** Trích xuất và phân tích định dạng dữ liệu thô trả về từ module định vị.
- 💻 **Thực hành:** 
  - `Lab4-03a_GPS_UART`: Đọc dữ liệu chuẩn NMEA thô từ module qua UART.
  - `Lab4-03b_GPS_Library`: Bóc tách tọa độ kinh tuyến, vĩ tuyến tự động.
- 🎥 **Video 4.5:** Tương tác, gửi lệnh chụp ảnh và thu thập hình ảnh từ module Máy ảnh.
- 💻 **Thực hành:** 
  - `Lab4-04a_Camera_UART`: Gửi tập lệnh điều khiển máy ảnh qua UART.
  - `Lab4-04b_Camera_Library`: Chụp ảnh và hiển thị về màn hình.
  - `Lab4-05_Read_All_Sensors`: Tổng hợp đọc tất cả cảm biến.
- 📝 **Tổng hợp Lab 4:** Xây dựng thành công hệ thống thu thập dữ liệu đa cảm biến toàn diện.

---

## Lab 5: Truyền thông & Trạm mặt đất
**🎯 Mục tiêu:** Truyền nhận dữ liệu tầm xa giữa Vệ tinh và Trạm mặt đất bằng sóng vô tuyến.

- 🎥 **Video 5.1:** Giới thiệu về phân hệ Giao tiếp Viễn thông không dây.
- 📖 **Doc 5.1:** Sóng vô tuyến và module truyền phát tín hiệu tầm xa.
- 🎥 **Video 5.2:** Hướng dẫn cấu hình các tham số vật lý của sóng vô tuyến.
- 📖 **Doc 5.2:** Đóng gói bản tin và kiến trúc Trạm mặt đất.
- 💻 **Thực hành:** 
  - `Lab5-01a_Send_Telemetry_UART`: Cấu hình thanh ghi LoRa và phát dữ liệu qua UART.
  - `Lab5-01b_Send_Telemetry_Library`: Đóng gói packet Telemetry hoàn chỉnh.
  - `Lab5-02a_Receive_Command_UART`: Lắng nghe chuỗi dữ liệu thô.
  - `Lab5-02b_Receive_Command_Library`: Giải mã lệnh (Command) từ Trái Đất.
- 🎥 **Video 5.3:** Xây dựng Trạm mặt đất để thu phát tín hiệu.
- 💻 **Thực hành:** `Lab5-03_Ground_Station_Demo`
- 📝 **Tổng hợp Lab 5:** Thiết lập thành công luồng giao tiếp vô tuyến hai chiều giữa vệ tinh và mặt đất.

---

## Lab 6: Phân hệ Cấu trúc (Structure)
**🎯 Mục tiêu:** Lắp ráp khung vệ tinh, chuyển đổi sang lập trình đa nhiệm, sử dụng cơ chế khóa và Bộ định thời bảo vệ vệ tinh không bị treo.

- 🎥 **Video 6.1:** Giới thiệu về cơ khí và cấu trúc bảo vệ vệ tinh.
- 📖 **Doc 6.1:** Khái quát về vật liệu và cấu trúc cơ khí của vệ tinh.
- 🎥 **Video 6.2:** Hướng dẫn lắp ráp khung vệ tinh cơ khí.
- 🎥 **Video 6.3:** Tại sao phần mềm vệ tinh cần Hệ điều hành?
- 📖 **Doc 6.2:** Khái niệm cơ bản về Tác vụ, Độ ưu tiên và Bộ điều phối trong Hệ điều hành Thời gian thực.
- 📖 **Doc 6.3:** Tranh chấp tài nguyên và cơ chế khóa bảo vệ.
- 💻 **Thực hành:** `Lab6-01_Multitasking_Scheduler` - Chạy song song nháy đèn, đọc cảm biến, gửi thông tin.
- 🎥 **Video 6.4:** Thực hành gỡ lỗi treo hệ thống bằng Bộ định thời.
- 📖 **Doc 6.4:** Bộ định thời Watchdog Timer trong hàng không vũ trụ.
- 💻 **Thực hành:** `Lab6-02_Watchdog_And_Event` - Kích hoạt tự động khởi động lại hệ thống khi bị treo.
- 📝 **Tổng hợp Lab 6:** Hoàn thiện bộ khung vật lý và đảm bảo độ tin cậy tuyệt đối cho phần mềm bay.

---

## Lab 7: Tích hợp Hệ thống & Nhiệm vụ
**🎯 Mục tiêu:** Lắp ráp toàn bộ các module đã học để hình thành một phần mềm bay hoàn thiện. Giải quyết các bài toán xung đột phần cứng.

- 🎥 **Video 7.1:** Giới thiệu về bài toán Tích hợp Hệ thống trên vệ tinh.
- 📖 **Doc 7.1:** Kỹ thuật ghép kênh bằng IC phần cứng.
- 💻 **Thực hành:** `Lab7-01_Camera_Multiplexer` - Chuyển mạch luân phiên phần cứng.
- 🎥 **Video 7.2:** Phân tích luồng dữ liệu của Phần mềm bay tổng hợp.
- 📖 **Doc 7.2:** Kiến trúc phân lớp phần mềm Vệ tinh toàn diện.
- 💻 **Thực hành:** 
  - `Lab7-02_Full_Satellite_Program` (Phiên bản vòng lặp tuần tự)
  - `Lab7-03_RTOS_Satellite_System` (Phiên bản chạy hệ điều hành đa nhiệm)
- 📝 **Tổng hợp Lab 7:** Vệ tinh đã tích hợp hoàn chỉnh và sẵn sàng cho chuyến bay thử nghiệm thực tế.

---

## Lab 8: Capstone Mini-Project
**🎯 Mục tiêu:** Áp dụng Tư duy Kỹ thuật Hệ thống để sinh viên tự thiết kế, lên ý tưởng và thực hiện một Sứ mệnh Vệ tinh mang tính sáng tạo.

- 🎥 **Video 8.1:** Giới thiệu về Kỹ thuật Hệ thống trong thiết kế và chế tạo vệ tinh.
- 📖 **Doc 8.1:** Giới thiệu lược đồ ngôn ngữ mô hình hóa trong thiết kế hệ thống.
- 📖 **Doc 8.2:** Gợi ý ý tưởng Đồ án (Vệ tinh khí tượng, Vệ tinh cảnh báo cháy rừng).
- 🎥 **Video 8.2:** Hướng dẫn cách tạo ra Dashboard trực quan hóa dữ liệu vệ tinh.
- 💻 **Thực hành:** `Lab8-01_Custom_Mission` - Khung mã nguồn tiêu chuẩn để tự tùy biến.
- 📝 **Tổng hợp Lab 8:** Hoàn tất đồ án, sinh viên nắm vững quy trình thiết kế và vận hành sứ mệnh vệ tinh độc lập.
