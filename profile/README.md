# 🛰️ Giáo trình Vệ tinh PTIT-STEM-CUBE

Chào mừng bạn đến với khóa học lập trình và vận hành Vệ tinh nhỏ chuẩn CubeSat 1U. Khóa học được thiết kế theo triết lý thực hành kết hợp tư duy Kỹ thuật Hệ thống Không gian (Space Systems Engineering), dẫn dắt học viên đi từ các nguyên lý vi điều khiển cơ bản đến một hệ thống vệ tinh hoàn chỉnh chạy Hệ điều hành thời gian thực trên quỹ đạo.

**Cấu trúc bài học chuẩn mực:** Trước khi thực hành với bất kỳ linh kiện (Component) nào, giáo trình luôn cung cấp tài liệu kỹ thuật (Doc) chuyên sâu trình bày rõ **Nguyên lý hoạt động phần cứng** và **Phương pháp lập trình** cho Component đó, tiếp nối bằng bài thực hành thực chiến và tổng kết kết quả.

---

## Lab 0: Giới thiệu Tổng quan Kỹ thuật Không gian & Vệ tinh CubeSat
**🎯 Mục tiêu:** Nắm vững lịch sử, tiêu chuẩn kích thước CubeSat 1U, ống phóng P-POD, môi trường vật lý quỹ đạo LEO và nguyên lý 6 phân hệ cốt lõi.

- 🎥 **Video 0.1:** Giới thiệu tổng quan về kỷ nguyên vệ tinh nhỏ CubeSat và các phân hệ trên không gian.
- 📖 **Doc 0.1:** Lịch sử CubeSat, Tiêu chuẩn Kỹ thuật CalPoly, Ống phóng P-POD & Môi trường Quỹ đạo LEO (Chân không, Chu kỳ nhiệt, Bức xạ, Vận tốc quỹ đạo).
- 📖 **Doc 0.2:** Kiến trúc Hệ thống Vệ tinh 1U & Chi tiết Vai trò 6 Phân hệ Cốt lõi (OBC, EPS, Sensors & Payload, COM, Structure, ADCS).
- 🎥 **Video 0.2:** Demo tương tác với mô hình vệ tinh 3D thời gian thực trên nền WebGL.
- 💻 **Thực hành:** Khám phá, xoay mô hình 3D và nhấp vào từng phân hệ trên giao diện Web LMS để phân tích thông số kỹ thuật chi tiết.
- 📝 **Tổng hợp Lab 0:** Nắm vững cấu trúc tổng thể và mối tương quan phối hợp giữa các phân hệ trên vệ tinh.

---

## Lab 1: Máy tính trên Bo mạch (OBC) & Môi trường Lập trình Nhúng
**🎯 Mục tiêu:** Làm chủ vi điều khiển ESP32-WROOM-32, môi trường Web IDE đám mây, nạp firmware qua Web Serial API, làm chủ nguyên lý và lập trình từng linh kiện ngoại vi cơ bản (LED, Nút nhấn, LED 7 đoạn 74HC595, UART, WiFi/Web Server).

- 🎥 **Video 1.1:** Giới thiệu về vi điều khiển lõi kép và phân hệ Xử lý Trung tâm (OBC).
- 📖 **Doc 1.1:** Kiến trúc Phần cứng Vi điều khiển ESP32-WROOM-32, Chân Strapping Pins an toàn và Bộ nhớ SRAM/Flash.
- 🎥 **Video 1.2:** Hướng dẫn biên dịch mã nguồn trên Cloud và nạp firmware lần đầu.
- 📖 **Doc 1.2:** Hướng dẫn Môi trường Lập trình Web IDE & Giao thức Nạp Firmware Trực tiếp Web Serial API.

### Component 1: Đèn LED Chỉ Thị & Điều Chế Xung LEDC PWM
- 📖 **Doc 1.3:** Nguyên lý Phần cứng & Kỹ thuật Lập trình Điều khiển LED Đơn, Chuỗi LED và Điều chế Xung LEDC PWM (Cấu hình ngõ ra Push-Pull, điện trở hạn dòng, tỷ lệ Duty Cycle).
- 💻 **Thực hành Component LED:**
  - `Lab1-01_Blink_LED`: Nhấp nháy đèn LED nhịp tim (Heartbeat) kiểm tra chu trình sống bo mạch.
  - `Lab1-02_Control_Multiple_LEDs`: Điều khiển chuỗi LED tuần tự bằng mảng và vòng lặp.

