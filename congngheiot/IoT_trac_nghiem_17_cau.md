# Ôn tập trắc nghiệm IoT (18 câu)

Quy ước: ✅ là đáp án đúng. Mỗi câu có phần **Ghi chú** giải thích lý do.

---

## Câu 1
Cơ chế vận hành cốt lõi của một "vật" (Thing) trong hệ thống IoT là gì?

- A. Mỗi "vật" bắt buộc phải tích hợp màn hình hiển thị cảm ứng để người dùng nhập liệu.
- ✅ **B. Mỗi "vật" được cung cấp một định danh duy nhất (UID) và có khả năng truyền tải dữ liệu qua mạng mà không cần sự tương tác trực tiếp giữa người với người hoặc giữa người với máy tính.**
- C. Mỗi "vật" hoạt động hoàn toàn độc lập và không kết nối với bất kỳ hạ tầng mạng nào.
- D. Mỗi "vật" được điều khiển trực tiếp bằng tay thông qua cáp nối vật lý.

**Ghi chú:** IoT = thiết bị có định danh duy nhất (UID) và tự truyền dữ liệu qua mạng, không cần con người can thiệp trực tiếp. A, C, D đều trái với bản chất kết nối và tự động của IoT.

---

## Câu 2
Trong các đặc điểm cốt lõi của IoT, "Tính không đồng nhất" (Heterogeneity) được hiểu như thế nào?

- A. Số lượng thiết bị kết nối luôn ít hơn so với số lượng máy tính cá nhân.
- B. Tất cả thiết bị IoT đều sử dụng chung một chuẩn phần cứng và giao thức mạng giống hệt nhau.
- C. Trạng thái của thiết bị cố định và không bao giờ thay đổi.
- ✅ **D. Các thiết bị IoT sử dụng phần cứng, hệ điều hành và giao thức truyền thông hoàn toàn khác nhau nhưng vẫn có thể tương tác được với nhau.**

**Ghi chú:** Không đồng nhất = đa dạng về phần cứng, hệ điều hành, giao thức nhưng vẫn phối hợp được. B trái ngược hoàn toàn; A thuộc đặc điểm quy mô lớn; C thuộc đặc điểm thay đổi linh hoạt (và sai).

---

## Câu 3
Đặc điểm "Thay đổi linh hoạt" (Dynamic Changes) của hệ thống IoT thể hiện qua yếu tố nào?

- A. Vị trí vật lý của thiết bị luôn được cố định tuyệt đối.
- ✅ **B. Trạng thái của thiết bị có thể thay đổi liên tục (ngủ, thức, ngắt kết nối, di chuyển, thay đổi nhiệt độ...).**
- C. Băng thông truyền tải dữ liệu không bao giờ biến động.
- D. Dữ liệu do cảm biến thu thập luôn là một hằng số.

**Ghi chú:** "Dynamic" nghĩa là trạng thái, vị trí, ngữ cảnh của thiết bị thay đổi liên tục. Các đáp án A, C, D đều khẳng định "cố định/không đổi" nên sai.

---

## Câu 4
Thành phần nào sau đây thuộc Tầng 1 (Tầng thiết bị / Cảm biến) và đảm nhận vai trò thực thi các hành động phản hồi (như đóng/mở van nước, điều khiển động cơ, rơ-le)?

- A. Router Wi-Fi.
- ✅ **B. Cơ cấu chấp hành (Actuator).**
- C. Web Dashboard.
- D. Hệ quản trị cơ sở dữ liệu.

**Ghi chú:** Actuator là thành phần ở Tầng 1 thực thi hành động vật lý. Router Wi-Fi thuộc Tầng 2 (Gateway/Network), Web Dashboard thuộc Tầng 4 (Application), CSDL thuộc Tầng 3 (Management Service).

---

## Câu 5
Trong kịch bản tủ lạnh thông minh, khi một loại thực phẩm sắp hết, tủ lạnh tự động gửi thông báo cần nhập hàng trực tiếp đến siêu thị nhờ các sản phẩm được gắn mã ID. Quá trình này thể hiện rõ nhất đặc điểm cốt lõi nào của IoT?

