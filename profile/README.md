# 🛰️ Giáo trình Vệ tinh PTIT-STEM-CUBE

Chào mừng bạn đến với khóa học lập trình và vận hành Vệ tinh nhỏ chuẩn CubeSat 1U. Khóa học được thiết kế theo triết lý thực hành kết hợp tư duy Kỹ thuật Hệ thống Không gian (Space Systems Engineering), dẫn dắt học viên đi từ các nguyên lý vi điều khiển cơ bản đến một hệ thống vệ tinh hoàn chỉnh chạy Hệ điều hành thời gian thực trên quỹ đạo.

Dưới đây là cấu trúc lộ trình học tập toàn diện dành cho học viên. Mỗi bài Lab đều được sắp xếp theo trình tự sư phạm chặt chẽ: bắt đầu bằng Video giới thiệu trực quan, tiếp nối là chuỗi tài liệu kỹ thuật chuyên sâu (Docs) và các bài thực hành thực chiến xen kẽ. Cuối mỗi Lab là phần tổng hợp đánh giá kết quả.

---

## Lab 0: Giới thiệu Tổng quan Kỹ thuật Không gian & Vệ tinh CubeSat
**🎯 Mục tiêu:** Giới thiệu lịch sử, triết lý tiêu chuẩn hóa CubeSat 1U, các đặc tính khắc nghiệt của môi trường quỹ đạo LEO và nắm vững kiến trúc 6 phân hệ cốt lõi của vệ tinh.

- 🎥 **Video 0.1:** Giới thiệu tổng quan về kỷ nguyên vệ tinh nhỏ CubeSat và các phân hệ trên không gian.
- 📖 **Doc 0.1:** Lịch sử CubeSat, Tiêu chuẩn Kỹ thuật CalPoly, Ống phóng P-POD & Môi trường Quỹ đạo LEO (Chân không, Chu kỳ nhiệt, Bức xạ, Vận tốc quỹ đạo).
- 📖 **Doc 0.2:** Kiến trúc Hệ thống Vệ tinh 1U & Chi tiết Vai trò 6 Phân hệ Cốt lõi (OBC, EPS, Sensors & Payload, COM, Structure, ADCS).
- 🎥 **Video 0.2:** Demo tương tác với mô hình vệ tinh 3D thời gian thực trên nền WebGL.
- 💻 **Thực hành:** Khám phá, xoay mô hình 3D và nhấp vào từng phân hệ trên giao diện Web LMS để phân tích thông số kỹ thuật chi tiết.
- 📝 **Tổng hợp Lab 0:** Nắm vững cấu trúc tổng thể và mối tương quan phối hợp giữa các phân hệ trên vệ tinh.

---

## Lab 1: Máy tính trên Bo mạch (OBC) & Môi trường Lập trình Nhúng
**🎯 Mục tiêu:** Làm chủ kiến trúc phần cứng vi điều khiển ESP32-WROOM-32, môi trường Web IDE đám mây, nạp code trực tiếp qua Web Serial API, điều khiển ngoại vi và kết nối mạng WiFi/Web Server.

