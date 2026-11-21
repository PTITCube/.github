# 🛰️ Giáo trình Vệ tinh PTIT-STEM-CUBE

Chào mừng bạn đến với khóa học lập trình và vận hành Vệ tinh nhỏ chuẩn CubeSat 1U. Khóa học được thiết kế theo triết lý thực hành kết hợp tư duy Kỹ thuật Hệ thống Không gian (Space Systems Engineering), dẫn dắt học viên đi từ các nguyên lý vi điều khiển cơ bản đến một hệ thống vệ tinh hoàn chỉnh chạy Hệ điều hành thời gian thực trên quỹ đạo.

**Cấu trúc bài học chuẩn mực:** Trước khi thực hành với bất kỳ linh kiện nào, giáo trình luôn cung cấp tài liệu kỹ thuật (Doc) chuyên sâu trình bày rõ **Nguyên lý hoạt động phần cứng** và **Phương pháp lập trình** cho linh kiện đó. Đặc biệt, sau mỗi phần Doc hoặc sau mỗi bài Thực hành, hệ thống luôn tích hợp phần **Câu hỏi kiểm tra / củng cố kiến thức** (Quiz) chuyên biệt:
- **Sau phần Doc:** Kiểm tra hiểu biết chuyên sâu về kiến trúc phần cứng, nguyên lý hoạt động và các chuẩn giao tiếp.
- **Sau phần Thực hành:** Kiểm tra chi tiết về khối chức năng code, giải thuật xử lý dữ liệu, cấu hình thanh ghi và kỹ năng gỡ lỗi hệ thống.

---

## Lab 0: Giới thiệu Tổng quan Kỹ thuật Không gian & Vệ tinh CubeSat
**🎯 Mục tiêu:** Nắm vững lịch sử, tiêu chuẩn kích thước CubeSat 1U, ống phóng P-POD, môi trường vật lý quỹ đạo LEO và nguyên lý 6 phân hệ cốt lõi.

- 🎥 **Video 0.1:** Tổng quan Vệ tinh Nhỏ CubeSat & Các Phân hệ Không gian
- 📖 **Doc 0.1:** Tiêu chuẩn CubeSat 1U, Ống phóng P-POD & Môi trường Quỹ đạo LEO
- ❓ **Câu hỏi kiểm tra Doc 0.1:** Trắc nghiệm lịch sử CubeSat, tiêu chuẩn 1U, cơ chế P-POD và các hiện tượng vật lý LEO (thoát khí, hàn nguội, SEU/SEL/TID, chu kỳ nhiệt).
- 📖 **Doc 0.2:** Kiến trúc Hệ thống & Vai trò 6 Phân hệ Cốt lõi trên CubeSat 1U
- ❓ **Câu hỏi kiểm tra Doc 0.2:** Trắc nghiệm chức năng cốt lõi, luồng dữ liệu viễn trắc/viễn lệnh và cơ chế phối hợp giữa 6 phân hệ.
- 🎥 **Video 0.2:** Mô hình 3D Vệ tinh CubeSat Thời gian thực trên WebGL
- 💻 **Thực hành:** Khám phá Mô hình 3D & Thông số Kỹ thuật các Phân hệ
- ❓ **Câu hỏi kiểm tra Thực hành:** Trắc nghiệm nhận diện vị trí bo mạch, cổng kết nối, ăng-ten và thông số kỹ thuật từng linh kiện trên mô hình 3D.
- 📝 **Tổng hợp Lab 0:** Nắm vững cấu trúc tổng thể và mối tương quan phối hợp giữa các phân hệ trên vệ tinh.

---

## Lab 1: Máy tính trên Bo mạch (OBC) & Môi trường Lập trình Nhúng
**🎯 Mục tiêu:** Làm chủ vi điều khiển ESP32-WROOM-32, môi trường Web IDE đám mây, nạp firmware qua Web Serial API, làm chủ nguyên lý và lập trình từng linh kiện ngoại vi cơ bản (LED, Nút nhấn, LED 7 đoạn 74HC595, UART, WiFi/Web Server).

- 🎥 **Video 1.1:** Tổng quan Phân hệ Xử lý Trung tâm (OBC) & Vi điều khiển ESP32
- 📖 **Doc 1.1:** Kiến trúc Phần cứng ESP32-WROOM-32, Strapping Pins & Bản đồ Bộ nhớ
- ❓ **Câu hỏi kiểm tra Doc 1.1:** Trắc nghiệm kiến trúc lõi kép Xtensa LX6, bộ nhớ SRAM/Flash, các chân Strapping Pins nguy hiểm và quy hoạch GPIO.
- 🎥 **Video 1.2:** Biên dịch Cloud & Nạp Firmware qua Web Serial API
- 📖 **Doc 1.2:** Môi trường Web IDE & Giao thức Nạp Firmware qua Web Serial API
- ❓ **Câu hỏi kiểm tra Doc 1.2:** Trắc nghiệm quy trình biên dịch Cloud Server, cơ chế bắt tay Web Serial API và cấu hình tốc độ nạp.
- 📖 **Doc 1.3:** Nguyên lý Điều khiển GPIO & Điều chế Độ rộng Xung LEDC PWM
- ❓ **Câu hỏi kiểm tra Doc 1.3:** Trắc nghiệm mạch ngõ ra Push-Pull, tính toán điện trở hạn dòng, cấu hình kênh LEDC và chu kỳ xung PWM.
- 💻 **Thực hành Component LED:**
  - `Lab1-01_Blink_LED`: Nhấp nháy LED Heartbeat giám sát chu trình sống của bo mạch.
  - `Lab1-02_Control_Multiple_LEDs`: Điều khiển chuỗi LED tuần tự bằng mảng và vòng lặp.
  - `Lab1-03_PWM_LED`: Điều chế xung PWM tạo hiệu ứng đèn thở (Breathing LED).