- ✅ **A. Tính thông minh và tự động (Intelligence & Automation).**
- B. Tính quy mô lớn (Huge Scale).
- C. Tính kết nối thụ động.
- D. Tính không đồng nhất (Heterogeneity).

**Ghi chú:** Tủ lạnh tự nhận biết tình trạng và tự đặt hàng mà không cần người can thiệp, đó là thông minh và tự động. "Kết nối thụ động" không phải đặc điểm cốt lõi của IoT.

---

## Câu 6
Khi người dùng mở ứng dụng di động (Mobile App) trên điện thoại để theo dõi biểu đồ nhiệt độ phòng và nhấn nút bật điều hòa từ xa, người dùng đang tương tác trực tiếp với tầng nào trong kiến trúc IoT?

- A. Tầng 3 (Management Service Layer).
- B. Tầng 2 (Gateway and Network Layer).
- ✅ **C. Tầng 4 (Application Layer).**
- D. Tầng 1 (Devices/Sensors Layer).

**Ghi chú:** Tầng ứng dụng (Application Layer) là nơi người dùng tương tác trực tiếp qua Mobile App, Web Dashboard.

---

## Câu 7
Trong một hệ thống nhà thông minh, cảm biến phát hiện mở cửa và rơ-le tự động bật đèn khi có người bước vào lần lượt đóng vai trò là những thành phần nào tại Tầng 1?

- ✅ **A. Cảm biến cửa là Cảm biến (Sensor); Rơ-le là Bộ chấp hành (Actuator).**
- B. Cảm biến cửa là Bộ chấp hành (Actuator); Rơ-le là Cảm biến (Sensor).
- C. Cả hai thiết bị đều là Web Dashboard.
- D. Cả hai thiết bị đều là IoT Gateway.

**Ghi chú:** Cảm biến thu thập thông tin (phát hiện mở cửa), còn rơ-le thực thi hành động (bật đèn) nên là Actuator.

---

## Câu 8
Để thiết kế một nút cảm biến đo độ ẩm đất chạy bằng pin đặt trong rừng sâu cách trạm thu phát 8km, gửi dữ liệu định kỳ 15 phút/lần, kỹ sư lựa chọn chuẩn kết nối không dây Wi-Fi 5GHz để truyền dữ liệu trực tiếp về Server. Lựa chọn trên của kỹ sư là Đúng hay Sai?

- Đúng
- ✅ **Sai**

**Ghi chú:** Wi-Fi 5GHz chỉ phủ vài chục mét và tiêu thụ nhiều điện, không phù hợp với khoảng cách 8 km và chạy pin. Nên dùng LoRa/LoRaWAN hoặc NB-IoT (tầm xa, tiết kiệm điện, dữ liệu nhỏ gửi thưa).

---

## Câu 9
Trong một hệ thống theo dõi 100 nút cảm biến gửi dữ liệu nhiệt độ về Server theo chu kỳ 1 giây/lần, việc chọn giao thức HTTP POST sẽ tối ưu băng thông và giảm tải cho Server hơn so với giao thức MQTT. Việc lựa chọn như vậy Đúng hay Sai?

- Đúng
- ✅ **Sai**

**Ghi chú:** HTTP có header nặng và mỗi lần gửi là một request riêng. MQTT (Publish/Subscribe, kết nối duy trì, header tối thiểu 2 byte) nhẹ hơn, tiết kiệm băng thông và giảm tải Server tốt hơn trong kịch bản nhiều nút gửi dày.

---

## Câu 10
Trong mạng Zigbee dạng lưới (Mesh Topology) gồm 1 Gateway và 20 nút Router, nếu 1 nút Router ở giữa mạng bị hỏng nguồn, toàn bộ các nút Router nằm phía sau nó sẽ vĩnh viễn mất kết nối và không thể gửi dữ liệu về Gateway được nữa. Nhận định này về mạng Zigbee Mesh Sai hay Đúng?

- Đúng
- ✅ **Sai**

**Ghi chú:** Mạng Mesh có khả năng tự định tuyến lại (self-healing). Khi một Router hỏng, các nút phía sau tìm đường khác qua các Router lân cận để về Gateway, nên không bị mất kết nối vĩnh viễn.

---