### Component 2: Nút Nhấn Cơ Khí (Digital Input)
- 📖 **Doc 1.4:** Nguyên lý Hoạt động & Kỹ thuật Lập trình Nút Nhấn Cơ học (Điện trở kéo lên nội `INPUT_PULLUP` và giải thuật chống rung tiếp điểm Debounce bằng phần mềm).
- 💻 **Thực hành Component Nút Nhấn:**
  - `Lab1-03_Button`: Đọc trạng thái mức logic của nút nhấn cơ bản.
  - `Lab1-04_LED_Button`: Đảo trạng thái đèn LED theo sự kiện nhấn nút kết hợp thuật toán chống rung.

### Component 3: LED 7 Đoạn & IC Dịch Bit Chốt Dữ Liệu 74HC595
- 📖 **Doc 1.5:** Nguyên lý Vi mạch Dịch Bit Chốt Dữ liệu 74HC595 & Kỹ thuật Lập trình Điều khiển Màn hình LED 7 Đoạn (3 đường tín hiệu DS, SH_CP, ST_CP và hàm dịch bit `shiftOut`).
- 💻 **Thực hành Component 74HC595 & LED 7 Đoạn:**
  - `Lab1-05_7_Segment_LED`: Lập trình dịch 8 bit qua IC 74HC595 hiển thị số đếm từ 0 đến 9 trên LED 7 đoạn.

### Component 4: Cổng Giao Tiếp Nối Tiếp UART (Serial Monitor)
- 📖 **Doc 1.6:** Nguyên lý Giao tiếp Nối tiếp Bất đồng bộ UART & Kỹ thuật Lập trình Truyền Nhận Ký tự Hai chiều với Máy tính qua Cổng Serial ở tốc độ 115200 bps.
- 💻 **Thực hành Component UART:**
  - `Lab1-06_Serial_Communication`: Giao tiếp cổng nối tiếp UART định dạng chuẩn.
  - `Lab1-07_Serial_Control_LED`: Xây dựng bộ phân tích cú pháp ký tự UART điều khiển bật/tắt thiết bị từ máy tính.

### Component 5: Kết Nối Mạng WiFi & Máy Chủ Web HTTP Nhúng
- 📖 **Doc 1.7:** Nguyên lý Mạng Không dây 802.11 (Chế độ Trạm STA vs Điểm truy cập SoftAP) & Kỹ thuật Lập trình Máy chủ Web HTTP Nhúng Xử lý Yêu cầu GET/POST.
- 📖 **Doc 1.8:** Quy chuẩn Lập trình C++ Định thời Non-blocking với hàm `millis()` & Kỹ thuật An toàn Chống Tràn số sau 49.7 Ngày.
- 🎥 **Video 1.3:** Giới thiệu về kết nối WiFi và Máy chủ Web nhúng.
- 💻 **Thực hành Component WiFi & Web Server:**
  - `Lab1-08_WiFi_Connection`: Kết nối ESP32 vào mạng WiFi cục bộ và in địa chỉ IP.
  - `Lab1-09_WiFi_AP_Mode`: Cấu hình vệ tinh tự phát mạng WiFi SoftAP bảo mật WPA2.
  - `Lab1-10_Web_Server_LED`: Dựng máy chủ HTTP nhúng điều khiển thiết bị qua giao diện trình duyệt web.
- 📝 **Tổng hợp Lab 1:** Hoàn thiện kỹ năng lập trình nhúng C++ cơ bản và điều khiển toàn diện các linh kiện ngoại vi của bo mạch OBC.

---

## Lab 2: Phân hệ Năng lượng (EPS) & Quản lý Nguồn Quỹ đạo
**🎯 Mục tiêu:** Nắm vững nguyên lý pin Li-Po, mạch sạc CC/CV TP4056, lập trình đọc điện áp và dung lượng pin với IC MAX17048 qua I2C, công tắc ngắt an toàn và lập trình chế độ ngủ sâu.

- 🎥 **Video 2.1:** Giới thiệu về Hệ thống Nguồn trên vệ tinh (Pin Li-Po, Mạch sạc CC/CV, IC Fuel Gauge).