- ❓ **Câu hỏi kiểm tra Thực hành LED:** Trắc nghiệm cấu hình `pinMode()`, `digitalWrite()`, các hàm LEDC PWM (`ledcSetup()`, `ledcAttachPin()`, `ledcWrite()`) và giải thuật Duty Cycle.
- 📖 **Doc 1.4:** Nút nhấn Cơ học, Điện trở Pull-up & Giải thuật Lọc Rung Tiếp điểm (Debounce)
- ❓ **Câu hỏi kiểm tra Doc 1.4:** Trắc nghiệm trạng thái Floating, điện trở kéo lên nội tâm (`INPUT_PULLUP`) và hiện tượng nảy tiếp điểm cơ khí.
- 💻 **Thực hành Component Nút Nhấn:**
  - `Lab1-04_Button`: Đọc trạng thái mức logic của nút nhấn.
  - `Lab1-05_LED_Button`: Đảo trạng thái đèn LED bằng nút nhấn kết hợp chống rung.
- ❓ **Câu hỏi kiểm tra Thực hành Nút Nhấn:** Trắc nghiệm phân tích hàm `digitalRead()`, biến trạng thái chốt (Toggle) và giải thuật lọc chống rung phần mềm.
- 📖 **Doc 1.5:** IC Dịch Bit Chốt 74HC595 & Lập trình Điều khiển LED 7 Đoạn
- ❓ **Câu hỏi kiểm tra Doc 1.5:** Trắc nghiệm cấu tạo thanh ghi dịch/chốt 8-bit, giản đồ xung nhịp (DS, SH_CP, ST_CP) và bảng mã giải mã LED 7 đoạn.
- 💻 **Thực hành Component 74HC595 & LED 7 Đoạn:**
  - `Lab1-06_7_Segment_LED`: Dịch 8-bit qua IC 74HC595 hiển thị số đếm 0-9 trên LED 7 đoạn.
- ❓ **Câu hỏi kiểm tra Thực hành 74HC595:** Trắc nghiệm hàm `shiftOut()`, thứ tự bit MSBFIRST/LSBFIRST, thao tác chốt `latchPin` và mảng mã byte hiển thị.
- 📖 **Doc 1.6:** Giao tiếp Nối tiếp Bất đồng bộ UART & Lập trình Serial
- ❓ **Câu hỏi kiểm tra Doc 1.6:** Trắc nghiệm cấu trúc khung truyền UART (Start, Data, Parity, Stop bits), tốc độ baud và bộ đệm phần cứng FIFO.
- 💻 **Thực hành Component UART:**
  - `Lab1-07_Serial_Communication`: Truyền nhận dữ liệu qua cổng nối tiếp UART.
  - `Lab1-08_Serial_Control_LED`: Phân tích cú pháp lệnh Serial điều khiển bật/tắt thiết bị.
- ❓ **Câu hỏi kiểm tra Thực hành UART:** Trắc nghiệm hàm `Serial.available()`, `Serial.read()`, cấu trúc `switch-case` giải mã lệnh và định dạng xuất chuỗi.
- 📖 **Doc 1.7:** Mạng Không dây WiFi (STA / SoftAP) & Máy chủ Web HTTP Nhúng
- ❓ **Câu hỏi kiểm tra Doc 1.7:** Trắc nghiệm chế độ trạm STA vs điểm truy cập SoftAP, cấp phát IP, giao thức HTTP và xử lý phương thức GET/POST.
- 📖 **Doc 1.8:** Kỹ thuật Định thời Non-blocking với `millis()` & Chống Tràn số
- ❓ **Câu hỏi kiểm tra Doc 1.8:** Trắc nghiệm tác hại của hàm chặn `delay()`, kiểu dữ liệu `unsigned long` và phép trừ chống lỗi tràn số sau 49.7 ngày.
- 🎥 **Video 1.3:** Kết nối WiFi & Điều khiển Thiết bị qua Web Server Nhúng
- 💻 **Thực hành Component WiFi & Web Server:**
  - `Lab1-09_WiFi_Connection`: Kết nối ESP32 vào mạng WiFi cục bộ và lấy địa chỉ IP.
  - `Lab1-10_WiFi_AP_Mode`: Cấu hình vệ tinh phát mạng WiFi SoftAP bảo mật WPA2.
  - `Lab1-11_Web_Server_LED`: Dựng Web Server HTTP nhúng điều khiển thiết bị qua trình duyệt.