- 🎥 **Video 1.1:** Giới thiệu về vi điều khiển lõi kép và phân hệ Xử lý Trung tâm (OBC).
- 📖 **Doc 1.1:** Kiến trúc phần cứng vi điều khiển ESP32-WROOM-32, Chân Strapping Pins, GPIO, ADC 12-bit, PWM LEDC và IC dịch bit 74HC595.
- 🎥 **Video 1.2:** Hướng dẫn biên dịch mã nguồn trên Cloud và nạp firmware lần đầu.
- 📖 **Doc 1.2:** Hướng dẫn Môi trường Lập trình Web IDE & Giao thức Nạp Firmware Trực tiếp Web Serial API.
- 💻 **Thực hành Ngoại vi Cơ bản:** 
  - `Lab1-01_Blink_LED`: Nhấp nháy đèn LED nhịp tim (Heartbeat) kiểm tra chu trình sống bo mạch.
  - `Lab1-02_Control_Multiple_LEDs`: Điều khiển chuỗi LED tuần tự bằng mảng và vòng lặp.
  - `Lab1-03_Button`: Đọc trạng thái ngõ vào số với điện trở kéo lên nội (`INPUT_PULLUP`).
  - `Lab1-04_LED_Button`: Đảo trạng thái đèn LED theo sự kiện nhấn nút kết hợp thuật toán chống rung tiếp điểm (Debounce).
  - `Lab1-05_7_Segment_LED`: Lập trình dịch 8 bit qua IC 74HC595 hiển thị số đếm trên LED 7 đoạn.
  - `Lab1-06_Serial_Communication`: Giao tiếp cổng nối tiếp UART ở tốc độ baud chuẩn 115200 bps.
  - `Lab1-07_Serial_Control_LED`: Bộ phân tích cú pháp ký tự UART điều khiển bật/tắt thiết bị từ máy tính.
- 📖 **Doc 1.3:** Lý thuyết Mạng Không dây 802.11, Máy chủ Web HTTP Nhúng & Cơ chế Điểm truy cập SoftAP Mode.
- 📖 **Doc 1.4:** Quy chuẩn Lập trình C++ Định thời Non-blocking với hàm `millis()` & Kỹ thuật An toàn Chống Tràn số sau 49.7 Ngày.
- 🎥 **Video 1.3:** Giới thiệu về kết nối WiFi và Máy chủ Web nhúng.
- 💻 **Thực hành Mạng & Máy chủ:**
  - `Lab1-08_WiFi_Connection`: Kết nối ESP32 vào mạng WiFi cục bộ và in địa chỉ IP.
  - `Lab1-09_WiFi_AP_Mode`: Cấu hình vệ tinh tự phát mạng WiFi SoftAP bảo mật WPA2.
  - `Lab1-10_Web_Server_LED`: Dựng máy chủ HTTP nhúng điều khiển thiết bị qua trình duyệt web.
- 📝 **Tổng hợp Lab 1:** Hoàn thiện kỹ năng lập trình nhúng C++ cơ bản và kết nối mạng không dây cho vi điều khiển chính.

---

## Lab 2: Phân hệ Năng lượng (EPS) & Quản lý Nguồn Quỹ đạo
**🎯 Mục tiêu:** Quản lý năng lượng sinh tồn, đặc tính pin Li-Po, mạch sạc CC/CV TP4056, đọc điện áp và dung lượng pin với IC MAX17048 qua I2C, công tắc ngắt an toàn và các chế độ ngủ sâu.

- 🎥 **Video 2.1:** Giới thiệu về Hệ thống Nguồn trên vệ tinh (Pin Li-Po, Mạch sạc CC/CV, IC Fuel Gauge).
- 📖 **Doc 2.1:** Tổng quan Phân hệ Năng lượng EPS, Công nghệ Pin Li-Po 3.7V, IC sạc TP4056, Ổn áp Buck 3.3V / Boost 5.0V & IC Đo Dung Lượng MAX17048 qua I2C.
- 🎥 **Video 2.2:** Giao tiếp I2C đọc các thanh ghi `VCELL` và `SOC` của IC MAX17048.
- 💻 **Thực hành Giám sát Nguồn:** 
  - `Lab2-01a_Battery_I2C`: Đọc trực tiếp thanh ghi điện áp và dung lượng pin MAX17048 qua thư viện `Wire.h`.
  - `Lab2-01b_Battery_Library`: Quản lý phân hệ nguồn EPS thông qua lớp thư viện PTITCube đóng gói cấp cao.