### Component 1: Pin Li-Po, Mạch Sạc TP4056 & IC Giám Sát Năng Lượng MAX17048
- 📖 **Doc 2.1:** Nguyên lý Pin Li-Po 3.7V, Thuật toán Sạc CC/CV của IC TP4056, Mạch Ổn áp Buck 3.3V / Boost 5.0V & Kỹ thuật Lập trình Đọc Thanh ghi `VCELL` (Điện áp) và `SOC` (Dung lượng %) của IC MAX17048 qua Bus I2C.
- 🎥 **Video 2.2:** Giao tiếp I2C đọc các thanh ghi của IC MAX17048.
- 💻 **Thực hành Component Nguồn & MAX17048:** 
  - `Lab2-01a_Battery_I2C`: Đọc trực tiếp thanh ghi điện áp và dung lượng pin MAX17048 qua thư viện `Wire.h`.
  - `Lab2-01b_Battery_Library`: Quản lý phân hệ nguồn EPS thông qua lớp thư viện PTITCube đóng gói cấp cao.

### Component 2: Công Tắc An Toàn & Bộ Định Thời RTC Tiết Kiệm Năng Lượng (Deep Sleep)
- 📖 **Doc 2.2:** Nguyên lý Ngắt An toàn Phóng (Chốt RBF, Công tắc Hành trình chân ray), Mạch Giám sát Sụt áp Brownout & Kỹ thuật Lập trình Chế độ Ngủ Sâu (Deep Sleep) Tiết kiệm Điện Năng với Bộ định thời RTC Timer.
- 💻 **Thực hành Component Tiết Kiệm Điện:** `Lab2-02_Power_Saving` - Kích hoạt chế độ Deep Sleep với bộ định thời RTC, đo đạc dòng điện suy giảm và quan sát chu trình thức dậy an toàn.
- 📝 **Tổng hợp Lab 2:** Nắm vững phương pháp quản lý, tối ưu hóa và bảo vệ nguồn điện cho vệ tinh.

---

## Lab 3: Xử lý Dữ liệu và Lệnh (C&DH) & Hệ thống Lưu trữ Hộp Đen
**🎯 Mục tiêu:** Nắm vững nguyên lý và lập trình giao tiếp SPI với thẻ MicroSD, xây dựng bộ phân tích lệnh Shell CLI, lập trình đa nhiệm FreeRTOS với khóa Mutex và bộ định thời Watchdog Timer.

- 🎥 **Video 3.1:** Giới thiệu về Hệ thống Lưu trữ dữ liệu hộp đen dự phòng trên vệ tinh.

### Component 1: Thẻ Nhớ MicroSD & Bus SPI Tốc Độ Cao
- 📖 **Doc 3.1:** Nguyên lý Giao tiếp Bus SPI Tốc độ cao (4 dây, Mode 0-3 CPOL/CPHA) & Kỹ thuật Lập trình Đọc/Ghi Thẻ Nhớ MicroSD với Hệ thống Tập tin FAT32, Cơ chế Đệm RAM và Vai trò Bắt buộc của hàm `file.flush()`.
- 🎥 **Video 3.2:** Thao tác đọc/ghi file an toàn, tránh lỗi phân mảnh và hỏng thẻ nhớ.
- 💻 **Thực hành Component Thẻ Nhớ MicroSD:** 
  - `Lab3-01a_MicroSD_SPI`: Giao tiếp thẻ nhớ bằng thư viện SPI thuần, khởi tạo phần cứng ở tần số cao.
  - `Lab3-01b_MicroSD_Library`: Ghi log dữ liệu viễn trắc tự động định dạng CSV với dấu thời gian.

### Component 2: Bộ Phân Tích Lệnh Dòng Lệnh Shell CLI
- 📖 **Doc 3.2:** Nguyên lý Phân tích Cú pháp Ký tự Nối tiếp & Kỹ thuật Lập trình Hệ thống Lệnh Dòng lệnh Shell CLI (`ls`, `cat`, `rm`, `df`, `reboot`) Quản lý Dữ liệu Vệ tinh qua Cổng Serial.
- 💻 **Thực hành Component Shell CLI:** `Lab3-02_Linux_FS_Commands` - Xây dựng và thực thi hệ thống lệnh quản lý tệp trên thẻ nhớ qua máy tính.