- ❓ **Câu hỏi kiểm tra Thực hành WiFi & Web Server:** Trắc nghiệm cấu hình `WiFi.begin()`, `WiFi.softAP()`, hàm định tuyến `server.on()` và vòng lặp `server.handleClient()`.
- 📝 **Tổng hợp Lab 1:** Hoàn thiện kỹ năng lập trình nhúng C++ cơ bản và điều khiển toàn diện các linh kiện ngoại vi của bo mạch OBC.

---

## Lab 2: Phân hệ Năng lượng (EPS) & Quản lý Nguồn Quỹ đạo
**🎯 Mục tiêu:** Nắm vững nguyên lý pin Li-Po, mạch sạc CC/CV TP4056, lập trình đọc điện áp và dung lượng pin với IC MAX17048 qua I2C, công tắc ngắt an toàn và lập trình điều khiển dòng ra vào mạch hạ áp cấp nguồn cảm biến để tiết kiệm năng lượng.

- 🎥 **Video 2.1:** Tổng quan Phân hệ Nguồn (EPS) & Quản lý Năng lượng Vệ tinh
- 📖 **Doc 2.1:** Pin Li-Po, Thuật toán Sạc CC/CV, Nguồn Xung & Giám sát Pin MAX17048 qua I2C
- ❓ **Câu hỏi kiểm tra Doc 2.1:** Trắc nghiệm đặc tính phóng pin Li-Po, 2 pha sạc CC/CV của TP4056, hiệu suất Buck/Boost và các thanh ghi `VCELL`, `SOC` của MAX17048 qua I2C.
- 🎥 **Video 2.2:** Đọc Thanh ghi Điện áp và Dung lượng Pin MAX17048 qua I2C
- 💻 **Thực hành Component Nguồn & MAX17048:** 
  - `Lab2-01a_Battery_I2C`: Đọc trực tiếp thanh ghi điện áp và dung lượng pin MAX17048 qua `Wire.h`.
  - `Lab2-01b_Battery_Library`: Giám sát thông số pin và quản lý nguồn EPS qua thư viện PTITCube.
- ❓ **Câu hỏi kiểm tra Thực hành Nguồn & MAX17048:** Trắc nghiệm ghép 2 byte thành số nguyên 16-bit, hệ số phân giải $78.125\mu\text{V}$, hàm `myEPS.getVoltage()` và ngưỡng cảnh báo pin yếu.
- 📖 **Doc 2.2:** Cơ chế An toàn Phóng (RBF), Mạch Giám sát Brownout & Kỹ thuật Power Gating Cảm biến
- ❓ **Câu hỏi kiểm tra Doc 2.2:** Trắc nghiệm công tắc hành trình chân ray, chốt RBF, mạch Reset Brownout (BOD) và kỹ thuật điều khiển dòng vào hạ áp để triệt tiêu dòng tĩnh của cảm biến.
- 💻 **Thực hành Component Tiết Kiệm Điện:** `Lab2-02_Power_Saving` - Tự động kích hoạt chế độ tiết kiệm năng lượng (Power Saving Mode) dựa trên điện áp/dung lượng pin và điều khiển mạch hạ áp qua thư viện `PTIT_EPS`.
- ❓ **Câu hỏi kiểm tra Thực hành Tiết Kiệm Điện:** Trắc nghiệm điều khiển chân khống chế dòng vào hạ áp, quy tắc logic (0 bật / 1 ngắt), thời gian ổn định nguồn và hiệu quả giảm tiêu thụ điện.
- 📝 **Tổng hợp Lab 2:** Nắm vững phương pháp quản lý, tối ưu hóa và bảo vệ nguồn điện cho vệ tinh.

---

## Lab 3: Xử lý Dữ liệu và Lệnh (C&DH) & Hệ thống Lưu trữ Hộp Đen
**🎯 Mục tiêu:** Nắm vững nguyên lý và lập trình giao tiếp SPI với thẻ MicroSD, xây dựng bộ phân tích lệnh Shell CLI, lập trình đa nhiệm FreeRTOS với khóa Mutex và bộ định thời Watchdog Timer.

- 🎥 **Video 3.1:** Phân hệ C&DH & Hệ thống Lưu trữ Hộp Đen Dữ liệu Vệ tinh
- 📖 **Doc 3.1:** Giao tiếp Bus SPI Tốc độ cao & Quản lý Hệ thống Tập tin FAT32 trên Thẻ MicroSD
- ❓ **Câu hỏi kiểm tra Doc 3.1:** Trắc nghiệm 4 đường tín hiệu SPI (MOSI, MISO, SCK, CS), chuẩn CPOL/CPHA Mode 0, bảng phân bổ FAT32 và vai trò hàm `file.flush()`.
- 🎥 **Video 3.2:** Thao tác Đọc/Ghi Thẻ MicroSD An toàn & Tránh Phân Mảnh Dữ liệu
- 💻 **Thực hành Component Thẻ Nhớ MicroSD:** 
  - `Lab3-01a_MicroSD_SPI`: Khởi tạo phần cứng và giao tiếp thẻ MicroSD qua bus SPI.
  - `Lab3-01b_MicroSD_Library`: Ghi log dữ liệu viễn trắc tự động định dạng CSV có dấu thời gian.
