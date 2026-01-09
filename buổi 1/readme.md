
#  Thị Giác Máy Tính  
##  Xử lý ảnh với PIL (Pillow) và OpenCV (cv2)
---
**Sinh viên thực hiện:** Nguyễn Hạn Vũ  
**MSSV:** 2374802010571  
**Môn học:** Thị giác máy tính  
**Giảng viên:** Thầy Đỗ Hữu Quân  
---

## 1. Giới thiệu chung  
Trong lĩnh vực Thị giác máy tính (Computer Vision), ảnh số là dữ liệu đầu vào quan trọng để máy tính có thể “nhìn”, phân tích và hiểu được thế giới xung quanh. Trước khi áp dụng các thuật toán nâng cao như nhận dạng khuôn mặt, phát hiện đối tượng hay học sâu, sinh viên cần nắm vững các thao tác xử lý ảnh cơ bản.

Bài Lab nhằm giúp sinh viên làm quen với hai thư viện xử lý ảnh phổ biến nhất trong Python là PIL (Pillow) và OpenCV (cv2). Thông qua việc thực hành trực tiếp trên ảnh, sinh viên hiểu được cách ảnh được lưu trữ, hiển thị và xử lý ở mức pixel.

Nội dung bài lab được triển khai trong hai file Jupyter Notebook:
2.1.1_Images_with_python_library_PIL.ipynb
2.1.2_Images_with_python_library_CV.ipynb
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
-Python: ngôn ngữ lập trình chính
-PIL (Pillow): thư viện xử lý ảnh cơ bản, dễ sử dụng
-OpenCV (cv2): thư viện mạnh cho thị giác máy tính
-NumPy: xử lý ảnh dưới dạng mảng số
-Matplotlib: hiển thị ảnh 

--
## 4. Nội dung thực hành  
4.1. Đọc và hiển thị ảnh
Ảnh được đọc từ file bằng thư viện PIL (Image.open()) và OpenCV (cv2.imread()), sau đó hiển thị bằng image.show() hoặc matplotlib. Sinh viên quan sát sự khác nhau giữa cách hiển thị ảnh của Pillow và matplotlib, đồng thời thực hiện chuyển đổi hệ màu BGR sang RGB khi hiển thị ảnh OpenCV.
4.2. Kiểm tra thông tin ảnh
Sinh viên kiểm tra các thông tin cơ bản của ảnh như kích thước ảnh (image.size, image.shape) và chế độ màu (image.mode). Qua đó hiểu được sự khác nhau giữa ảnh màu RGB và ảnh xám.
4.3. Truy cập và thao tác pixel
Thực hiện truy cập giá trị pixel tại một vị trí cụ thể bằng image.load() (PIL) và thông qua mảng NumPy (OpenCV). Sinh viên nhận biết mỗi pixel ảnh màu gồm ba giá trị tương ứng với các kênh Red, Green và Blue.
4.4. Chuyển ảnh sang ảnh xám
Ảnh màu được chuyển sang ảnh xám bằng ImageOps.grayscale() hoặc hiển thị ảnh xám với cmap='gray'. Việc này giúp đơn giản hóa ảnh và thuận lợi cho các bước xử lý tiếp theo.
4.5. Giảm mức xám (Quantization)
Sinh viên thực hiện giảm số mức xám của ảnh từ 256 xuống các mức nhỏ hơn như 128, 64, 32, 16 và 8, sau đó quan sát sự thay đổi chất lượng ảnh khi số mức xám giảm.
4.6. Tách và xử lý kênh màu RGB
Ảnh màu được tách thành các kênh Red, Green và Blue bằng image.split() hoặc thao tác trực tiếp trên mảng NumPy. Sinh viên quan sát vai trò của từng kênh màu trong việc tạo nên ảnh màu hoàn chỉnh.
4.7. Chuyển ảnh sang mảng NumPy
Ảnhđược chuyển sang dạng mảng NumPy bằng np.array(image) để phục vụ cho các thao tác xử lý ảnh và thị giác máy tính nâng cao.
---

## 5. So sánh PIL và OpenCV  
PIL (Pillow) và OpenCV (cv2) đều là các thư viện dùng để xử lý ảnh trong Python nhưng phục vụ những mục đích khác nhau.
PIL (Pillow) là thư viện xử lý ảnh cơ bản, dễ học và dễ sử dụng. Ảnh trong PIL được biểu diễn dưới dạng đối tượng PIL.Image.Image, phù hợp cho các thao tác đơn giản như mở ảnh, lưu ảnh, chuyển ảnh sang xám, cắt ảnh hoặc ghép ảnh. PIL sử dụng hệ màu RGB nên khi hiển thị ảnh bằng matplotlib có thể hiển thị trực tiếp mà không cần chuyển đổi. Tuy nhiên, tốc độ xử lý của PIL không cao và khả năng xử lý ảnh nâng cao còn hạn chế.
OpenCV (cv2) là thư viện mạnh chuyên dùng cho xử lý ảnh và thị giác máy tính (Computer Vision). Ảnh trong OpenCV được lưu trực tiếp dưới dạng mảng NumPy (numpy.ndarray), do đó rất thuận tiện cho việc tính toán và xử lý pixel. OpenCV sử dụng hệ màu BGR, vì vậy khi hiển thị ảnh bằng matplotlib cần chuyển đổi từ BGR sang RGB để tránh sai màu. OpenCV có tốc độ xử lý nhanh, hỗ trợ nhiều thuật toán nâng cao như lọc ảnh, phát hiện cạnh, nhận diện khuôn mặt và ứng dụng trong AI.
Tóm lại, PIL phù hợp cho người mới học và các bài toán xử lý ảnh đơn giản, trong khi OpenCV phù hợp cho các bài toán phức tạp, yêu cầu hiệu năng cao và ứng dụng trong Computer Vision.
## 6. Hướng dẫn chạy  
Để chạy các chương trình trong hai file notebook, sinh viên thực hiện các bước sau:
Cài đặt các thư viện cần thiết bằng lệnh
pip install pillow opencv-python numpy matplotlib
Mở hai file Jupyter Notebook:
-2.1.1_Images_with_python_library_PIL.ipynb
-2.1.2_Images_with_python_library_CV.ipynb
Chạy lần lượt từng cell trong notebook theo thứ tự từ trên xuống dưới.
Quan sát kết quả ảnh hiển thị sau mỗi bước xử lý để hiểu rõ tác dụng của từng thao tác.
Có thể thay đổi tham số (kích thước ảnh, kênh màu, mức xám, v.v.) để thử nghiệm thêm và quan sát sự thay đổi của ảnh.
---

## 7. Kết luận  
Thông qua bài lab này, sinh viên đã làm quen với các thao tác xử lý ảnh cơ bản trong lĩnh vực thị giác máy tính, bao gồm đọc và hiển thị ảnh, truy cập pixel, chuyển ảnh sang ảnh xám, giảm mức xám và tách các kênh màu RGB. Đồng thời, sinh viên hiểu được cách biểu diễn ảnh số dưới dạng đối tượng ảnh và mảng NumPy.
Bài lab cũng giúp sinh viên nhận biết sự khác nhau giữa hai thư viện phổ biến là PIL (Pillow) và OpenCV (cv2) trong xử lý ảnh. Đây là nền tảng quan trọng để tiếp tục học và áp dụng các kỹ thuật xử lý ảnh và thị giác máy tính nâng cao trong các bài học tiếp theo.
---
## 8. Tài liệu tham khảo  
- Tài liệu thực hành – ĐH Văn Lang  
- Pillow Documentation  
- OpenCV Documentation  

