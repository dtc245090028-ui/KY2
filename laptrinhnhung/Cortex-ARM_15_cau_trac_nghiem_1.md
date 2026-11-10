# Cortex-ARM: trắc nghiệm kèm đáp án và cách giải (Đề 1 + bổ sung Đề 2)

> Ký hiệu: ✅ = đáp án đúng, ❌ = đáp án sai.
> Câu 1 là câu lý thuyết có thể khác theo cách thầy dạy, nên đối chiếu thêm với slide.
> Cuối file có phần **bổ sung Đề 2** (cùng bài "Bài kiểm tra tuần 1 – Lập trình nhúng", nhưng thứ tự câu và thứ tự đáp án A-D bị xáo trộn).

---

## Câu 1
**Đáp án nào sau đây đúng nhất khi mô tả về các thành phần bên trong lõi Cortex ARM?**

- A. ❌ Chứa 1 CPU ARM và hệ thống các thiết kế tiêu chuẩn
- B. ❌ Chứa 1 CPU ARM và hệ thống các thanh ghi
- C. ✅ Chứa 1 CPU ARM và bộ xử lý ngắt tiêu chuẩn và các ngoại vi
- D. ❌ Chứa 1 CPU ARM và hệ thống BUS tiêu chuẩn

**Ghi chú / cách giải:**
- Lõi Cortex-M không chỉ có CPU mà còn tích hợp sẵn bộ xử lý ngắt chuẩn (NVIC) và các khối ngoại vi lõi (SysTick, debug...).
- A, B, D mỗi đáp án chỉ nêu một phần hoặc nêu chung chung, không đủ ý "ngắt + ngoại vi".
- Đây là câu lý thuyết nên chọn C theo hướng "đầy đủ nhất". Nếu slide của thầy ghi khác thì theo slide.

---

## Câu 2
**Tập lệnh Thumb-2 dùng cho lõi vi điều khiển Cortex-ARM có mã lệnh bao nhiêu bít?**

- A. ❌ 8 bít
- B. ✅ Trộn lẫn giữa 32 bít và 16 bít
- C. ❌ 16 bít
- D. ❌ 32 bít

**Ghi chú / cách giải:**
- Thumb-2 là tập lệnh hỗn hợp: có lệnh 16 bít (gọn, tiết kiệm bộ nhớ) và lệnh 32 bít (mạnh hơn), chạy trộn lẫn với nhau.
- Thumb gốc chỉ có 16 bít, ARM gốc chỉ có 32 bít, nên C và D chỉ đúng một nửa.

---

## Câu 3
**Giá trị số 0x3FFC nên được lưu trong ô nhớ có kích thước bao nhiêu để tối ưu bộ nhớ?**

- A. ✅ 16 bít
- B. ❌ 8 bít
- C. ❌ 32 bít
- D. ❌ 64 bít

**Ghi chú / cách giải:**
- 0x3FFC = 0011 1111 1111 1100 (nhị phân) = 16380 (thập phân).
- 16380 > 255 nên 8 bít không đủ.
- 16380 < 65535 (0xFFFF) nên 16 bít là đủ.
- Chọn ô nhớ nhỏ nhất vẫn chứa được giá trị, tức 16 bít.

---

## Câu 4
**Khi chỉ tính toán với các giá trị số trong phạm vi từ 0-255 nên sử dụng ô nhớ có kích thước bao nhiêu để tối ưu bộ nhớ?**

- A. ❌ 10 bít
- B. ❌ 64 bít
- C. ✅ 8 bít
- D. ❌ 32 bít

**Ghi chú / cách giải:**
- 0 đến 255 gồm 256 giá trị = 2^8, nên đúng 8 bít.
- 10 bít không phải kích thước ô nhớ chuẩn. 32 và 64 bít đều lãng phí.

---

## Câu 5 (chọn 2 đáp án đúng)
**Khi thực hiện cộng hai giá trị trong ô nhớ M1, M2 rồi lưu kết quả vào M3 sử dụng cơ chế load and store thì các thao tác nào sau đây được thực hiện (chọn 2):**