- ❓ **Câu hỏi kiểm tra Thực hành Thẻ Nhớ MicroSD:** Trắc nghiệm hàm `SD.begin()`, cờ mở tệp `FILE_APPEND`, định dạng chuỗi CSV và cơ chế xả đệm `dataFile.flush()`.
- 📖 **Doc 3.2:** Kiến trúc Bộ Phân tích Cú pháp Lệnh Shell CLI Quản lý Tập tin trên Vệ tinh
- ❓ **Câu hỏi kiểm tra Doc 3.2:** Trắc nghiệm kiến trúc Lexer/Parser dòng lệnh, tách token khoảng trắng, mã lệnh và tham số theo triết lý Silent Success.
- 💻 **Thực hành Component Shell CLI:** `Lab3-02_Linux_FS_Commands` - Xây dựng hệ thống 11 lệnh Linux quản lý tệp trên thẻ nhớ qua cổng Serial.
- ❓ **Câu hỏi kiểm tra Thực hành Shell CLI:** Trắc nghiệm duyệt thư mục `file.openNextFile()`, đọc tệp `file.read()`, xóa tệp `SD.remove()` và kiểm tra dung lượng `SD.usedBytes()`.
- 🎥 **Video 3.3:** Hệ điều hành Thời gian thực (FreeRTOS) & Lập trình Đa nhiệm trên Vệ tinh
- 📖 **Doc 3.3:** Đa nhiệm FreeRTOS, Quản lý Tác vụ, Xung đột Tài nguyên & Đồng bộ hóa bằng Mutex
- ❓ **Câu hỏi kiểm tra Doc 3.3:** Trắc nghiệm bộ điều phối chiếm quyền (Preemption), tranh chấp tài nguyên dùng chung, nghịch đảo ưu tiên (Priority Inversion) và kế thừa ưu tiên qua Mutex.
- 💻 **Thực hành Component FreeRTOS Multitasking:** `Lab3-03_Multitasking_Scheduler` - Thực thi đồng thời 3 tác vụ độc lập đồng bộ hóa an toàn qua Mutex và `PTIT_Scheduler`.
- ❓ **Câu hỏi kiểm tra Thực hành FreeRTOS:** Trắc nghiệm hàm `xTaskCreatePinnedToCore()`, vòng lặp `for(;;) `, `vTaskDelay()` và cặp hàm khóa tài nguyên `xSemaphoreTake()` / `xSemaphoreGive()`.
- 🎥 **Video 3.4:** Tự Động Phục Hồi Lỗi Treo Hệ Thống Bằng Watchdog Timer
- 📖 **Doc 3.4:** Cơ chế Mạch Giám sát Phần cứng WDT & Lập trình Task Watchdog Timer (TWDT)
- ❓ **Câu hỏi kiểm tra Doc 3.4:** Trắc nghiệm cơ chế đếm ngược WDT, phân biệt IWDT và TWDT, quy trình làm tươi Watchdog Timer (Feed/Reset WDT).
- 💻 **Thực hành Component Watchdog:** `Lab3-04_Watchdog_Timer` - Kích hoạt Task Watchdog Timer, nạp lại định kỳ và tự động phục hồi khi hệ thống bị treo.
- 💻 **Thực hành Component Hướng sự kiện (Event-Driven):** `Lab3-05_Event_Driven_Queue` - Xây dựng kiến trúc hướng sự kiện xử lý ngắt và viễn lệnh qua FreeRTOS Queue.
- ❓ **Câu hỏi kiểm tra Thực hành Watchdog & Event:** Trắc nghiệm cấu hình `esp_task_wdt_init()`, `esp_task_wdt_add()`, `esp_task_wdt_reset()` và truyền nhận hàng đợi `xQueueSend()` / `xQueueReceive()`.
- 📝 **Tổng hợp Lab 3:** Thiết lập thành công hộp đen lưu trữ dữ liệu quỹ đạo và xây dựng nền tảng phần mềm đa nhiệm tin cậy cao.

---

## Lab 4: Phân hệ Cảm biến (Sensors) & Tải trọng Quang học
**🎯 Mục tiêu:** Nắm vững nguyên lý và lập trình từng cảm biến cụ thể: cảm biến khí quyển BMP280, cảm biến quán tính IMU MPU6500, module định vị GNSS L76X, tải trọng Camera OV2640 và IC chuyển mạch 74HC4066.

- 🎥 **Video 4.1:** Tổng quan Phân hệ Cảm biến & Tải trọng Quang học trên Vệ tinh
- 📖 **Doc 4.1:** Giao thức Bus I2C & Lập trình Cảm biến Khí quyển BMP280
- ❓ **Câu hỏi kiểm tra Doc 4.1:** Trắc nghiệm phần cứng Open-Drain, điều kiện START/STOP, địa chỉ I2C `0x76` của BMP280 và công thức tính độ cao khí áp.
- 🎥 **Video 4.2:** Đọc Cảm biến Khí quyển Áp suất, Nhiệt độ & Tính Độ cao Barometric
- 💻 **Thực hành Component BMP280:** 
  - `Lab4-01a_Environment_I2C`: Đọc mảng hằng số hiệu chuẩn và dữ liệu thô từ BMP280 qua I2C.
  - `Lab4-01b_Environment_Library`: Đọc và tính toán áp suất khí quyển, nhiệt độ, độ cao qua thư viện PTITCube.