## Câu 11 (chọn 2 đáp án)
Trong một trạm đo môi trường, bo mạch ESP8266 bị khởi động lại (Reset) liên tục ngay tại thời điểm kích hoạt kết nối Wi-Fi để gửi dữ liệu. Hai phân tích nguyên nhân và giải pháp phần cứng nào sau đây là chuẩn xác nhất?

- ✅ **A. Khắc phục bằng cách sử dụng bộ nguồn có dòng ra đủ lớn (1A - 2A) và gắn thêm tụ hóa dung lượng lớn (lớn hơn 470µF) song song ở chân cấp nguồn VCC/GND gần ESP.**
- B. Khắc phục bằng cách tháo bỏ hoàn toàn anten vô tuyến để làm giảm công suất tiêu thụ điện của khối RF trên ESP.
- ✅ **C. Khi khối RF Wi-Fi kích hoạt phát sóng đòi hỏi dòng đỉnh (Peak Current) lớn; nếu nguồn cấp không đáp ứng đủ sẽ làm sụt áp VCC gây ra hiện tượng Reset vi điều khiển.**
- D. Hiện tượng Reset xảy ra do giao thức MQTT quá nặng gây tràn bộ nhớ RAM của vi điều khiển ESP8266.

**Ghi chú:** Nguyên nhân là dòng đỉnh của khối RF làm sụt áp VCC (C), cách khắc phục là nguồn đủ dòng và tụ lớn lọc nguồn (A). B sai vì tháo anten không giải quyết sụt áp. D sai vì đây là lỗi phần cứng nguồn, không phải tràn RAM.

---

## Câu 12 (chọn 2 đáp án)
Để xây dựng trạm Gateway truyền thông xa, kỹ sư đấu nối bo mạch ESP32 với module truyền thông LoRa Ai-Thinker Ra-02 (chip SX1278). Hai phát biểu nào sau đây mô tả đúng về mặt giao tiếp phần cứng giữa hai thiết bị này?

- A. Bắt buộc phải sử dụng mạch chuyển mức logic 5V sang 3.3V cho tất cả các chân giao tiếp giữa ESP32 và module LoRa Ra-02.
- ✅ **B. Cả ESP32 và module LoRa SX1278 đều vận hành ở mức điện áp logic 3.3V, do đó có thể nối trực tiếp các chân tín hiệu dữ liệu với nhau mà không cần mạch chuyển mức logic.**
- ✅ **C. Module LoRa Ra-02 trao đổi dữ liệu tốc độ cao với ESP32 thông qua chuẩn giao tiếp nối tiếp SPI (với các chân MOSI, MISO, SCK, CS).**
- D. Module LoRa Ra-02 truyền nhận dữ liệu với ESP32 qua kết nối không dây Bluetooth BLE nên không cần đấu nối cáp tín hiệu data.

**Ghi chú:** Cả hai cùng mức 3.3V nên nối thẳng được (B), và Ra-02 giao tiếp với ESP32 qua SPI (C). A sai vì không cần chuyển mức. D sai vì LoRa không dùng BLE, vẫn phải đấu dây SPI.

---

## Câu 13 (chọn 2 đáp án)
Một hệ thống giám sát nhiệt độ xưởng sản xuất dùng ESP32 yêu cầu: Khi nhiệt độ vượt 60°C, ESP32 phải gửi ngay cảnh báo về máy chủ Cloud và nhận lệnh phản hồi để bật rơ-le còi báo động. Hai lý do kỹ thuật nào sau đây giải thích vì sao giao thức MQTT là lựa chọn tối ưu hơn HTTP REST cho bài toán này trên ESP32?

- A. MQTT cho phép ESP32 truyền trực tiếp các luồng video HD từ camera an ninh về Server mà không tốn băng thông mạng.
- ✅ **B. MQTT hỗ trợ các mức quản lý chất lượng dịch vụ (QoS), đảm bảo thông điệp cảnh báo hoặc lệnh điều khiển còi báo động không bị thất lạc trong quá trình truyền.**
- C. MQTT là giao thức hoạt động không cần máy chủ trung gian (Broker), các thiết bị ESP32 tự tìm thấy và kết nối trực tiếp với nhau.
- ✅ **D. MQTT hoạt động theo mô hình Publish/Subscribe trên nền kết nối duy trì liên tục, tiêu đề gói tin cực nhỏ (tối thiểu 2 bytes), giúp truyền tin cảnh báo với độ trễ siêu thấp.**