- A. ✅ Cộng R1 và R3 lưu kết quả vào R4; Đưa R4 vào M3
- B. ❌ Đưa R1 vào M1; Đưa R3 vào M2
- C. ❌ Cộng M1 với M2 lưu kết quả vào M3; Đưa M4 vào R4
- D. ✅ Đưa M1 vào R1; Đưa M2 vào R3

**Ghi chú / cách giải:**
Cơ chế load and store: phép tính chỉ làm trên thanh ghi, bộ nhớ chỉ dùng để nạp (load) và cất (store).
1. **Load**: Đưa M1 vào R1, đưa M2 vào R3 (đáp án D).
2. **Tính**: Cộng R1 + R3, kết quả vào R4.
3. **Store**: Đưa R4 vào M3 (đáp án A).
- B sai vì đưa **từ thanh ghi vào bộ nhớ** M1, M2, ngược chiều và ghi đè dữ liệu gốc.
- C sai vì cộng trực tiếp trên ô nhớ (không đúng load/store) và có M4, R4 không liên quan.

---

## Câu 6
**Thứ tự các công đoạn thực hiện lệnh của một Pipeline trong lõi Cortex ARM là:**

- A. ❌ Xử lý ưu tiên lệnh, nhập lệnh, giải mã lệnh, thực thi lệnh
- B. ❌ Nhập lệnh, thực thi lệnh, giải mã lệnh
- C. ✅ Nhập lệnh, giải mã lệnh, thực thi lệnh
- D. ❌ Giải mã lệnh, thực thi lệnh

**Ghi chú / cách giải:**
- Pipeline cơ bản 3 giai đoạn: **Fetch (nhập lệnh) → Decode (giải mã) → Execute (thực thi)**.
- B sai thứ tự (thực thi trước giải mã). D thiếu bước nhập lệnh. A thêm bước "xử lý ưu tiên lệnh" không có trong pipeline.

---

## Câu 7
**Khi thực hiện phép toán cộng 20 + 50 thì những cặp thanh ghi nào trong CPU ARM có thể được sử dụng để lưu các toán hạng?**

- A. ✅ R1 và R3
- B. ❌ R3 và R14
- C. ❌ R2 và R15
- D. ❌ R4 và R13

**Ghi chú / cách giải:**
- R0 đến R12 là thanh ghi đa dụng, dùng chứa toán hạng được.
- R13 = SP (con trỏ ngăn xếp), R14 = LR (thanh ghi liên kết), R15 = PC (bộ đếm chương trình): là thanh ghi đặc biệt, không dùng chứa toán hạng.
- B có R14, C có R15, D có R13 nên đều sai. Chỉ A gồm hai thanh ghi đa dụng.

---

## Câu 8 (điền số)
**Biết rằng trong vi điều khiển Cortex ARM mỗi thao tác cất và lấy dữ liệu từ ngăn xếp mất 12 xung và thời gian chuyển liên tiếp giữa 2 chương trình con phục vụ ngắt là 6 xung.**

1) Nếu có 2 ngắt xảy ra liên tiếp và được xử lý theo cơ chế ngắt nối đuôi thì hệ thống tiết kiệm được **18** xung nhịp so với cơ chế xử lý ngắt thông thường.

2) Nếu có 3 ngắt xảy ra liên tiếp và được xử lý theo cơ chế ngắt nối đuôi thì hệ thống tiết kiệm được **36** xung nhịp so với cơ chế xử lý ngắt thông thường.

**Ghi chú / cách giải:**
Ngắt nối đuôi (tail-chaining) bỏ qua bước lấy dữ liệu (pop) rồi cất lại (push) giữa các ngắt liền nhau, chỉ mất 6 xung để chuyển.

- **Thông thường**: mỗi ngắt tốn cất 12 + lấy 12 = 24 xung.
- **Nối đuôi**: cất 12 (ngắt đầu) + 6 xung cho mỗi lần chuyển + lấy 12 (ngắt cuối).