### Component 3: Hệ Điều Hành Thời Gian Thực FreeRTOS & Khóa Mutex
- 🎥 **Video 3.3:** Tại sao phần mềm vệ tinh hiện đại bắt buộc phải dùng Hệ điều hành Thời gian thực (RTOS)?
- 📖 **Doc 3.3:** Nguyên lý Đa nhiệm FreeRTOS (Tác vụ Task, Mức ưu tiên Priority, Ngăn xếp Stack, Bộ điều phối Preemptive Scheduler), Hiện tượng Tranh chấp Tài nguyên Dùng chung, Sự cố Nghịch đảo Ưu tiên (Priority Inversion - Mars Pathfinder) & Kỹ thuật Lập trình Đồng bộ hóa bằng Khóa Mutex.
- 💻 **Thực hành Component FreeRTOS Multitasking:** `Lab3-03_Multitasking_Scheduler` - Chạy đồng thời 3 tác vụ độc lập được đồng bộ hóa an toàn bằng khóa Mutex.

### Component 4: Bộ Định Thời Giám Sát Phần Cứng Watchdog Timer (WDT)
- 🎥 **Video 3.4:** Gỡ lỗi treo hệ thống do bức xạ không gian bằng Bộ định thời Chó canh.
- 📖 **Doc 3.4:** Nguyên lý Mạch Đếm Giám sát Phần cứng WDT, Phân cấp Chó canh (IWDT, TWDT) & Kỹ thuật Lập trình Task Watchdog Timer (TWDT) Tự động Phục hồi Lỗi Treo Vi điều khiển.
- 💻 **Thực hành Component Watchdog:** `Lab3-04_Watchdog_And_Event` - Kích hoạt Task Watchdog Timer, mô phỏng tình huống tác vụ bị treo và quan sát quá trình tự động reset phục hồi.
- 📝 **Tổng hợp Lab 3:** Thiết lập thành công hộp đen lưu trữ dữ liệu quỹ đạo và xây dựng nền tảng phần mềm đa nhiệm tin cậy cao.

---

## Lab 4: Phân hệ Cảm biến (Sensors) & Tải trọng Quang học
**🎯 Mục tiêu:** Nắm vững nguyên lý và lập trình từng cảm biến cụ thể: cảm biến khí quyển BMP280, cảm biến quán tính IMU MPU6500, module định vị GNSS L76X, tải trọng Camera OV2640 và IC chuyển mạch 74HC4066.

- 🎥 **Video 4.1:** Giới thiệu tổng quan về hệ thống Cảm biến và Tải trọng quang học trên vệ tinh.

### Component 1: Mạng Giao Tiếp I2C & Cảm Biến Khí Quyển BMP280
- 📖 **Doc 4.1:** Nguyên lý Bus I2C Chuẩn Công nghiệp (Open-Drain, Điện trở kéo lên, START/STOP, ACK/NACK, Clock Stretching, Burst Read) & Nguyên lý, Kỹ thuật Lập trình Cảm biến Khí quyển BMP280 (Đọc mảng hằng số hiệu chuẩn 24 byte, đo Áp suất, Nhiệt độ và Tính toán Độ cao Khí áp).
- 🎥 **Video 4.2:** Tương tác với cảm biến khí quyển nhiệt độ và áp suất.
- 💻 **Thực hành Component BMP280:** 
  - `Lab4-01a_Environment_I2C`: Đọc mảng hằng số hiệu chuẩn 24 byte và dữ liệu thô từ BMP280 qua I2C.
  - `Lab4-01b_Environment_Library`: Tối ưu hóa tính toán áp suất khí quyển, nhiệt độ và độ cao barometric.

### Component 2: Cảm Biến Quán Tính 6 Trục IMU MPU6500
- 🎥 **Video 4.3:** Tương tác với cảm biến quán tính IMU 6 trục và thuật toán ước lượng góc nghiêng.
- 📖 **Doc 4.2:** Nguyên lý Cảm biến Quán tính MEMS 6 Trục MPU6500 (Gia tốc kế 3 trục, Con quay hồi chuyển 3 trục) & Kỹ thuật Lập trình Bộ Lọc Bù (Complementary Filter) Khử Trôi Dạt Gyro Tính toán Góc Nghiêng Roll, Pitch.
- 💻 **Thực hành Component IMU MPU6500:** 
  - `Lab4-02a_IMU_I2C`: Đọc dữ liệu gia tốc và vận tốc góc thô 14 byte liên tiếp từ MPU6500.
  - `Lab4-02b_IMU_Library`: Cài đặt bộ lọc bù tính toán góc nghiêng vệ tinh (Roll, Pitch) mượt mà.