**Ghi chú:** QoS đảm bảo tin cảnh báo/lệnh không mất (B); Publish/Subscribe, kết nối duy trì và header nhỏ cho độ trễ thấp (D). A sai vì MQTT không dành cho video HD. C sai vì MQTT bắt buộc có Broker làm trung gian.

---

## Câu 14 (ghép đôi)
Hãy ghép từng hiện tượng lỗi của hệ thống IoT với nguyên nhân kỹ thuật tương ứng.

**Các nguyên nhân kỹ thuật:**
1. Cấu hình MQTT với QoS Level = 0 và Clean Session = true nên gói tin bị hủy khi mất kết nối.
2. Lập trình chưa đưa vi điều khiển vào chế độ Deep Sleep sau khi gửi dữ liệu.
3. Nguồn cấp không đáp ứng đủ dòng đỉnh (Peak Current) khi khối RF hoạt động.
4. Chân dữ liệu lệch mức logic (5V nối thẳng vào 3.3V) gây tràn dòng/hỏng vi mạch I/O.

**Các hiện tượng lỗi:**
- (a) Ứng dụng di động không nhận được dữ liệu cảm biến phát ra trong khoảng thời gian bị mất mạng tạm thời.
- (b) Bo mạch ESP8266 bị sụt áp và Reset liên tục mỗi khi bật Wi-Fi truyền dữ liệu.
- (c) Nút cảm biến dùng pin lithium 2000mAh bị hết sạch pin chỉ sau 3 ngày hoạt động.
- (d) Module Zigbee CC2530 bị nóng bất thường và hỏng cổng UART sau khi cắm vào Arduino Uno.

**Đáp án ghép đúng:**
- ✅ (a) ↔ nguyên nhân 1 (QoS 0 + Clean Session = true)
- ✅ (b) ↔ nguyên nhân 3 (nguồn không đủ dòng đỉnh)
- ✅ (c) ↔ nguyên nhân 2 (chưa dùng Deep Sleep)
- ✅ (d) ↔ nguyên nhân 4 (5V nối thẳng vào 3.3V)

**Ghi chú:**
- (a) QoS 0 gửi một lần không xác nhận và Clean Session = true xóa phiên khi mất kết nối, nên tin phát lúc mất mạng bị mất.
- (b) Khối RF cần dòng đỉnh lớn, nguồn yếu gây sụt áp và reset.
- (c) Không dùng Deep Sleep thì vi điều khiển chạy liên tục, pin cạn rất nhanh.
- (d) CC2530 chạy logic 3.3V, nối thẳng với I/O 5V của Arduino Uno gây quá áp, nóng và hỏng chân.

---

## Câu 15 (chọn 2 đáp án)
Trong bài thực hành kết nối bo mạch Arduino Uno (điện áp I/O 5V) với module Wi-Fi ESP-12E (điện áp I/O 3.3V) qua giao tiếp nối tiếp UART để gửi dữ liệu cảm biến lên Server. Hai thao tác ghép nối phần cứng nào sau đây là đúng kỹ thuật để vừa đảm bảo an toàn phần cứng vừa truyền được dữ liệu?

- ✅ **A. Chân TX của ESP-12E (xuất mức 3.3V) có thể đấu trực tiếp vào chân RX của Arduino Uno (5V) vì điện áp 3.3V được Arduino Uno nhận diện là mức logic HIGH hợp lệ.**
- B. Đấu nối một điện trở kéo lên (Pull-up) 10kΩ từ chân RX của ESP-12E lên đường nguồn 5V để tăng cường tín hiệu UART.
- ✅ **C. Chân TX của Arduino Uno (xuất mức 5V) phải đấu nối qua mạch phân áp điện trở (hoặc IC chuyển mức logic 5V sang 3.3V) trước khi đi vào chân RX của ESP-12E.**
- D. Đấu nối trực tiếp chân nguồn 5V của Arduino Uno vào chân VCC của ESP-12E mà không qua IC hạ áp 3.3V.