Ý 1 (2 ngắt):
- Thông thường: 2 × 24 = 48
- Nối đuôi: 12 + 6 + 12 = 30
- Tiết kiệm: 48 − 30 = **18**

Ý 2 (3 ngắt):
- Thông thường: 3 × 24 = 72
- Nối đuôi: 12 + 6 + 6 + 12 = 36
- Tiết kiệm: 72 − 36 = **36**

---

## Câu 9
**Trong vi điều khiển Cortex ARM, biết rằng mỗi thao tác cất và lấy dữ liệu từ ngăn xếp mất 12 xung, thời gian chuyển liên tiếp giữa 2 chương trình con phục vụ ngắt là 6 xung, thời gian thực thi hai chương trình con phục vụ ngắt là 20 và 40 xung. Số chu kỳ máy cần thiết để vi điều khiển hoàn thành thực thi 2 chương trình con phục vụ ngắt trên sử dụng cơ chế ngắt nối đuôi là:**

- A. ❌ 66
- B. ❌ 84
- C. ❌ 60
- D. ✅ 90

**Ghi chú / cách giải:**
Tổng = cất (12) + ISR 1 (20) + chuyển (6) + ISR 2 (40) + lấy (12)
= 12 + 20 + 6 + 40 + 12 = **90 xung**.

(Tham khảo: nếu xử lý thông thường thì 2 × 24 + 20 + 40 = 108 xung, nối đuôi tiết kiệm đúng 18 xung như câu 8.)

---

## Câu 10
**Vùng nhớ Bit Band Region có kích thước 1MB thì kích thước của vùng nhớ Bit Band Alias trong không gian nhớ cho các ngoại vi là:**

- A. ❌ 32KB
- B. ✅ 32MB
- C. ❌ 31MB
- D. ❌ 4MB

**Ghi chú / cách giải:**
- 1MB = 2^20 byte = 2^20 × 8 = 2^23 bít.
- Mỗi bít ở Region ánh xạ thành **1 từ 4 byte** (32 bít) ở Alias.
- Kích thước Alias = 2^23 × 4 byte = 2^25 byte = **32MB**.
- Tức Alias luôn gấp 32 lần Region.

---

## Câu 11
**Cho biết chip xử lý trong hình thuộc loại lõi ARM Cortex loại nào?** (Hình: chip VORAGO VA10820-QFO, trên chip ghi "ARM Cortex-M0")

- A. ❌ Cortex-ARM
- B. ❌ Cortex-A
- C. ✅ Cortex-M
- D. ❌ Cortex-R

**Ghi chú / cách giải:**
- Trên thân chip in rõ dòng **ARM Cortex-M0**, M0 thuộc họ Cortex-M (vi điều khiển).
- Cortex-A dành cho ứng dụng cao cấp (điện thoại...), Cortex-R cho thời gian thực. "Cortex-ARM" không phải tên một dòng lõi.

---

## Câu 12
**Cho biết các chip xử lý Cortex R được mô tả như trong hình. Cho biết lõi Cortex loại R82 có thể hỗ trợ kích thước RAM tối đa là bao nhiêu?**

- A. ✅ 1TB
- B. ❌ 1GB
- C. ❌ 4GB
- D. ❌ 32GB

**Ghi chú / cách giải:**
Đọc bảng thông số, cột **Cortex-R82** (cột ngoài cùng bên phải):
- Architecture: Armv8-R AArch64
- **Address Bits: 40**
- **Addressable Memory: 1TB**

Kiểm tra: 2^40 byte = 1TB. Các cột R4, R5, R7, R8, R52, R52+ đều là 32 bít địa chỉ nên chỉ 4GB, đó là đáp án gây nhầm (C).

---