### Component 3: Module Định Vị Toàn Cầu GNSS (GPS)
- 🎥 **Video 4.4:** Tương tác và lấy dữ liệu tọa độ từ module định vị toàn cầu GNSS.
- 📖 **Doc 4.3:** Nguyên lý Phần Cứng Module Định Vị GNSS L76X & Giao Tiếp UART Nhận Luồng Dữ Liệu NMEA Thô (Ăng-ten gốm, cơ chế Cold/Hot start, tốc độ baud 9600 bps trên UART2).
- 💻 **Thực hành Nhóm 1 (Đọc giá trị thô NMEA):** 
  - `Lab4-03a_GPS_Raw_UART`: Khởi tạo cổng UART kết nối module GNSS, đọc luồng byte thô và in trực tiếp các dòng câu tin NMEA thô (`$GPRMC`, `$GPGGA`) chưa qua xử lý lên màn hình Serial.
- 📖 **Doc 4.4:** Phân Tích Chuyên Sâu Chuẩn Giao Thức NMEA 0183 & Kỹ Thuật Chuyển Đổi Dữ Liệu Thô Thành Các Trường Có Ý Nghĩa (Cấu trúc chi tiết từng trường của `$GPRMC`/`$GPGGA`, công thức đổi tọa độ Độ-Phút sang Độ Thập Phân Decimal Degrees, kiểm tra Checksum XOR, chỉ số phẩm chất HDOP và kiến trúc bộ giải mã Parser).
- 💻 **Thực hành Nhóm 2 (Chuyển đổi NMEA thành các trường giá trị có ý nghĩa):** 
  - `Lab4-03b_GPS_NMEA_Parser`: Sử dụng thư viện giải mã NMEA bóc tách luồng dữ liệu thô thành các biến số thực có ý nghĩa: Kinh độ, Vĩ độ, Cao độ (m), Vận tốc (km/h), Số lượng vệ tinh bám khóa, HDOP và Thời gian chuẩn quốc tế UTC.

### Component 4: Tải Trọng Camera Viễn Thám OV2640
- 📖 **Doc 4.5:** Nguyên lý Cảm biến Ảnh Màu CMOS 2 Megapixel OV2640, Bộ Nén Phần Cứng JPEG & Kỹ thuật Lập trình Gửi Lệnh Cấu hình, Nhận Khối Byte Ảnh JPEG qua UART.
- 💻 **Thực hành Component Camera OV2640:** 
  - `Lab4-04a_Camera_UART`: Gửi tập lệnh cấu hình thanh ghi và bắt đầu phiên chụp ảnh từ Camera OV2640.
  - `Lab4-04b_Camera_Library`: Thu nhận khối byte ảnh JPEG nén phần cứng và hiển thị lên màn hình.

### Component 5: IC Chuyển Mạch Multiplexer 74HC4066
- 🎥 **Video 4.5:** Giải quyết xung đột phần cứng khi Camera và GPS dùng chung cổng UART.
- 📖 **Doc 4.6:** Nguyên lý Vi mạch Khóa Chuyển Mạch Tương tự 4 Kênh 74HC4066 (Quad Bilateral Switch) & Kỹ thuật Lập trình Điều khiển Chuyển Mạch Luân phiên On-Demand giữa Camera và GNSS trên Cùng Cổng UART.
- 💻 **Thực hành Component Multiplexer:** `Lab4-05_Camera_Multiplexer` - Chuyển mạch luân phiên Camera & GPS bằng IC Multiplexer 74HC4066 giải quyết xung đột cổng UART.

### Component 6: Tích Hợp Đa Cảm Biến Toàn Diện
- 📖 **Doc 4.7:** Nguyên lý Phối Hợp Mạng Đa Cảm Biến Trên Vệ Tinh & Kỹ thuật Lập trình Thu thập Dữ liệu Đồng bộ Trong Một Chu Trình Khép Kín.
- 💻 **Thực hành Tích Hợp Đa Cảm Biến:** `Lab4-06_Read_All_Sensors` - Tổng hợp đọc tất cả cảm biến và tải trọng trên vệ tinh trong một chương trình hoàn chỉnh.
- 📝 **Tổng hợp Lab 4:** Xây dựng thành công hệ sinh thái thu thập dữ liệu đa cảm biến và tải trọng quang học hoàn chỉnh.

