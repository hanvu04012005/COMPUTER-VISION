# Thị Giác Máy Tính  
## Geometric Transformations (PIL & OpenCV)
---
**Sinh viên thực hiện:** Nguyễn Hạn Vũ  
**MSSV:** 2374802010571  
**Môn học:** Thị giác máy tính  
**Giảng viên:** Thầy Đỗ Hữu Quân  
---

## Giới thiệu
Trong bài thực hành này, em thực hiện các phép **biến đổi hình học (Geometric Transformations)** trên ảnh số bằng Python.  
Hai thư viện được sử dụng là **PIL (Pillow)** và **OpenCV (cv2)** nhằm giúp làm quen và so sánh cách triển khai các phép biến đổi ảnh cơ bản giữa hai thư viện.

Mục tiêu của bài:
- Hiểu nguyên lý các phép biến đổi hình học trên ảnh
- Thực hành dịch chuyển, xoay, co giãn ảnh
- Áp dụng biến đổi affine bằng PIL và OpenCV

---

## Danh sách file

### 1. `2374802010571_NguyenHanVu_MaLHP_Lab02.ipynb`
Notebook tổng hợp nội dung **Lab 02**, bao gồm các bài thực hành liên quan đến xử lý ảnh và biến đổi hình học.

#### Nội dung thực hiện:
- Đọc và hiển thị ảnh
- Thao tác xử lý ảnh cơ bản
- Thực hiện các phép biến đổi hình học
- Minh họa kết quả bằng hình ảnh trực quan

---

### 2. `2.4.1_Gemetric_trasfroms_PIL.ipynb`
Notebook sử dụng thư viện **PIL (Pillow)** để thực hiện các phép biến đổi hình học trên ảnh.

#### Nội dung thực hiện:
- Dịch chuyển ảnh (Translation)
- Xoay ảnh (Rotation)
- Thay đổi kích thước ảnh (Scaling)
- Biến đổi affine cơ bản bằng PIL

---

### 3. `2.4.2_Gemetric_trasfroms_OpenCV.ipynb`
Notebook sử dụng thư viện **OpenCV (cv2)** để thực hiện các phép biến đổi hình học.

#### Nội dung thực hiện:
- Dịch chuyển ảnh bằng ma trận biến đổi
- Xoay ảnh với `cv2.getRotationMatrix2D`
- Thay đổi kích thước ảnh
- Biến đổi affine và perspective trong OpenCV

---

## Công cụ và thư viện sử dụng
- Python
- PIL (Pillow)
- OpenCV (cv2)
- NumPy
- Matplotlib

---

## Kết luận
Qua bài thực hành này, sinh viên nắm được cách áp dụng các phép biến đổi hình học trên ảnh và hiểu rõ sự khác nhau giữa việc triển khai bằng **PIL** và **OpenCV**, làm nền tảng cho các bài toán xử lý ảnh và thị giác máy tính nâng cao.