## Câu 13 (điền địa chỉ hệ hexa, chữ in hoa)
**Tính địa chỉ vật lý của từ trong vùng Bit Band Alias, biết:**
- Địa chỉ cơ sở vùng Bit Band Alias: 0x22000000
- Địa chỉ cơ sở vùng Bit Band Region: 0x20000000
- Địa chỉ offset của byte trong vùng Bit Band Region ánh xạ tới vùng bit band Alias là 0x00000025 với bít 4 là bít đang xem xét.

**Đáp án: `0x220004B0`**

**Cách giải:**

Công thức: **Alias = Base_Alias + (byte_offset × 32) + (bit × 4)**

- byte_offset × 32 = 0x25 × 32 = 37 × 32 = 1184 = **0x4A0**
- bit × 4 = 4 × 4 = 16 = **0x10**
- Alias = 0x22000000 + 0x4A0 + 0x10 = **0x220004B0**

---

## Câu 14 (điền địa chỉ hệ hexa, chữ in hoa)
**Tính địa chỉ vật lý của từ trong vùng Bit Band Alias, biết:**
- Địa chỉ cơ sở vùng Bit Band Alias: 0x42000000
- Địa chỉ cơ sở vùng Bit Band Region: 0x40000000
- Địa chỉ offset của byte trong vùng Bit Band Region ánh xạ tới vùng bit band Alias là 0x0000005C với bít 6 là bít đang xem xét.

**Đáp án: `0x42000B98`**

**Cách giải:**

- byte_offset × 32 = 0x5C × 32 = 92 × 32 = 2944 = **0xB80**
- bit × 4 = 6 × 4 = 24 = **0x18**
- Alias = 0x42000000 + 0xB80 + 0x18 = **0x42000B98**

---

## Câu 15 (điền địa chỉ hệ hexa, chữ in hoa)
**Tính địa chỉ vật lý của từ trong vùng Bit Band Alias, biết:**
- Địa chỉ cơ sở vùng Bit Band Alias: 0x42000000
- Địa chỉ cơ sở vùng Bit Band Region: 0x40000000
- Địa chỉ offset của byte trong vùng Bit Band Region ánh xạ tới vùng bit band Alias là 0x0000012D với bít 7 là bít đang xem xét.

**Đáp án: `0x420025BC`**

**Cách giải:**

- byte_offset × 32 = 0x12D × 32 = 301 × 32 = 9632 = **0x25A0**
- bit × 4 = 7 × 4 = 28 = **0x1C**
- Alias = 0x42000000 + 0x25A0 + 0x1C = **0x420025BC**

---

## Bảng đáp án nhanh

| Câu | Đáp án |
|---|---|
| 1 | C |
| 2 | B |
| 3 | A |
| 4 | C |
| 5 | A, D |
| 6 | C |
| 7 | A |
| 8 | 18 và 36 |
| 9 | D (90) |
| 10 | B (32MB) |
| 11 | C |
| 12 | A (1TB) |
| 13 | 0x220004B0 |
| 14 | 0x42000B98 |
| 15 | 0x420025BC |

## Ghi nhớ nhanh

- **Bit-band**: 1 bít Region ↔ 1 từ 4 byte Alias, Alias gấp 32 lần Region (1MB → 32MB).
- **Công thức Alias** = Base_Alias + byte_offset × 32 + bit × 4. Nhớ đổi sang hexa: ×32 tương đương dịch trái 5 bít, ×4 tương đương dịch trái 2 bít.
- **Ngắt nối đuôi**: cất 12 + (ISR + 6 chuyển) … + lấy 12, bỏ các cặp lấy/cất ở giữa.
- **Thanh ghi**: R0-R12 đa dụng, R13 = SP, R14 = LR, R15 = PC.


---
---

# BỔ SUNG ĐỀ 2 (Bài kiểm tra tuần 1 – Môn Lập trình nhúng)

> Đề 2 có nhiều câu trùng nội dung với Đề 1 nhưng **thứ tự đáp án A-D khác**, nên phải chọn theo nội dung chứ không theo chữ cái.
> Phần 1 là các câu **mới** (chưa có ở Đề 1). Phần 2 là bảng đối chiếu các câu trùng.

