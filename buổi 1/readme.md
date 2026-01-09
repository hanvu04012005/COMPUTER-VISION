
#  Thị Giác Máy Tính  
##  Xử lý ảnh với PIL (Pillow) và OpenCV (cv2)

---
**Sinh viên thực hiện:** Nguyễn Hạn Vũ  
**MSSV:** 2374802010571  
**Môn học:** Thị giác máy tính  
**Giảng viên:** Thầy Đỗ Hữu Quân  
---

## 1. Giới thiệu chung  
Trong lĩnh vực **Thị giác máy tính (Computer Vision)**, ảnh số là đối tượng dữ liệu quan trọng nhất. Để xử lý và phân tích ảnh hiệu quả, Python cung cấp nhiều thư viện hỗ trợ, trong đó phổ biến nhất là **PIL (Pillow)** và **OpenCV (cv2)**.
Bài lab này giúp sinh viên:
- Làm quen với cách đọc và hiển thị ảnh số  
- Hiểu cách biểu diễn ảnh dưới dạng pixel và mảng số  
- Thực hành các thao tác xử lý ảnh cơ bản  
- So sánh hai thư viện PIL và OpenCV để thấy rõ sự khác nhau  
---
## 2. Mục tiêu bài Lab  

Sau khi hoàn thành bài lab này, sinh viên có thể:
- Đọc và hiển thị ảnh bằng Python  
- Chuyển đổi ảnh giữa các không gian màu  
- Truy cập và chỉnh sửa pixel ảnh  
- Chuyển ảnh sang ảnh xám và giảm mức xám  
- Tách và xử lý từng kênh màu RGB  
- Hiểu sự khác biệt giữa PIL và OpenCV trong xử lý ảnh  
---
## 3. Công cụ và thư viện sử dụng  
- **Python**  
- **PIL (Pillow)**  
- **OpenCV (cv2)**  
- **NumPy**  
- **Matplotlib**  

--
## 4. Nội dung thực hành  
### 4.1. Đọc và hiển thị ảnh  
Sử dụng PIL và OpenCV để đọc ảnh từ file và hiển thị bằng matplotlib.
### 4.2. Kiểm tra thông tin ảnh  
Kiểm tra kích thước, số kênh màu và chế độ màu của ảnh.
### 4.3. Truy cập pixel  
Thao tác pixel thông qua đối tượng ảnh và mảng NumPy.
### 4.4. Chuyển ảnh sang ảnh xám  
Chuyển ảnh màu sang ảnh xám để đơn giản hóa xử lý.
### 4.5. Giảm mức xám  
Giảm số mức xám để quan sát ảnh hưởng đến chất lượng ảnh.
### 4.6. Tách kênh màu  
Tách và xử lý các kênh màu Red, Green, Blue.
### 4.7. Sao chép ảnh  
Phân biệt sao chép và gán ảnh trong xử lý ảnh.
---

## 5. So sánh PIL và OpenCV  
PIL dễ dùng, phù hợp học cơ bản. OpenCV mạnh, nhanh và dùng cho thị giác máy tính chuyên sâu.
---
## 6. Hướng dẫn chạy  
```bash
pip install pillow opencv-python numpy matplotlib
```
---

## 7. Kết luận  
Bài lab giúp sinh viên nắm được nền tảng xử lý ảnh và thị giác máy tính.
---
## 8. Tài liệu tham khảo  
- Tài liệu thực hành – ĐH Văn Lang  
- Pillow Documentation  
- OpenCV Documentation  