- ❓ **Câu hỏi kiểm tra Thực hành BMP280:** Trắc nghiệm hàm `Wire.read()`, bù trừ phi tuyến tính với các hệ số hiệu chuẩn (`dig_T`, `dig_P`) và công thức tính độ cao Hypsometric.
- 🎥 **Video 4.3:** Cảm biến Quán tính IMU 6 Trục & Thuật toán Ước lượng Góc Nghiêng
- 📖 **Doc 4.2:** Cảm biến IMU 6 Trục MPU6500, Từ kế 3 Trục GY-271 & Bộ Lọc Bù (Complementary Filter)
- ❓ **Câu hỏi kiểm tra Doc 4.2:** Trắc nghiệm cảm biến MEMS, hiện tượng trôi dạt Gyro, công thức tính góc hướng La bàn $\text{atan2}(Y, X)$ và hệ số bộ lọc bù $\alpha = 0.98$.
- 💻 **Thực hành Component IMU MPU6500 & La Bàn:** 
  - `Lab4-02a_IMU_I2C`: Đọc dữ liệu gia tốc, vận tốc góc từ MPU6500 và từ trường từ GY-271 qua I2C thuần.
  - `Lab4-02b_IMU_Library`: Cài đặt bộ lọc bù ước lượng góc nghiêng Roll, Pitch và Heading La bàn qua thư viện.
- ❓ **Câu hỏi kiểm tra Thực hành IMU MPU6500:** Trắc nghiệm thanh ghi `PWR_MGMT_1 (0x6B)`, đọc Burst 14 byte từ `0x3B`, chuyển đổi số nguyên bù 2 sang đơn vị trọng trường ($g$) và thuật toán lọc bù.
- 🎥 **Video 4.4:** Thu nhận Tọa độ Toàn cầu Định vị GNSS từ Module L76X
- 📖 **Doc 4.3:** Module Định vị GNSS L76X & Giao tiếp UART Nhận Bản tin NMEA Thô
- ❓ **Câu hỏi kiểm tra Doc 4.3:** Trắc nghiệm cấu tạo ăng-ten gốm, thời gian chốt vệ tinh TTFF (Cold/Hot start) và cấu hình UART2 tốc độ 9600 bps.
- 💻 **Thực hành Đọc giá trị thô NMEA:** 
  - `Lab4-03a_GPS_UART`: Nhận và xuất trực tiếp luồng bản tin NMEA thô (`$GPRMC`, `$GPGGA`) từ GNSS qua UART.
  - `Lab4-03b_GPS_Library`: Đệm dòng dữ liệu, phân loại câu tin NMEA và kiểm tra tính toàn vẹn Checksum XOR.
- ❓ **Câu hỏi kiểm tra Thực hành Đọc NMEA thô:** Trắc nghiệm cấu hình `Serial2.begin(9600)`, vòng lặp đọc byte và nhận diện bản tin `$GPRMC`.
- 📖 **Doc 4.4:** Chuẩn Giao thức NMEA 0183 & Kỹ thuật Giải mã Tọa độ GPS Thập phân
- ❓ **Câu hỏi kiểm tra Doc 4.4:** Trắc nghiệm cấu trúc bản tin NMEA, công thức đổi tọa độ Độ-Phút sang Độ Thập phân, tính Checksum XOR và chỉ số HDOP.
- 💻 **Thực hành Chuyển đổi NMEA thành các trường giá trị có ý nghĩa:** 
  - `Lab4-03c_GPS_PTITCube`: Bóc tách tọa độ, độ cao, vận tốc, hướng đi và thời gian UTC qua thư viện PTITCube.
- ❓ **Câu hỏi kiểm tra Thực hành Giải mã NMEA:** Trắc nghiệm máy trạng thái `myGPS.update()`, kiểm tra điều kiện chốt vệ tinh và trích xuất dữ liệu tọa độ số thực.
- 📖 **Doc 4.5:** Camera CMOS OV2640, Nén Ảnh Phần cứng JPEG & Giao thức Bắt tay UART
- ❓ **Câu hỏi kiểm tra Doc 4.5:** Trắc nghiệm ma trận điểm ảnh CMOS, xung nhịp XCLK, cơ chế nén JPEG và cặp byte đánh dấu ảnh (`0xFFD8` / `0xFFD9`).
- 💻 **Thực hành Component Camera OV2640:** 
  - `Lab4-04a_Camera_UART`: Bắt tay UART chụp ảnh với ESP32-CAM và ghi trực tiếp luồng JPEG vào MicroSD.
  - `Lab4-04b_Camera_Library`: Chụp ảnh và tự động quản lý lưu trữ vào MicroSD qua thư viện `PTIT_Camera`.