## PHẦN 1: Các câu mới

### Đề 2 – Câu 2
**Một hệ nhúng dùng vi điều khiển chạy hệ điều hành với các ứng dụng đồ họa cần sử dụng lõi Cortex loại:**

- A. ❌ Cortex-M
- B. ✅ Cortex-A
- C. ❌ Cortex-R
- D. ❌ Cortex-V

**Ghi chú / cách giải:**
- Chạy hệ điều hành đầy đủ (Linux, Android...) và ứng dụng đồ họa là nhóm **ứng dụng hiệu năng cao**, dùng **Cortex-A** (có MMU, hỗ trợ bộ nhớ ảo).
- Cortex-M dành cho vi điều khiển giá rẻ, tiết kiệm điện. Cortex-R dành cho hệ thời gian thực, độ tin cậy cao.
- Cortex-V không tồn tại.

---

### Đề 2 – Câu 3 (chọn 2 đáp án đúng)
**Câu nào đúng khi mô tả về Pipeline trong lõi Cortex ARM (chọn 2)?**

- A. ✅ Là phần cứng thực hiện các lệnh đơn hiệu quả
- B. ❌ Là phần mềm thực hiện các lệnh đơn hiệu quả
- C. ❌ Là phần cứng thực hiện các lệnh rẽ nhánh hiệu quả
- D. ✅ Gồm các công đoạn xử lý riêng biệt để tăng tốc hệ thống

**Ghi chú / cách giải:**
- Pipeline là **cơ chế phần cứng** chia việc thực hiện lệnh thành các công đoạn riêng (nhập lệnh, giải mã, thực thi) chạy gối đầu nhau, nhờ đó tăng tốc (đáp án D).
- Pipeline chạy hiệu quả với các **lệnh đơn, tuần tự** (đáp án A).
- B sai vì pipeline là phần cứng, không phải phần mềm.
- C sai vì lệnh rẽ nhánh làm phải xóa (flush) các lệnh đã nạp trước trong pipeline nên **không** hiệu quả.

---

### Đề 2 – Câu 5
**Các ưu điểm của tập lệnh Thumb-2 là:**

- A. ✅ Cho phép trộn lẫn các lệnh 32 bít và 16 bít
- B. ❌ Chỉ cho phép các lệnh 32 bít
- C. ❌ Chỉ cho phép các lệnh 16 bít
- D. ❌ Cho phép trộn lẫn các lệnh 8 bít

**Ghi chú / cách giải:**
- Thumb-2 kết hợp lệnh 16 bít (mã gọn, tiết kiệm bộ nhớ) và lệnh 32 bít (mạnh, nhanh) trong cùng một chương trình, không cần chuyển chế độ.
- B và C chỉ nêu một loại lệnh nên sai. Không có lệnh 8 bít trong Thumb-2 (D sai).

---

### Đề 2 – Câu 7
**Câu nào mô tả đúng về các thanh ghi trong lõi Cortex ARM?**

- A. ❌ R14 là thanh ghi con trỏ ngăn xếp
- B. ❌ R12 là thanh ghi liên kết
- C. ✅ R15 là thanh ghi bộ đếm chương trình
- D. ❌ R13 là thanh ghi bộ đếm chương trình

**Ghi chú / cách giải:**
- R13 = **SP** (con trỏ ngăn xếp), R14 = **LR** (thanh ghi liên kết), R15 = **PC** (bộ đếm chương trình).
- A sai (R14 là LR, không phải SP). B sai (R12 là thanh ghi đa dụng, không phải LR). D sai (R13 là SP, không phải PC).

---

### Đề 2 – Câu 10
**Mỗi bít trong không gian nhớ Bit Band Region tương ứng với bao nhiêu bít trong không gian nhớ Bit Band Alias?**

- A. ❌ 8 bít
- B. ✅ 32 bít
- C. ❌ 1 bít
- D. ❌ 16 bít