---

## Lab 5: Phân hệ Truyền thông (COM) & Trạm Mặt Đất
**🎯 Mục tiêu:** Nắm vững lý thuyết truyền sóng không gian, tính toán cân bằng tuyến Link Budget, lập trình module LoRa Ebyte E32, đóng gói khung bản tin viễn trắc với mã CRC-16 và xây dựng trạm mặt đất thu nhận tín hiệu.

- 🎥 **Video 5.1:** Giới thiệu về phân hệ Giao tiếp Viễn thông không gian băng tần UHF.
- 📖 **Doc 5.1:** Cơ sở Lý thuyết Truyền thông Vô tuyến Không gian (Đặc tính Sóng UHF 433MHz, Phương trình Suy hao FSPL của Friis, Cân bằng Tuyến Link Budget & Hiệu ứng Dịch tần Doppler Quỹ đạo LEO).

### Component 1: Module Thu Phát Vô Tuyến LoRa Ebyte E32
- 📖 **Doc 5.2:** Nguyên lý Công nghệ Trải phổ LoRa CSS, Sơ đồ Chân và Chế độ Hoạt động (M0, M1, AUX) của Module Ebyte E32-433T20D & Kỹ thuật Lập trình Cấu hình Thanh ghi, Thu Phát Luồng Byte qua UART.
- 🎥 **Video 5.2:** Cấu hình các tham số vật lý của sóng vô tuyến và kỹ thuật đóng gói bản tin.
- 💻 **Thực hành Component LoRa E32:** 
  - `Lab5-01a_Send_Telemetry_UART`: Cấu hình thanh ghi LoRa E32 và phát luồng dữ liệu byte qua UART.
  - `Lab5-01b_Send_Telemetry_Library`: Đóng gói cấu trúc bản tin Telemetry chuẩn kèm mã tính CRC-16 tự động.
  - `Lab5-02a_Receive_Command_UART`: Lắng nghe chuỗi dữ liệu thô từ cổng không gian và kiểm tra chuỗi đồng bộ Sync Word.
  - `Lab5-02b_Receive_Command_Library`: Giải mã mệnh lệnh điều khiển từ Trái Đất và kích hoạt chân chấp hành.

### Component 2: Trạm Mặt Đất & Giao Thức Truyền Tin Hai Chiều
- 📖 **Doc 5.3:** Nguyên lý Đóng gói Khung Bản tin Telemetry, Thuật toán Kiểm tra Lỗi Chu kỳ CRC-16-CCITT, Cơ chế Stop-and-Wait ARQ & Kiến trúc Trạm Mặt Đất (SDR, Biểu đồ Thác nước Waterfall, Cơ cấu Xoay Rotator Bám đuổi Quỹ đạo TLE).
- 🎥 **Video 5.3:** Xây dựng và vận hành Trạm mặt đất thu phát tín hiệu thực tế.
- 💻 **Thực hành Trạm Mặt Đất:** `Lab5-03_Satellite_Comm_System` - Thiết lập luồng giao tiếp vô tuyến hai chiều hoàn chỉnh giữa vệ tinh và trạm mặt đất.
- 📝 **Tổng hợp Lab 5:** Hoàn thành liên kết truyền thông viễn trắc và viễn lệnh không gian hai chiều tin cậy cao.

---

## Lab 6: Phân hệ Cấu trúc Cơ khí (Structure) & Tích hợp Vật lý
**🎯 Mục tiêu:** Hiểu rõ vai trò đa chiều của khung cơ khí, tiêu chuẩn vật liệu nhôm hàng không Al 6061-T6, xử lý bề mặt Anodize Type III / Alodine, ngăn xếp PC/104, bu lông thông hơi và trực tiếp lắp ráp hoàn thiện khung vệ tinh của bộ kit.

- 🎥 **Video 6.1:** Giới thiệu về cơ khí chính xác, tải trọng phóng tên lửa và cấu trúc bảo vệ vệ tinh trong không gian.