- 📖 **Doc 2.2:** Quản lý Rủi ro Sụt áp (Brownout), Cơ chế Ngắt An toàn Phóng (Chốt RBF, Công tắc Hành trình) & Các Chế độ Tiết kiệm Điện Quỹ đạo (Light Sleep, Deep Sleep với RTC Timer).
- 💻 **Thực hành Tiết kiệm Năng lượng:** `Lab2-02_Power_Saving` - Kích hoạt chế độ Deep Sleep với bộ định thời RTC, quan sát dòng điện suy giảm và chu trình thức dậy an toàn.
- 📝 **Tổng hợp Lab 2:** Nắm vững phương pháp quản lý, tối ưu hóa và sa thải phụ tải bảo vệ nguồn điện cho vệ tinh.

---

## Lab 3: Xử lý Dữ liệu và Lệnh (C&DH) & Hệ thống Lưu trữ Hộp Đen
**🎯 Mục tiêu:** Giao tiếp bus SPI tốc độ cao với thẻ nhớ MicroSD, xây dựng bộ phân tích lệnh Shell CLI, chuyển đổi sang lập trình đa nhiệm FreeRTOS và bảo vệ hệ thống bằng Watchdog Timer.

- 🎥 **Video 3.1:** Giới thiệu về Hệ thống Lưu trữ dữ liệu hộp đen dự phòng trên vệ tinh.
- 📖 **Doc 3.1:** Giao thức Giao tiếp SPI Tốc độ cao (4 dây, 4 Chế độ Mode 0-3) & Kiến trúc Hệ thống Tập tin FAT32 trên Thẻ MicroSD, Tầm quan trọng Cốt tử của hàm `file.flush()`.
- 🎥 **Video 3.2:** Thao tác đọc/ghi file an toàn, cơ chế đệm RAM và phòng ngừa lỗi hỏng thẻ nhớ.
- 💻 **Thực hành Lưu trữ:** 
  - `Lab3-01a_MicroSD_SPI`: Giao tiếp thẻ nhớ bằng thư viện SPI thuần, khởi tạo phần cứng ở tần số cao.
  - `Lab3-01b_MicroSD_Library`: Ghi log dữ liệu viễn trắc tự động định dạng CSV với dấu thời gian.
  - `Lab3-02_Linux_FS_Commands`: Xây dựng hệ thống lệnh dòng lệnh Shell CLI (`ls`, `cat`, `rm`, `df`, `reboot`) qua cổng Serial.
- 🎥 **Video 3.3:** Tại sao phần mềm vệ tinh hiện đại bắt buộc phải dùng Hệ điều hành Thời gian thực (RTOS)?
- 📖 **Doc 3.2:** Khái niệm Tác vụ (Task), Độ ưu tiên (Priority), Ngăn xếp Stack và Bộ điều phối Chiếm trước (Preemptive Scheduler) trong FreeRTOS.
- 📖 **Doc 3.3:** Tranh chấp Tài nguyên Dùng chung, Cơ chế Khóa Bảo vệ (Mutex), Sự cố Nghịch đảo Mức ưu tiên (Priority Inversion - Mars Pathfinder) & Phòng ngừa Deadlock.
- 💻 **Thực hành Đa nhiệm:** `Lab3-03_Multitasking_Scheduler` - Chạy đồng thời 3 tác vụ độc lập được đồng bộ hóa bằng khóa Mutex.
- 🎥 **Video 3.4:** Gỡ lỗi treo hệ thống do bức xạ không gian bằng Bộ định thời Chó canh.
- 📖 **Doc 3.4:** Bộ định thời Giám sát Phần cứng Watchdog Timer (IWDT, TWDT) & Kiến trúc Tự Phục hồi FDIR trong Hàng không Vũ trụ.
- 💻 **Thực hành Chó canh:** `Lab3-04_Watchdog_And_Event` - Kích hoạt Task Watchdog Timer, mô phỏng tình huống tác vụ bị treo và quan sát quá trình tự động reset phục hồi.
- 📝 **Tổng hợp Lab 3:** Thiết lập thành công hộp đen lưu trữ dữ liệu quỹ đạo và xây dựng nền tảng phần mềm đa nhiệm tin cậy cao.