**Ghi chú / cách giải:**
- Mỗi bít ở Region ánh xạ tới **một từ 4 byte = 32 bít** ở Alias. Đây chính là lý do Alias lớn gấp 32 lần Region (1MB → 32MB).
- Trong từ 32 bít đó chỉ bít thấp nhất (bít 0) mang giá trị thật của bít cần truy cập, 31 bít còn lại không dùng. Đáp án C (1 bít) là bẫy dễ nhầm, vì đề hỏi kích thước vùng ánh xạ chứ không hỏi bít có nghĩa.

---

### Đề 2 – Câu 13 (điền địa chỉ hệ hexa, chữ in hoa)
**Tính địa chỉ vật lý của từ trong vùng Bit Band Alias, biết:**
- Địa chỉ cơ sở vùng Bit Band Alias: 0x22000000
- Địa chỉ cơ sở vùng Bit Band Region: 0x20000000
- Địa chỉ offset của byte trong vùng Bit Band Region ánh xạ tới vùng bit band Alias là 0x0000002C với bít 3 là bít đang xem xét.

**Đáp án: `0x2200058C`**

**Cách giải:**

Công thức: **Alias = Base_Alias + (byte_offset × 32) + (bit × 4)**

- byte_offset × 32 = 0x2C × 32 = 44 × 32 = 1408 = **0x580**
- bit × 4 = 3 × 4 = 12 = **0xC**
- Alias = 0x22000000 + 0x580 + 0xC = **0x2200058C**

---

## PHẦN 2: Đối chiếu các câu trùng với Đề 1 (thứ tự đáp án khác)

| Câu Đề 2 | Trùng với Đề 1 | Thứ tự đáp án trong Đề 2 | Đáp án đúng ở Đề 2 |
|---|---|---|---|
| Câu 1 | Câu 1 | A. Chứa 1 CPU ARM và hệ thống các thanh ghi / B. ... hệ thống các thiết kế tiêu chuẩn / C. ... bộ xử lý ngắt tiêu chuẩn và các ngoại vi / D. ... hệ thống BUS tiêu chuẩn | **C** |
| Câu 4 (chọn 2) | Câu 5 | A. Cộng M1 với M2 lưu vào M3; Đưa M4 và R4 / B. Cộng R1 và R3 lưu vào R4; Đưa R4 vào M3 / C. Đưa R1 và M1; Đưa R3 vào M2 / D. Đưa M1 vào R1; Đưa M2 vào R3 | **B và D** |
| Câu 6 | Câu 7 | A. R1 và R3 / B. R3 và R14 / C. R4 và R13 / D. R2 và R15 | **A** (R1 và R3) |
| Câu 8 | Câu 8 | Điền số, giống hệt | **18 và 36** |
| Câu 9 | Câu 9 | A. 84 / B. 90 / C. 60 / D. 66 | **B** (90) |
| Câu 11 | Câu 11 | A. Cortex-R / B. Cortex-ARM / C. Cortex-M / D. Cortex-A | **C** (Cortex-M) |
| Câu 14 | Câu 13 | Điền địa chỉ: Alias 0x22000000, offset 0x25, bít 4 | **0x220004B0** |
| Câu 15 | Câu 15 | Điền địa chỉ: Alias 0x42000000, offset 0x12D, bít 7 | **0x420025BC** |

Lưu ý: Đề 2 không có câu 12 (bảng thông số Cortex-R82) trong các ảnh đã gửi. Câu đó chỉ có ở Đề 1 (đáp án 1TB).

## Bảng đáp án nhanh Đề 2

| Câu | Đáp án |
|---|---|
| 1 | C |
| 2 | B (Cortex-A) |
| 3 | A, D |
| 4 | B, D |
| 5 | A |
| 6 | A |
| 7 | C |
| 8 | 18 và 36 |
| 9 | B (90) |
| 10 | B (32 bít) |
| 11 | C |
| 13 | 0x2200058C |
| 14 | 0x220004B0 |
| 15 | 0x420025BC |