### Component: Khung Cấu Trúc Cơ Khí & Ngăn Xếp Bo Mạch PC/104
- 📖 **Doc 6.1:** Vai Trò Khung Cơ Khí & Tác Động Đa Chiều Lên Các Phân Hệ Khác (Tấm tản nhiệt pin EPS, Lồng Faraday chắn bức xạ OBC, Mặt đất phẳng phản xạ 50 Ohm cho ăng-ten COM, Mặt phẳng tham chiếu cứng vững cho cảm biến).
- 📖 **Doc 6.2:** Vật Liệu Hợp Kim Không Gian (Al 6061-T6, Al 7075-T6), Công nghệ Xử lý Bề mặt Chọn lọc (Anodize Type III chống hàn nguội vs Alodine Class 3 tiếp mass) & Tiêu chuẩn Thoát khí Chân không ASTM E595 (TML < 1%, CVCM < 0.1%).
- 📖 **Doc 6.3:** Tiêu chuẩn Ngăn xếp Bo mạch PC/104, Bu lông Inox A2-70, Keo khóa ren Loctite 222, Bu lông Thông Hơi (Vented Screws) Chống Rò rỉ Ảo TVAC, Bảng Cân Đối Khối Lượng (Mass Budget) & Cân Bằng Trọng Tâm CoM trong Phạm vi $\pm 20\text{ mm}$.
- 🎥 **Video 6.2:** Hướng dẫn quy trình lắp khung vệ tinh của bộ kit.
- 💻 **Thực hành Component Khung Cơ Khí:** Lắp ráp khung theo hướng dẫn và chụp hình ảnh sản phẩm hoàn thiện làm kết quả.
- 📝 **Tổng hợp Lab 6:** Hoàn thiện bộ khung vật lý cho vệ tinh của bộ kit.

---

## Lab 7: Tích hợp Hệ thống Toàn diện & Vận hành Sứ mệnh Bay
**🎯 Mục tiêu:** Nắm vững phương pháp giải quyết 5 thách thức tích hợp đa phân hệ, lập trình phần mềm bay tuần tự Non-blocking, lập trình hệ thống đa nhiệm FreeRTOS, cài đặt máy trạng thái hữu hạn sứ mệnh (Mission FSM) và mô phỏng chu kỳ quỹ đạo 95 phút.

- 🎥 **Video 7.1:** Giới thiệu về bài toán Tích hợp Hệ thống Toàn diện (System Integration) trên vệ tinh.

### Component 1: Phần Mềm Bay Tuần Tự Non-Blocking
- 📖 **Doc 7.1:** Năm Thách Thức Kỹ Thuật Khốc Liệt Khi Tích Hợp Đa Phân Hệ vào Khối 1U (Xung đột Bus I2C/SPI, Nhiễu Tương thích Điện từ EMI/EMC, Sụt áp Đỉnh Tải Brownout, Bẫy nhiệt Chân không, Deadlock) & Kỹ thuật Lập trình Phần mềm Bay theo Kiến trúc Vòng lặp Tuần tự Non-blocking kết hợp `millis()`.
- 💻 **Thực hành Phần mềm Bay Tuần tự:** `Lab7-01_Full_Satellite_Program` - Phiên bản phần mềm bay tích hợp chạy theo vòng lặp tuần tự Non-blocking (Super-Loop) kết hợp `millis()`.

### Component 2: Phần Mềm Bay Đa Nhiệm FreeRTOS, Máy Trạng Thái FSM & Mô Phỏng Quỹ Đạo
- 📖 **Doc 7.2:** Kiến Trúc Phân Lớp Phần Mềm Bay (FSW Layered Architecture), Máy Trạng Thái Hữu Hạn Sứ Mệnh (Mission FSM: `STATE_BOOT` với 30 phút im lặng vô tuyến, `STATE_DETUMBLE` B-dot, `STATE_NORMAL_OPS`, `STATE_PAYLOAD_EXEC`, `STATE_POWER_SAVE`, `STATE_SAFE_MODE`) & Chiến lược Tự Phục Hồi FDIR.
- 📖 **Doc 7.3:** Sổ Tay Vận Hành Bay (Flight Operations Manual - FOM), Giao Thức Thông Qua Trạm Mặt Đất (AOS, Data Dump, LOS) & Kỹ Thuật Lập trình Đa Nhiệm FreeRTOS Mô Phỏng Chu Kỳ Quỹ Đạo LEO 95 Phút (60 phút Ban ngày Nắng / 35 phút Vùng tối Eclipse).
- 🎥 **Video 7.2:** Phân tích luồng dữ liệu thời gian thực và kịch bản phối hợp giữa các phân hệ.
- 💻 **Thực hành Phần mềm Bay Đa nhiệm:** `Lab7-02_RTOS_Satellite_System` - Phiên bản phần mềm bay chạy Hệ điều hành Thời gian thực đa nhiệm FreeRTOS phân chia hai lõi CPU, tích hợp mô phỏng chu kỳ quỹ đạo 95 phút.
- 📝 **Tổng hợp Lab 7:** Vệ tinh đã được tích hợp hoàn chỉnh phần cứng và phần mềm, sẵn sàng vận hành bay thử nghiệm trên quỹ đạo giả lập.