---

## Lab 4: Phân hệ Cảm biến (Sensors) & Tải trọng Quang học
**🎯 Mục tiêu:** Giao tiếp mạng cảm biến đa điểm I2C, trích xuất dữ liệu khí áp BMP280, tính toán tư thế với IMU MPU6500, định vị toàn cầu GNSS L76X và điều khiển Camera OV2640 qua IC Multiplexer 74HC4066.

- 🎥 **Video 4.1:** Giới thiệu tổng quan về hệ thống Cảm biến và Tải trọng quang học trên vệ tinh.
- 📖 **Doc 4.1:** Đi sâu Giao thức I2C Chuẩn Công nghiệp (Open-Drain, Điện trở kéo lên, START/STOP, ACK/NACK, Clock Stretching, Burst Read).
- 🎥 **Video 4.2:** Tương tác với cảm biến khí quyển nhiệt độ và áp suất.
- 💻 **Thực hành Khí áp:** 
  - `Lab4-01a_Environment_I2C`: Đọc mảng hằng số hiệu chuẩn 24 byte và dữ liệu thô từ BMP280 qua I2C.
  - `Lab4-01b_Environment_Library`: Tối ưu hóa tính toán áp suất khí quyển, nhiệt độ và độ cao barometric.
- 🎥 **Video 4.3:** Tương tác với cảm biến quán tính IMU 6 trục và thuật toán ước lượng góc nghiêng.
- 📖 **Doc 4.2:** Cảm biến Khí quyển BMP280, Cảm biến Quán tính IMU MPU6500 & Thuật toán Bộ Lọc Bù (Complementary Filter) Khử Trôi Dạt Gyro.
- 💻 **Thực hành IMU:** 
  - `Lab4-02a_IMU_I2C`: Đọc dữ liệu gia tốc và vận tốc góc thô 14 byte liên tiếp từ MPU6500.
  - `Lab4-02b_IMU_Library`: Cài đặt bộ lọc bù tính toán góc nghiêng vệ tinh (Roll, Pitch) mượt mà.
- 🎥 **Video 4.4:** Tương tác và lấy dữ liệu tọa độ từ module định vị toàn cầu GNSS.
- 📖 **Doc 4.3:** Module Định vị Toàn cầu GNSS L76X (Chuẩn NMEA 0183), Tải trọng Camera OV2640 Xung Nhịp Cao & Kỹ thuật Cách ly Nhiễu EMI bằng IC Chuyển mạch 74HC4066.
- 💻 **Thực hành Định vị & Camera:** 
  - `Lab4-03a_GPS_UART`: Đọc dữ liệu chuỗi NMEA ASCII thô từ module qua cổng UART.
  - `Lab4-03b_GPS_Library`: Tự động trích xuất tọa độ kinh độ, vĩ độ, độ cao và số lượng vệ tinh bám khóa.
  - `Lab4-04a_Camera_UART`: Gửi tập lệnh cấu hình thanh ghi và bắt đầu phiên chụp ảnh từ Camera OV2640.
  - `Lab4-04b_Camera_Library`: Thu nhận khối byte ảnh JPEG nén phần cứng và hiển thị lên màn hình.
  - `Lab4-05_Read_All_Sensors`: Tổng hợp đọc đồng thời tất cả các cảm biến trong một chu trình khép kín.
- 🎥 **Video 4.5:** Giải quyết xung đột phần cứng và nhiễu sóng hài XCLK giữa Camera và GNSS.
- 💻 **Thực hành Multiplexer:** `Lab4-06_Camera_Multiplexer` - Chuyển mạch luân phiên On-Demand giữa Camera và GNSS bằng IC 74HC4066, triệt tiêu nhiễu điện từ.
- 📝 **Tổng hợp Lab 4:** Xây dựng thành công hệ sinh thái thu thập dữ liệu đa cảm biến và tải trọng quang học hoàn chỉnh.

