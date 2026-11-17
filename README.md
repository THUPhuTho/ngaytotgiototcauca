# NGƯ THỜI QUANG (FishCast Bắc Bộ v2.0)
### Ứng Dụng Dự Báo Thời Điểm Cá Ăn Thời Gian Thực Dựa Trên Chiêm Tinh & Khí Tượng Miền Bắc

---

## 🌊 1. Giới Thiệu
**Ngư Thời Quang** là ứng dụng web thời gian thực chuyên sâu dành riêng cho cần thủ khu vực **Miền Bắc Việt Nam**. Ứng dụng kết hợp giữa:
1. **Thuật Chiêm Tinh Học & Lịch Vạn Niên Cổ Truyền**: Lịch âm GMT+7 (thuật toán GS Hồ Ngọc Đức), Can Chi ngày/tháng/năm, Ngũ Hành nạp âm, 12 Trực ngày, Nhị thập bát tú, Giờ Hoàng Đạo xuất hành và Hướng Hỷ Thần / Tài Thần.
2. **Thuyết Nhật Nguyệt (Solunar Theory)**: Xác định 4 khung giờ cá ăn vàng trong ngày (2 khung Major và 2 khung Minor) dựa trên vị trí Mặt Trăng và lực hấp dẫn thủy triều.
3. **Khí Tượng Học Thời Gian Thực Miền Bắc**: Kết nối trực tiếp Open-Meteo High-Resolution API để phân tích Áp suất khí quyển (hPa), Hướng & Tốc độ gió (gió Nồm Đông Nam, gió Bấc Đông Bắc, gió Lào), Nhiệt độ không khí & mặt nước, Độ ẩm.

---

## 🚀 2. Cách Khởi Chạy Ứng Dụng
Ứng dụng được thiết kế hoàn toàn **Standalone & Client-side**, không yêu cầu cài đặt server hay backend.

