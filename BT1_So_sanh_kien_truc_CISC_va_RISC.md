# BT1  
## SO SÁNH KIẾN TRÚC CISC VÀ RISC

### 1. Giới thiệu

Trong lĩnh vực thiết kế vi xử lý, người ta thường nhắc đến hai hướng kiến trúc chính là **CISC (Complex Instruction Set Computer)** và **RISC (Reduced Instruction Set Computer)**. Đây là hai cách tiếp cận khác nhau trong việc thiết kế tập lệnh của bộ xử lý – phần "bộ não" điều khiển hoạt động của máy tính.

**CISC** được phát triển trước, với mục tiêu là giúp việc lập trình dễ hơn bằng cách tạo ra nhiều lệnh phức tạp. Mỗi lệnh trong CISC có thể thực hiện được nhiều thao tác cùng lúc, ví dụ như lấy dữ liệu từ bộ nhớ, xử lý rồi lưu lại.  

**RISC** ra đời sau, đi theo hướng ngược lại: giảm bớt độ phức tạp, chỉ giữ lại những lệnh cơ bản nhất, nhưng tối ưu để mỗi lệnh thực hiện rất nhanh – thường chỉ trong một chu kỳ xung nhịp. Tư tưởng của RISC là **đơn giản để nhanh hơn**.

---

### 2. Ưu và nhược điểm của từng kiến trúc

#### 2.1. CISC
**Ưu điểm:**
- Có nhiều loại lệnh, nên viết chương trình ở mức thấp (assembly) dễ hơn.
- Một lệnh có thể làm nhiều việc, nhờ đó chương trình thường ngắn hơn.
- Phù hợp với máy tính cá nhân và hệ thống cần tương thích với phần mềm cũ.

**Nhược điểm:**
- Cấu trúc phần cứng phức tạp, khó thiết kế và khó tăng tốc pipeline.
- Mỗi lệnh thường cần nhiều chu kỳ xung nhịp để hoàn thành → tốc độ xử lý chậm hơn.
- Tốn năng lượng, không thích hợp với thiết bị di động hoặc nhúng.

#### 2.2. RISC
**Ưu điểm:**
- Cấu trúc lệnh đơn giản → xử lý nhanh, dễ tối ưu pipeline.
- Hầu hết các lệnh thực hiện trong một chu kỳ xung nhịp.
- Tốn ít năng lượng hơn, phù hợp với các hệ thống nhúng, điện thoại, IoT.
- Thiết kế CPU đơn giản, dễ mở rộng và cải tiến.

**Nhược điểm:**
- Cần nhiều lệnh hơn để làm cùng một công việc so với CISC → chương trình dài hơn.
- Đòi hỏi trình biên dịch phải thông minh để tối ưu mã.
- Ít tương thích với các phần mềm cũ dựa trên kiến trúc CISC.

---

### 3. So sánh giữa CISC và RISC

| Tiêu chí | CISC | RISC |
|-----------|------|------|
| **Cấu trúc tập lệnh** | Tập lệnh nhiều và phức tạp, độ dài lệnh không cố định | Tập lệnh ít, độ dài cố định, mỗi lệnh thực hiện một thao tác nhỏ |
| **Tốc độ xử lý** | Chậm hơn, cần nhiều chu kỳ cho mỗi lệnh | Nhanh hơn, mỗi lệnh thường chỉ 1 chu kỳ |
| **Kích thước chương trình** | Ngắn hơn | Dài hơn do cần nhiều lệnh hơn |
| **Độ phức tạp phần cứng** | Phức tạp, nhiều vi mạch điều khiển | Đơn giản, dễ tối ưu và mở rộng |
| **Ứng dụng thực tế** | Dùng trong CPU Intel, AMD – phổ biến trên PC, laptop | Dùng trong ARM, MIPS, RISC-V – phổ biến trên điện thoại, nhúng, IoT |

**Ví dụ thực tế:**
- **CISC**: Các bộ xử lý Intel Core, AMD Ryzen sử dụng kiến trúc x86.  
- **RISC**: Dòng chip ARM Cortex (trên điện thoại, máy tính bảng, Raspberry Pi) hoặc RISC-V (dùng nhiều trong IoT, nghiên cứu và thiết bị nhỏ gọn).

---

### 4. Nhận xét và kết luận

Theo quan điểm của tôi, trong bối cảnh hiện nay – khi **các hệ thống nhúng và thiết bị di động phát triển mạnh** – thì **RISC phù hợp hơn**.  

Lý do là:
1. **Tiết kiệm điện năng**, giúp kéo dài thời gian sử dụng pin – yếu tố quan trọng trong IoT và thiết bị cầm tay.  
2. **Tốc độ xử lý cao**, nhờ mỗi lệnh đơn giản và được thực thi nhanh.  
3. **Thiết kế phần cứng dễ mở rộng**, thuận lợi cho các công ty nhỏ hoặc startup phát triển chip riêng.  
4. **Cộng đồng phát triển mạnh**, đặc biệt với **RISC-V mã nguồn mở**, giúp giảm chi phí nghiên cứu và sản xuất.

Tuy nhiên, kiến trúc **CISC** vẫn chiếm ưu thế trong máy tính để bàn và máy chủ – nơi cần khả năng tương thích phần mềm và xử lý các tác vụ phức tạp.  

Tóm lại, **CISC** và **RISC** là hai hướng thiết kế khác nhau, mỗi bên có thế mạnh riêng.  
CISC tập trung vào sự linh hoạt và tương thích phần mềm, còn RISC chú trọng hiệu năng, năng lượng và sự đơn giản.  

Trong tương lai, khi xu hướng điện toán di động, IoT và AI biên (Edge AI) tiếp tục phát triển, **RISC – đặc biệt là ARM và RISC-V – sẽ là lựa chọn tối ưu** cho các hệ thống nhúng và thiết bị nhỏ gọn.