---

## Lab 5: Phân hệ Truyền thông (COM) & Trạm Mặt Đất
**🎯 Mục tiêu:** Nắm vững lý thuyết truyền sóng không gian, tính toán cân bằng tuyến Link Budget, đóng gói khung bản tin viễn trắc với mã CRC-16, truyền nhận dữ liệu tầm xa với LoRa Ebyte E32 và kiến trúc Trạm mặt đất.

- 🎥 **Video 5.1:** Giới thiệu về phân hệ Giao tiếp Viễn thông không gian băng tần UHF.
- 📖 **Doc 5.1:** Cơ sở Lý thuyết Truyền thông Vô tuyến Không gian (Đặc tính Sóng UHF 433MHz, Phương trình Suy hao FSPL của Friis, Cân bằng Tuyến Link Budget & Hiệu ứng Dịch tần Doppler Quỹ đạo LEO).
- 🎥 **Video 5.2:** Cấu hình các tham số vật lý của sóng vô tuyến và kỹ thuật đóng gói bản tin.
- 📖 **Doc 5.2:** Giao thức Đóng gói Bản tin Viễn trắc (Telemetry Framing), Thuật toán Kiểm tra Lỗi Chu kỳ CRC-16-CCITT, Cơ chế Dừng và Chờ Stop-and-Wait ARQ & Tổng quan Chuẩn CCSDS / AX.25.
- 📖 **Doc 5.3:** Module Truyền thông LoRa Ebyte E32 (Băng tần 433MHz, Công nghệ Trải phổ CSS, Chân M0/M1/AUX) & Kiến trúc Trạm Mặt Đất (SDR, Biểu đồ Thác nước Waterfall, Chân đế Xoay Rotator Bám đuổi TLE).
- 💻 **Thực hành Truyền Thông:** 
  - `Lab5-01a_Send_Telemetry_UART`: Cấu hình thanh ghi LoRa E32 và phát luồng dữ liệu byte qua UART.
  - `Lab5-01b_Send_Telemetry_Library`: Đóng gói cấu trúc bản tin Telemetry chuẩn kèm mã tính CRC-16 tự động.
  - `Lab5-02a_Receive_Command_UART`: Lắng nghe chuỗi dữ liệu thô từ cổng không gian và kiểm tra chuỗi đồng bộ Sync Word.
  - `Lab5-02b_Receive_Command_Library`: Giải mã mệnh lệnh điều khiển từ Trái Đất và kích hoạt chân chấp hành.
- 🎥 **Video 5.3:** Xây dựng và vận hành Trạm mặt đất thu phát tín hiệu thực tế.
- 💻 **Thực hành Toàn diện:** `Lab5-03_Satellite_Comm_System` - Thiết lập luồng giao tiếp vô tuyến hai chiều hoàn chỉnh giữa vệ tinh và trạm mặt đất.
- 📝 **Tổng hợp Lab 5:** Hoàn thành liên kết truyền thông viễn trắc và viễn lệnh không gian hai chiều tin cậy cao.

---

## Lab 6: Phân hệ Cấu trúc Cơ khí (Structure) & Tích hợp Vật lý
**🎯 Mục tiêu:** Hiểu rõ vai trò đa chiều của khung cơ khí lên các phân hệ, tiêu chuẩn vật liệu nhôm hàng không Al 6061-T6/7075-T6, xử lý bề mặt Anodize Type III / Alodine, ngăn xếp PC/104, bu lông thông hơi và cân bằng trọng tâm CoM.