### Cách 1: Mở trực tiếp trên trình duyệt máy tính
1. Truy cập thư mục: `C:\Users\phuth\.gemini\antigravity\scratch\vietnam-fishing-realtime\`
2. Nhấp đúp vào file `index.html` để mở trong Google Chrome, Microsoft Edge, Cốc Cốc hoặc Safari.

### Cách 2: Sử dụng trên Điện Thoại (Smartphone)
1. Bạn có thể mở file `index.html` hoặc đưa lên bất kỳ hosting miễn phí nào (GitHub Pages, Vercel, Netlify).
2. Chọn **"Thêm vào Màn hình chính" (Add to Home Screen)** trên Safari (iOS) hoặc Chrome (Android) để sử dụng như một App di động toàn màn hình.

---

## 🧭 3. Cơ Sở Thuật Toán 5 Trụ Cột

| Trụ Cột | Trọng Số | Nguyên Lý & Tác Động Lên Cá Miền Bắc |
| :--- | :---: | :--- |
| **Áp Suất Khí Quyển (Barometer)** | **30%** | **Yếu tố sống còn của cần thủ**: Áp suất lý tưởng là `1011 - 1017 hPa`. Bong bóng bơi của cá thích nghi hoàn hảo, cá tích cực bơi lội sục bùn kiếm mồi. Khi áp suất tụt mạnh trước cơn dông, cá ăn đón nước cực dữ trong 1-2h trước khi bão ập xuống. |
| **Thuyết Solunar & Pha Trăng** | **25%** | **Khung giờ ăn chính (Major)** khi Mặt trăng ở Thiên đỉnh (Overhead) hoặc Chân thiên đỉnh (Underfoot). **Khung giờ ăn phụ (Minor)** lúc Trăng mọc/lặn. Ngày Mùng 1 (Trăng non) và Ngày Rằm (Trăng tròn) lực triều cực đại kích thích cá ăn mạnh nhất. |
| **Gió & Mặt Sóng Hồ** | **20%** | Tốc độ `6 - 17 km/h` (Cấp 2 - 3) tạo gợn sóng lăn tăn làm tán sắc ánh sáng, cá mất cảnh giác và lượng oxy hòa tan dồi dào. Gió **Đông Nam (Nồm ẩm)** là gió vàng; gió **Đông Bắc (Bấc lạnh)** làm cá tụt đáy. |
| **Nhiệt Độ Sinh Thái** | **15%** | `20°C - 28°C` là dải nhiệt độ vàng của hệ cá nước ngọt Bắc Bộ (Chép, Trắm, Rô phi, Trôi). Dưới `14°C` (rét hại) cá ngậm miệng; trên `35°C` (nắng hè) cá trốn đáy sâu hoặc chỉ ăn đêm. |
| **Chiêm Tinh & Bát Trạch** | **10%** | Tra cứu **Giờ Hoàng Đạo** xuất hành giúp cần thủ đón vượng khí. Ngày rơi vào **Trực Mãn, Trực Khai, Trực Định, Trực Thành** sông nước hanh thông, cá dính lưỡi bền chặt. Hướng Hỷ Thần / Tài Thần giúp chọn vị trí buông cần đón lộc. |

---

## 🎯 4. Cẩm Nang Loài Cá Miền Bắc
- **Cá Chép Sông & Hồ**: Đáy bùn non (1.8m - 2.8m). Mồi khoai lang ủ lên men, ngũ cốc thơm ngọt. Nhạy nhất khi áp suất ổn định.
- **Cá Trắm Đen (Săn Củ)**: Đáy sâu (3.0m - 5.5m). Mồi ốc vặn đập dập ủ tỏi ớt, cua đồng. Khung giờ vàng: Major ban đêm lúc tĩnh mịch.
- **Cá Trắm Cỏ**: Tầng lửng đến tầng đáy. Mồi lá sắn, ngọn cỏ non, ngô ngọt luộc mật ong. Rất thích gió Đông Nam gợn sóng lăn tăn.
- **Cá Rô Phi / Diêu Hồng**: Thích nắng ấm 25-30°C, sóng vỗ bờ tạo bọt khí oxy. Mồi cám tôm tanh, nhộng tằm xay.
- **Cá Trôi (Trôi Ấn, Trôi Đỏ)**: Đáy phẳng, chân kè đá. Mồi chua thối lên men. Nhạy vào xế chiều mùa thu đông.
- **Cá Lăng, Nheo (Hồ Sông Đà, Thác Bà)**: Thích bóng tối, hốc đá sâu 4-7m, mồi tanh sống hoặc cá con băm nhỏ.

---

## 📍 5. Địa Điểm Tích Hợp Sẵn Tọa Độ GPS
- **Hà Nội**: Hồ Tây, Sông Hồng, Sông Đuống, Hồ Đồng Mô, Hồ Suối Hai.
- **Hòa Bình**: Lòng Hồ Sông Đà (Thủ phủ săn Trắm Đen, Cá Lăng).
- **Yên Bái**: Hồ Thác Bà.
- **Phú Thọ**: Đầm Ao Châu, Sông Lô.
- **Hải Phòng**: Sông Cấm, Đồ Sơn, Cửa Sông Bạch Đằng.
- **Quảng Ninh**: Hồ Yên Lập, Vịnh Hạ Long.
- **Ninh Bình**: Đầm Vân Long, Sông Đáy.
- **Nam Định / Thái Bình**: Hạ lưu Sông Hồng, Sông Đào.
- **Bắc Ninh / Bắc Giang**: Sông Cầu, Hồ Cấm Sơn.
- **Vĩnh Phúc**: Hồ Đại Lải, Hồ Xạ Hương.
- **Nút GPS Tự Động**: Tự động nhận diện tọa độ thực tế nơi bạn đang đứng buông cần.

---
*Chúc các cần thủ Bắc Bộ chuyến đi đại thắng, đầy giỏ, bắt được cá củ!* 🎣