---

## Lab 8: Kỹ thuật Hệ thống Sứ mệnh, Dashboard Builder & Đồ án Capstone
**🎯 Mục tiêu:** Áp dụng phương pháp luận Kỹ thuật Hệ thống Không gian (Systems Engineering), vòng đời dự án NASA/ESA (Phases A-F), ma trận kiểm định MECE, lập trình khối trực quan hóa Dashboard LMS và triển khai 1 trong 3 đề tài đồ án công nghệ không gian thực chiến.

- 🎥 **Video 8.1:** Giới thiệu về Kỹ thuật Hệ thống Không gian (Systems Engineering) và Vòng đời Dự án Hàng không Vũ trụ.
- 📖 **Doc 8.1:** Phương Pháp Luận Kỹ Thuật Hệ Thống Không Gian (Systems Engineering), Vòng Đời Dự Án NASA/ESA theo Pha (Pre-Phase A, Phase A/SRR, Phase B/PDR, Phase C/CDR, Phase D/FRR, Phase E, Phase F) & Ma Trận Kiểm Định Toàn Diện MECE (Test, Analysis, Inspection, Demonstration).

### Component: Khối Trực Quan Hóa Dashboard Builder & Đồ Án Sứ Mệnh Không Gian
- 📖 **Doc 8.2:** Nguyên lý Lựa chọn & Kỹ thuật Lập trình Ánh xạ Dữ liệu Các Khối Trực Quan Hóa (Widgets) trên Dashboard LMS (Radial Gauge, Time-Series Chart, Attitude 3D View, Ground Track Map, Raw Terminal, Uplink Console, Progressive Image Gallery).
- 📖 **Doc 8.3:** Nguyên lý Thiết kế & Khung Mã Nguồn cho 3 Đề Tài Đồ Án Capstone Mini-Project Chuyên Sâu Thực Chiến:
  - *Đề tài 1:* Hệ thống Vệ tinh Viễn thám Giám sát & Cảnh báo Cháy rừng (Wildfire Early Warning Satellite - Geofencing, Xử lý ảnh màu, Nén và Phân mảnh LoRa).
  - *Đề tài 2:* Trạm Vệ tinh LEO Thu thập & Chuyển tiếp Dữ liệu Nông nghiệp Thông minh (Smart Agtech Store-and-Forward Gateway - Polling Beacon, Thuật toán ALOHA, Quản lý thẻ nhớ).
  - *Đề tài 3:* Mạng lưới Vệ tinh Tìm kiếm Cứu nạn Không gian Khẩn cấp (Search and Rescue - SAR Satellite Relay - Bắt tín hiệu phao cứu sinh LoRa SF12, Cờ khẩn cấp, Bản đồ điều phối cứu hộ).
- 🎥 **Video 8.2:** Hướng dẫn sử dụng công cụ kéo thả Dashboard Builder kết nối cổng Web Serial thời gian thực.
- 💻 **Thực hành Đồ án Capstone:** `Lab8-01_Custom_Mission` - Triển khai khung mã nguồn tiêu chuẩn, tùy biến máy trạng thái, tích hợp cảm biến/camera và thiết kế Dashboard hoàn chỉnh cho đề tài lựa chọn.
- 📝 **Tổng hợp Lab 8:** Hoàn tất đồ án Capstone, làm chủ toàn bộ quy trình thiết kế, lập trình và vận hành một sứ mệnh vệ tinh CubeSat độc lập.