- 🎥 **Video 6.1:** Giới thiệu về cơ khí chính xác, tải trọng phóng tên lửa và cấu trúc bảo vệ vệ tinh trong không gian.
- 📖 **Doc 6.1:** Vai Trò Khung Cơ Khí & Tác Động Đa Chiều Lên Các Phân Hệ Khác (Tấm tản nhiệt pin EPS, Lồng Faraday chắn bức xạ OBC, Mặt đất phẳng phản xạ 50 Ohm cho ăng-ten COM, Mặt phẳng tham chiếu cứng vững cho cảm biến).
- 📖 **Doc 6.2:** Vật Liệu Hợp Kim Không Gian (Al 6061-T6, Al 7075-T6), Công nghệ Xử lý Bề mặt Chọn lọc (Anodize Type III chống hàn nguội vs Alodine Class 3 tiếp mass) & Tiêu chuẩn Thoát khí Chân không ASTM E595 (TML < 1%, CVCM < 0.1%).
- 📖 **Doc 6.3:** Tiêu chuẩn Ngăn xếp Bo mạch PC/104, Bu lông Inox A2-70, Keo khóa ren Loctite 222, Bu lông Thông Hơi (Vented Screws) Chống Rò rỉ Ảo TVAC, Bảng Cân Đối Khối Lượng (Mass Budget) & Cân Bằng Trọng Tâm CoM trong Phạm vi $\pm 20\text{ mm}$.
- 🎥 **Video 6.2:** Hướng dẫn quy trình lắp ráp khung cơ khí vệ tinh trong môi trường phòng sạch ISO Class 7/8.
- 💻 **Thực hành Tự Kiểm tra Cơ khí:** Lập trình giải thuật C++ tính toán tọa độ trọng tâm CoM 3 chiều từ bảng khối lượng linh kiện và xác nhận dung sai phóng P-POD.
- 📝 **Tổng hợp Lab 6:** Hoàn thiện bộ khung cơ khí vật lý vững chắc đạt đầy đủ tiêu chuẩn an toàn phóng không gian.

---

## Lab 7: Tích hợp Hệ thống Toàn diện & Vận hành Sứ mệnh Bay
**🎯 Mục tiêu:** Giải quyết 5 thách thức kỹ thuật khi tích hợp đầy đủ các phân hệ vào khối 1U, cài đặt máy trạng thái hữu hạn điều khiển sứ mệnh (Mission FSM), tuân thủ quy trình vận hành bay FOM và mô phỏng chu kỳ quỹ đạo LEO 95 phút.

- 🎥 **Video 7.1:** Giới thiệu về bài toán Tích hợp Hệ thống Toàn diện (System Integration) trên vệ tinh.
- 📖 **Doc 7.1:** Năm Thách Thức Kỹ Thuật Khốc Liệt Khi Tích Hợp Đa Phân Hệ vào Khối 1U (Xung đột Bus I2C/SPI, Nhiễu Tương thích Điện từ EMI/EMC, Sụt áp Đỉnh Tải Brownout, Bẫy nhiệt Chân không, Tính Tất định Thời gian thực & Ngăn ngừa Deadlock).
- 📖 **Doc 7.2:** Kiến Trúc Phân Lớp Phần Mềm Bay (FSW Layered Architecture) & Máy Trạng Thái Hữu Hạn Sứ Mệnh (Mission FSM: `STATE_BOOT` với 30 phút im lặng vô tuyến, `STATE_DETUMBLE` B-dot, `STATE_NORMAL_OPS`, `STATE_PAYLOAD_EXEC`, `STATE_POWER_SAVE`, `STATE_SAFE_MODE`) & Chiến lược FDIR.
- 📖 **Doc 7.3:** Sổ Tay Vận Hành Bay (Flight Operations Manual - FOM), Giao Thức Thông Qua Trạm Mặt Đất (AOS, Data Dump, LOS) & Kỹ Thuật Mô Phỏng Chu Kỳ Quỹ Đạo LEO 95 Phút (60 phút Ban ngày Nắng / 35 phút Vùng tối Eclipse).
- 🎥 **Video 7.2:** Phân tích luồng dữ liệu thời gian thực và kịch bản phối hợp giữa các phân hệ.
- 💻 **Thực hành Tích hợp Hệ thống:** 
  - `Lab7-01_Full_Satellite_Program`: Phiên bản phần mềm bay tích hợp chạy theo vòng lặp tuần tự Non-blocking (Super-Loop) kết hợp `millis()`.
  - `Lab7-02_RTOS_Satellite_System`: Phiên bản phần mềm bay chạy Hệ điều hành Thời gian thực đa nhiệm FreeRTOS phân chia hai lõi CPU, tích hợp mô phỏng chu kỳ quỹ đạo 95 phút.