- ❓ **Câu hỏi kiểm tra Thực hành Camera OV2640:** Trắc nghiệm gói lệnh chụp ảnh, đệm nhận luồng byte ảnh nhị phân qua UART và lưu trữ dữ liệu ảnh.
- 🎥 **Video 4.5:** Giải quyết Xung đột Cổng UART giữa Camera và GPS bằng IC Ghép kênh
- 📖 **Doc 4.6:** IC Khóa Chuyển mạch Tương tự 74HC4066 & Kỹ thuật Ghép kênh UART Luân phiên
- ❓ **Câu hỏi kiểm tra Doc 4.6:** Trắc nghiệm xung đột cổng UART phần cứng, cấu tạo công tắc 74HC4066, điện trở tiếp xúc $R_{ON}$ và giải pháp phân chia thời gian (TDM).
- 💻 **Thực hành Component Multiplexer:** `Lab4-05_Camera_Multiplexer` - Chuyển mạch luân phiên Camera & GPS bằng IC Multiplexer 74HC4066 giải quyết xung đột cổng UART.
- ❓ **Câu hỏi kiểm tra Thực hành Multiplexer:** Trắc nghiệm điều khiển chân chọn kênh GPIO `HIGH`/`LOW`, quy trình flush bộ đệm và luân phiên giữa lấy tọa độ và chụp ảnh.
- 📖 **Doc 4.7:** Kiến trúc Thu thập Mạng Đa Cảm biến Đồng bộ Trong Chu trình Khép kín
- ❓ **Câu hỏi kiểm tra Doc 4.7:** Trắc nghiệm chu trình vòng lặp cảm biến tập trung, chiến lược đồng bộ dấu thời gian (Timestamping) và phân bổ chu kỳ lấy mẫu.
- 💻 **Thực hành Tích Hợp Đa Cảm Biến:** `Lab4-06_Read_All_Sensors` - Thu thập dữ liệu toàn bộ cảm biến (BMP280, MPU6500, QMC5883, GPS) và đóng gói gói tin Telemetry.
- ❓ **Câu hỏi kiểm tra Thực hành Đa Cảm Biến:** Trắc nghiệm cấu trúc dữ liệu `struct TelemetryPacket`, gom dữ liệu khí áp, quán tính, tọa độ và tối ưu tài nguyên.
- 📝 **Tổng hợp Lab 4:** Xây dựng thành công hệ sinh thái thu thập dữ liệu đa cảm biến và tải trọng quang học hoàn chỉnh.

---

## Lab 5: Phân hệ Truyền thông (COM) & Trạm Mặt Đất
**🎯 Mục tiêu:** Nắm vững lý thuyết truyền sóng không gian, tính toán cân bằng tuyến Link Budget, lập trình module LoRa Ebyte E32, đóng gói khung bản tin viễn trắc với mã CRC-16 và xây dựng trạm mặt đất thu nhận tín hiệu.

- 🎥 **Video 5.1:** Tổng quan Phân hệ Truyền thông (COM) Băng tần UHF trên Vệ tinh
- 📖 **Doc 5.1:** Lý thuyết Sóng Vô tuyến Không gian, Cân bằng Tuyến Link Budget & Dịch tần Doppler
- ❓ **Câu hỏi kiểm tra Doc 5.1:** Trắc nghiệm công thức suy hao không gian tự do Friis, các thông số Link Budget (EIRP, độ nhạy thu) và độ lệch tần Doppler băng UHF 433MHz trên quỹ đạo LEO.
- 📖 **Doc 5.2:** Công nghệ Trải phổ LoRa CSS & Lập trình Module Ebyte E32-433T20D
- ❓ **Câu hỏi kiểm tra Doc 5.2:** Trắc nghiệm kỹ thuật trải phổ Chirp Spread Spectrum (CSS), các chân chế độ M0/M1, chân tín hiệu bận AUX và cấu hình công suất phát.
- 🎥 **Video 5.2:** Cấu hình Tham số Vô tuyến & Kỹ thuật Đóng gói Bản tin Viễn trắc
- 💻 **Thực hành Component LoRa E32:** 
  - `Lab5-01a_Send_Telemetry_UART`: Cấu hình tham số LoRa E32 và phát luồng dữ liệu viễn trắc qua UART.
  - `Lab5-01b_Send_Telemetry_Library`: Đóng gói bản tin Telemetry chuẩn kèm mã kiểm tra CRC-16 tự động.
  - `Lab5-02a_Receive_Command_UART`: Thu nhận luồng dữ liệu không gian và kiểm tra chuỗi đồng bộ Sync Word.
  - `Lab5-02b_Receive_Command_Library`: Giải mã viễn lệnh Telecommand từ Trái Đất và điều khiển cơ cấu chấp hành.
- ❓ **Câu hỏi kiểm tra Thực hành LoRa E32:** Trắc nghiệm kiểm tra chân `AUX == HIGH`, gửi dữ liệu qua `SerialLoRa.write()`, cấu trúc khung tin và xác thực Header/Sync Word.
- 📖 **Doc 5.3:** Đóng gói Bản tin Telemetry, Kiểm lỗi CRC-16 & Kiến trúc Trạm Mặt Đất
- ❓ **Câu hỏi kiểm tra Doc 5.3:** Trắc nghiệm đa thức sinh CRC-16-CCITT (`0x1021`), cơ chế Stop-and-Wait ARQ, máy thu vô tuyến định nghĩa bằng phần mềm (SDR) và phần tử quỹ đạo TLE.
- 🎥 **Video 5.3:** Xây dựng & Vận hành Trạm Mặt Đất Thu Phát Tín hiệu Thực tế
- 💻 **Thực hành Trạm Mặt Đất:** `Lab5-03_Ground_Station_Demo` - Thiết lập luồng giao tiếp vô tuyến hai chiều hoàn chỉnh giữa vệ tinh và trạm mặt đất.
- ❓ **Câu hỏi kiểm tra Thực hành Trạm Mặt Đất:** Trắc nghiệm xác thực mã CRC-16 bản tin Downlink, đóng gói Telecommand và giải mã phản hồi ACK từ vệ tinh.
- 📝 **Tổng hợp Lab 5:** Hoàn thành liên kết truyền thông viễn trắc và viễn lệnh không gian hai chiều tin cậy cao.

