<h1 align="center">PHÁT HIỆN VÀ KHOANH VÙNG KHỐI U NÃO TRONG ẢNH MRI </h1>

<div align="center">

<p align="center">
  <img src="logoDaiNam.png" alt="DaiNam University Logo" width="200"/>
  <img src="LogoAIoTLab.png" alt="DaiNam University Logo" width="150"/>


</p>

[![Made by AIoTLab](https://img.shields.io/badge/Made%20by%20AIoTLab-blue?style=for-the-badge)](https://www.facebook.com/DNUAIoTLab)
[![Fit DNU](https://img.shields.io/badge/Fit%20DNU-green?style=for-the-badge)](https://fitdnu.net/)
[![DaiNam University](https://img.shields.io/badge/DaiNam%20University-red?style=for-the-badge)](https://dainam.edu.vn)

</div>

<h2 align="center">Phát hiện và khoanh vùng u não trong ảnh MRI bằng mô hình U-Net</h2>

<p align="left">
  Phát hiện và khoanh vùng những nơi u não tồn tại trong ảnh MRI của não. Sử dụng mô hình U-Net trong quá trình phát hiện và khoanh vùng những nơi não xuất hiện những điểm lạ hoặc bất thường nghi vấn đó là u não. Mô hình U-Net giúp nhận diện những vùng u não một cách tương đối chính xác ngoài ra còn giúp phát hiện những vùng tuyến yên sau não có tổn thương từ đó giúp việc chữa trị và chuẩn đoán u não dễ dàng hơn cho bác sĩ đồng thời giảm chi phí chuẩn đoán.
</p>

---

## 🌟 Giới thiệu

- **📌 Giúp chuẩn đoán các khối u thông qua ảnh MRI của não
- **💡 Theo dõi sự phát triển của khối u 
- **📊 Việc phát hiện có thể không đúng hoặc xảy ra lỗi trong quá trình phân tích
---
## 🏗️ HỆ THỐNG
<p align="center">
  <img src="Screenshot 2025-03-11 095146.png" alt="System Architecture" width="800"/>
</p>

---
## 📂 Cấu trúc dự án

📦 Project  
├── 📂 Labeled  # Thư mục chứa dữ liệu

│  │  ├──📂Traning ├── 📂 Images #Thư mục chứa ảnh

                    ├── 📂Labels  #Thư mục chứa nhãn
      
      ├──📂Testing ├── 📂 Images
      │             ├── 📂Labels
      
      │
      ├──📂Valid ├── 📂 Images
                  ├── 📂Labels
├── 📂 Nhom10-BTL #Thư mục chứa bài thuyết trình PowerPoint

|── 📂KhoanhVungUNao_U_Net #Thư mục chưa file code
---

## 🛠️ Yêu cầu hệ thống
- Sử dụng mô hình U-Net để xây dựng model
- Sử dụng colab để chạy code giúp quá trình diễn ra nhanh hơn (nếu máy đủ khỏe có thể sử dụng visual studio code)


## Các bước thực hiện
## Bước 1: Kết nối với Drive để lấy dữ liệu
- Dữ liệu đã được thu thập từ trước ở trên kaggle và được up lên drive, dữ liệu gồm ba thư mục chính là tranining, testing và valid. Mỗi thư mục sẽ gồm hai thư mục con là images và labels.

## Bước 2: Hàm tạo mask cho ảnh
- Cài đặt kích thước ảnh đầu vào với 256x256 pixel
- Tạo hàm để tạo mask cho ảnh từ file labels, do file này dẽ được lưu trữ dưới file text.
  <p align="center">
  <img src="Screenshot 2025-03-18 134334.png" alt="System Architectur" width="400"/>
</p>

## Bước 3: Load toàn bộ dữ liệu 
- Ta load toàn bộ dữ liệu trong file chứa dataset.

## Bước 4: Giảm kích thước dữ liệu
- Nếu máy đủ khỏe ta có thể cho toàn bộ dữ liệu vào training. Nếu muốn quá trình traninng diễn ra nhanh hơn ta có thể giảm kích thước dữ liệu vào để có thể traning nhanh hơn.

## Bước 5: Xây dựng mô hình U-Net
- Xây dựng một mô hình U-Net và xây dựng mô hình phù hợp với quá trình phát hiện và khoanh vùng u não.

## Bước 6: Training mô hình
- Sau khi xây dựng xong mô hình U-Net, ta sẽ cho dữ liệu vào training. Quá trinhg traning sẽ chạy với 50 epoch để quá trình training đạt được kết quả như mong muốn.
 
## Bước 7: Xây dựng hàm xuất hình ảnh kết quả ra màn hình
- Sau khi training xây dựng một hàm để xuất kết quả ra màn hình. Từ đó giúp quan sát được kết quả mô hình chạy và huấn luyện.
  <p align="center">
  <img src="Screenshot 2025-03-10 230657.png" alt="System Architectur" width="650"/>
</p>
  
## 🤝 Đóng góp
Dự án được phát triển bởi 3 thành viên:

| Họ và Tên        | Vai trò                  |
|------------------|--------------------------|
| Dương Văn Việt   | Tìm kiếm dataset, xây dựng mô hình U-Net, tìm kiếm mã nguồn, triển khai và thực hiện báo cáo và dự án, làm powerpoitn, overleaf.|
| Lê Anh Ngọc      | Hỗ trợ bài tập lớn.      |
| Nguyễn Mạnh Tuân | Hỗ trợ bài tập lớn.      |

© 2025 NHÓM 10, CNTT17-15, TRƯỜNG ĐẠI HỌC ĐẠI NAM