- 📝 **Tổng hợp Lab 7:** Vệ tinh đã được tích hợp hoàn chỉnh phần cứng và phần mềm, sẵn sàng vận hành bay thử nghiệm trên quỹ đạo giả lập.

---

## Lab 8: Kỹ thuật Hệ thống Sứ mệnh, Dashboard Builder & Đồ án Capstone
**🎯 Mục tiêu:** Áp dụng phương pháp luận Kỹ thuật Hệ thống Không gian (Systems Engineering), vòng đời dự án NASA/ESA (Phases A-F), ma trận kiểm định MECE, thiết kế bảng điều khiển trực quan hóa Dashboard LMS và triển khai 1 trong 3 đề tài đồ án công nghệ không gian thực chiến.

- 🎥 **Video 8.1:** Giới thiệu về Kỹ thuật Hệ thống Không gian (Systems Engineering) và Vòng đời Dự án Hàng không Vũ trụ.
- 📖 **Doc 8.1:** Phương Pháp Luận Kỹ Thuật Hệ Thống Không Gian (Systems Engineering), Vòng Đời Dự Án NASA/ESA theo Pha (Pre-Phase A, Phase A/SRR, Phase B/PDR, Phase C/CDR, Phase D/FRR, Phase E, Phase F) & Ma Trận Kiểm Định Toàn Diện MECE (Test, Analysis, Inspection, Demonstration).
- 📖 **Doc 8.2:** Hướng Dẫn Lựa Chọn & Thiết Kế Khối Trực Quan Hóa (Widgets) trên Dashboard LMS (Radial Gauge, Time-Series Chart, Attitude 3D View, Ground Track Map, Raw Terminal, Uplink Console, Progressive Image Gallery).
- 📖 **Doc 8.3:** Ba Đề Tài Đồ Án Capstone Mini-Project Chuyên Sâu Thực Chiến:
  - *Đề tài 1:* Hệ thống Vệ tinh Viễn thám Giám sát & Cảnh báo Cháy rừng (Wildfire Early Warning Satellite - Geofencing, Xử lý ảnh màu, Nén và Phân mảnh LoRa).
  - *Đề tài 2:* Trạm Vệ tinh LEO Thu thập & Chuyển tiếp Dữ liệu Nông nghiệp Thông minh (Smart Agtech Store-and-Forward Gateway - Polling Beacon, Thuật toán ALOHA, Quản lý thẻ nhớ).
  - *Đề tài 3:* Mạng lưới Vệ tinh Tìm kiếm Cứu nạn Không gian Khẩn cấp (Search and Rescue - SAR Satellite Relay - Bắt tín hiệu phao cứu sinh LoRa SF12, Cờ khẩn cấp, Bản đồ điều phối cứu hộ).
- 🎥 **Video 8.2:** Hướng dẫn sử dụng công cụ kéo thả Dashboard Builder kết nối cổng Web Serial thời gian thực.
- 💻 **Thực hành Đồ án Capstone:** `Lab8-01_Custom_Mission` - Triển khai khung mã nguồn tiêu chuẩn, tùy biến máy trạng thái, tích hợp cảm biến/camera và thiết kế Dashboard hoàn chỉnh cho đề tài lựa chọn.
- 📝 **Tổng hợp Lab 8:** Hoàn tất đồ án Capstone, làm chủ toàn bộ quy trình thiết kế, lập trình và vận hành một sứ mệnh vệ tinh CubeSat độc lập.