---

## Lab 6: Phân hệ Cấu trúc Cơ khí (Structure) & Tích hợp Vật lý
**🎯 Mục tiêu:** Hiểu rõ vai trò đa chiều của khung cơ khí, tiêu chuẩn vật liệu nhôm hàng không Al 6061-T6, xử lý bề mặt Anodize Type III / Alodine, ngăn xếp PC/104, bu lông thông hơi và trực tiếp lắp ráp hoàn thiện khung vệ tinh của bộ kit.

- 🎥 **Video 6.1:** Tổng quan Phân hệ Cấu trúc Cơ khí (Structure) & Bảo vệ Vệ tinh Trong Không gian
- 📖 **Doc 6.1:** Vai trò Khung Cơ khí & Tác động Đa chiều Lên Các Phân hệ trên CubeSat
- ❓ **Câu hỏi kiểm tra Doc 6.1:** Trắc nghiệm tác động đa chiều của khung: tản nhiệt thụ động (EPS), lồng Faraday chắn nhiễu EMI (OBC), mặt đất phản xạ Ground Plane (COM) và hệ quy chiếu tọa độ (ADCS/Sensors).
- 📖 **Doc 6.2:** Hợp kim Nhôm Hàng không, Công nghệ Xử lý Bề mặt & Tiêu chuẩn Thoát khí ASTM E595
- ❓ **Câu hỏi kiểm tra Doc 6.2:** Trắc nghiệm so sánh Al 6061-T6 vs Al 7075-T6, lớp Anodize Type III cách điện chống hàn nguội, lớp Alodine tiếp mass vỏ và tiêu chuẩn thoát khí ASTM E595 (TML và CVCM).
- 📖 **Doc 6.3:** Tiêu chuẩn Ngăn xếp Bo mạch PC/104, Bu lông Thông hơi & Cân đối Khối lượng (Mass Budget)
- ❓ **Câu hỏi kiểm tra Doc 6.3:** Trắc nghiệm khoảng cách ngăn xếp PC/104, hiện tượng rò rỉ ảo do bẫy khí, bu lông thông hơi, keo khóa ren Loctite 222 và cân bằng trọng tâm CoM trong phạm vi $\pm 20\text{ mm}$.
- 🎥 **Video 6.2:** Hướng dẫn Quy trình Lắp ráp Khung Cơ khí CubeSat 1U của Bộ Kit
- 💻 **Thực hành Khung Cơ Khí:** Lắp ráp khung cơ khí theo hướng dẫn và kiểm tra dung sai kết cấu thực tế.
- ❓ **Câu hỏi kiểm tra Thực hành Khung Cơ Khí:** Trắc nghiệm thứ tự siết bu lông theo đường chéo, kiểm tra dung sai kích thước 1U ($100\times 100\times 113.5\text{ mm}$) và quy trình nghiệm thu vật lý.
- 📝 **Tổng hợp Lab 6:** Hoàn thiện bộ khung vật lý cho vệ tinh của bộ kit.

---

## Lab 7: Tích hợp Hệ thống Toàn diện & Vận hành Sứ mệnh Bay
**🎯 Mục tiêu:** Nắm vững phương pháp giải quyết 5 thách thức tích hợp đa phân hệ, lập trình phần mềm bay tuần tự Non-blocking, lập trình hệ thống đa nhiệm FreeRTOS, cài đặt máy trạng thái hữu hạn sứ mệnh (Mission FSM) và mô phỏng chu kỳ quỹ đạo 95 phút.