**Ghi chú:** Hướng 3.3V → 5V (ESP TX → Arduino RX) nối thẳng được vì 3.3V vẫn đủ nhận là HIGH (A). Hướng 5V → 3.3V (Arduino TX → ESP RX) phải hạ áp bằng phân áp hoặc IC chuyển mức (C). B sai vì kéo lên 5V làm quá áp chân ESP. D sai vì ESP-12E chỉ chịu 3.3V, cấp 5V sẽ hỏng module.

---

## Câu 16 (chọn 2 đáp án)
Nhóm sinh viên thực hành bài tập đo mức chất lỏng trong bể chứa bằng cảm biến siêu âm HC-SR04 (vận hành nguồn 5V) kết nối với vi điều khiển ESP32 (mức logic I/O 3.3V). Hai phát biểu nào sau đây mô tả đúng nguyên lý vận hành và cách đấu nối chân tín hiệu Echo an toàn?

- ✅ **A. Cảm biến xác định khoảng cách dựa trên việc đo thời gian phản xạ (Time of Flight) của sóng âm tần số cao từ đầu phát đến bề mặt chất lỏng và dội về đầu thu.**
- ✅ **B. Do chân Echo của cảm biến HC-SR04 xuất xung logic 5V, nhóm thực hành phải gắn mạch phân áp điện trở trên đường tín hiệu Echo trước khi đưa vào chân GPIO của ESP32.**
- C. Cảm biến siêu âm đo khoảng cách bằng cách phân tích sự thay đổi cường độ ánh sáng chiếu vuông góc xuống mặt chất lỏng.
- D. Chân Echo của cảm biến HC-SR04 xuất ra điện áp tuyến tính Analog (0V - 5V) nên bắt buộc phải đấu vào chân ADC của ESP32 mà không qua phân áp.

**Ghi chú:** HC-SR04 đo thời gian sóng âm đi và về (Time of Flight) (A), và chân Echo xuất xung số 5V nên phải phân áp trước khi vào GPIO 3.3V của ESP32 (B). C sai vì dùng sóng âm, không dùng ánh sáng. D sai vì Echo là xung số, không phải tín hiệu Analog.

---

## Câu 17
Trong thực hành ghép nối bo mạch vi điều khiển ESP32 (mức logic 3.3V) với cảm biến công nghiệp xuất tín hiệu UART ở mức logic 5V, để truyền nhận tín hiệu hai chiều an toàn mà không làm quá áp gây hỏng các chân GPIO của ESP32, mạch điện tử chuyên dụng được sử dụng là gì?

- ✅ **Mạch chuyển đổi mức logic (Logic Level Converter)**
- Mạch cầu H (H-Bridge)
- Mạch khuếch đại thuật toán (Op-Amp)
- Mạch chỉnh lưu cầu (Bridge Rectifier)

**Ghi chú:** Mạch chuyển đổi mức logic (loại hai chiều) dịch qua lại giữa 3.3V và 5V. Cầu H dùng điều khiển động cơ, Op-Amp dùng khuếch đại tín hiệu analog, mạch chỉnh lưu cầu dùng đổi AC sang DC.

---

## Câu 18
Việc phân tích và xử lý dữ liệu thô ngay tại biên (Edge Computing) ở Tầng 3 nhằm mục đích chính nào?

- A. Loại bỏ nhu cầu sử dụng các cảm biến ở Tầng 1.
- B. Tăng kích thước gói tin khi truyền trên mạng diện rộng.
- ✅ **C. Giảm độ trễ xử lý và tối ưu hóa trước khi dữ liệu được gửi về trung tâm dữ liệu.**
- D. Thay thế hoàn toàn màn hình hiển thị của ứng dụng di động.

**Ghi chú:** Edge Computing xử lý dữ liệu gần nguồn phát sinh, nên giảm độ trễ và giảm lượng dữ liệu phải đẩy về trung tâm dữ liệu/Cloud. A sai vì vẫn cần cảm biến để thu thập dữ liệu. B sai vì edge giúp giảm, không tăng, dữ liệu truyền. D sai vì không liên quan đến màn hình ứng dụng.