- 🎥 **Video 7.1:** Tổng quan Bài toán Tích hợp Hệ thống Toàn diện (System Integration) trên Vệ tinh
- 📖 **Doc 7.1:** 5 Thách thức Tích hợp Hệ thống 1U & Kiến trúc Phần mềm Bay Tuần tự Non-blocking
- ❓ **Câu hỏi kiểm tra Doc 7.1:** Trắc nghiệm 5 thách thức tích hợp (nhiễu EMI cao tần từ LoRa, sụt áp Brownout, bẫy nhiệt chân không, nghẽn đường truyền) và kiến trúc Super-Loop Non-blocking.
- 💻 **Thực hành Phần mềm Bay Tuần tự:** `Lab7-01_Full_Satellite_Program` - Phần mềm bay tích hợp chạy theo vòng lặp tuần tự Non-blocking kết hợp `millis()`.
- ❓ **Câu hỏi kiểm tra Thực hành Phần mềm Bay Tuần tự:** Trắc nghiệm cấu trúc hàm `loop()`, các biến cờ thời gian bất đồng bộ (`lastTelemetry`, `lastSensorRead`) và cơ chế gom dữ liệu không dùng `delay()`.
- 📖 **Doc 7.2:** Kiến trúc Phân lớp Phần mềm Bay (FSW), Máy Trạng thái Sứ mệnh & Cơ chế Tự phục hồi FDIR
- ❓ **Câu hỏi kiểm tra Doc 7.2:** Trắc nghiệm quy định 30 phút im lặng vô tuyến trong `STATE_BOOT`, thuật toán dập quay B-dot, ngưỡng chuyển trạng thái `STATE_POWER_SAVE` và quy trình phục hồi FDIR.
- 📖 **Doc 7.3:** Sổ tay Vận hành Bay (FOM) & Mô phỏng Chu kỳ Quỹ đạo LEO 95 Phút
- ❓ **Câu hỏi kiểm tra Doc 7.3:** Trắc nghiệm cửa sổ liên lạc trạm mặt đất (AOS, Data Dump, LOS) và mô hình phân bổ chu kỳ quỹ đạo LEO (60 phút ban ngày / 35 phút vùng tối).
- 🎥 **Video 7.2:** Luồng Dữ liệu Thời gian thực & Kịch bản Hoạt động Phối hợp Đa Phân hệ
- 💻 **Thực hành Phần mềm Bay Đa nhiệm:** `Lab7-02_RTOS_Satellite_System` - Phần mềm bay đa nhiệm FreeRTOS phân chia hai lõi CPU, tích hợp mô phỏng chu kỳ quỹ đạo 95 phút.
- ❓ **Câu hỏi kiểm tra Thực hành Phần mềm Bay Đa nhiệm:** Trắc nghiệm phân chia tác vụ giữa Core 0 (Truyền thông) và Core 1 (Cảm biến), hàng đợi Queue liên lõi và mô phỏng chu kỳ ánh sáng mặt trời.
- 📝 **Tổng hợp Lab 7:** Vệ tinh đã được tích hợp hoàn chỉnh phần cứng và phần mềm, sẵn sàng vận hành bay thử nghiệm trên quỹ đạo giả lập.

---

## Lab 8: Kỹ thuật Hệ thống Sứ mệnh, Dashboard Builder & Đồ án Capstone
**🎯 Mục tiêu:** Áp dụng phương pháp luận Kỹ thuật Hệ thống Không gian (Systems Engineering), vòng đời dự án NASA/ESA (Phases A-F), ma trận kiểm định MECE, lập trình khối trực quan hóa Dashboard LMS và triển khai 1 trong 3 đề tài đồ án công nghệ không gian thực chiến.

- 🎥 **Video 8.1:** Kỹ thuật Hệ thống Không gian (Systems Engineering) & Vòng đời Dự án Hàng không Vũ trụ
- 📖 **Doc 8.1:** Phương pháp luận Kỹ thuật Hệ thống, Vòng đời Dự án NASA/ESA & Ma trận Kiểm định MECE
- ❓ **Câu hỏi kiểm tra Doc 8.1:** Trắc nghiệm các mốc thẩm định dự án (SRR, PDR, CDR, FRR) và 4 phương pháp kiểm định MECE (Test, Analysis, Inspection, Demonstration).
- 📖 **Doc 8.2:** Thiết kế Giao diện Giám sát & Ánh xạ Dữ liệu Các Widget trên Dashboard LMS
- ❓ **Câu hỏi kiểm tra Doc 8.2:** Trắc nghiệm lựa chọn widget trực quan hóa dữ liệu phù hợp (Gauge đo áp pin, biểu đồ chuỗi thời gian, mô hình 3D tư thế IMU, bản đồ quỹ đạo Ground Track).
- 📖 **Doc 8.3:** Thiết kế Sứ mệnh & Khung Mã nguồn cho 3 Đề tài Đồ án Capstone Thực chiến
- ❓ **Câu hỏi kiểm tra Doc 8.3:** Trắc nghiệm bài toán kỹ thuật của 3 đề tài sứ mệnh (hàng rào địa lý Geofencing cháy rừng, Store-and-Forward nông nghiệp IoT, chuyển tiếp phao cứu sinh LoRa).
- 🎥 **Video 8.2:** Xây dựng Giao diện Giám sát với Dashboard Builder qua Cổng Web Serial
- 💻 **Thực hành Đồ án Capstone:** `Lab8-01_Custom_Mission` - Triển khai khung mã nguồn chuẩn, tùy biến máy trạng thái, tích hợp cảm biến và thiết kế Dashboard hoàn chỉnh.
- ❓ **Câu hỏi kiểm tra Thực hành Đồ án Capstone:** Trắc nghiệm kiến trúc mã nguồn đồ án, thiết lập máy trạng thái nhiệm vụ, tối ưu hóa băng thông truyền tin và kiểm thử chức năng toàn hệ thống.
- 📝 **Tổng hợp Lab 8:** Hoàn tất đồ án Capstone, làm chủ toàn bộ quy trình thiết kế, lập trình và vận hành một sứ mệnh vệ tinh CubeSat độc lập.
