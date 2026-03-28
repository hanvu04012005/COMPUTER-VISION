# Thị Giác Máy Tính

## Nhận Diện Đối Tượng Trong Video (Video Detection)

---

**Sinh viên thực hiện:** Nguyễn Hạn Vũ

**MSSV:** 2374802010571

**Môn học:** Thị giác máy tính

**Giảng viên:** Thầy Đỗ Hữu Quân

---

## Giới thiệu

Trong bài thực hành này, em thực hiện bài toán **nhận diện đối tượng trong video (Video Object Detection)** bằng Python.
Bài lab sử dụng thư viện **ImageAI** kết hợp với mô hình học sâu **RetinaNet** để phát hiện các đối tượng trong video.

### Mục tiêu:

* Hiểu cách áp dụng Deep Learning vào video
* Thực hiện nhận diện đối tượng theo từng frame
* Làm quen với thư viện ImageAI
* Xuất video sau khi detect

---

## Dữ liệu đầu vào

* Nguồn video: https://pixabay.com/vi/videos/search/lễ%20hội/
* Độ dài: **12 – 20 giây**
* Yêu cầu: **có người trong video**
* Tên file: `video_predetect.mp4`

---

## Danh sách file

### 1. `2374802010571_NguyenHanVu_MaLHP_Lab08.ipynb`

Notebook chính thực hiện bài Lab 08.

**Nội dung:**

* Cài đặt ImageAI
* Load mô hình RetinaNet
* Nhận diện đối tượng trong video
* Xuất video kết quả

---




### 2. `retinanet_resnet50_fpn_coco-eeacb38b.pth`

Trọng số mô hình RetinaNet (pretrained COCO)

Nguồn:
https://github.com/OlafenwaMoses/ImageAI/blob/master/imageai/Detection/VIDEO.md

---

## Công cụ sử dụng

* Python
* ImageAI
* OpenCV
* NumPy

---

## Phương pháp thực hiện

### 1. Load mô hình

Sử dụng mô hình **RetinaNet** pretrained.

### 2. Xử lý video

* Chia video thành các frame
* Detect từng frame

### 3. Nhận diện đối tượng

Các object phổ biến:

* Person
* Car
* Bicycle
* ...

### 4. Xuất video

* Vẽ bounding box
* Gắn label
* Xuất file `.mp4`

---

## Code chính

```python
!pip install imageai

from imageai.Detection import VideoObjectDetection
import os

execution_path = os.getcwd()

detector = VideoObjectDetection()
detector.setModelTypeAsRetinaNet()
detector.setModelPath(os.path.join(execution_path,
"retinanet_resnet50_fpn_coco-eeacb38b.pth"))

detector.loadModel()

video_path = detector.detectObjectsFromVideo(
    input_file_path=os.path.join(execution_path, "video_predetect.mp4"),
    output_file_path=os.path.join(execution_path, "video_detected"),
    frames_per_second=5,
    log_progress=True
)

print(video_path)
```

---

## Kết luận

Qua bài lab, sinh viên:

* Hiểu cách áp dụng Deep Learning vào video
* Biết sử dụng ImageAI để detect object
* Làm quen với RetinaNet
* Xuất video kết quả

### Ứng dụng:

* Giám sát an ninh
* Smart city
* Xe tự lái
* Phân tích hành vi

---
dạ do vid sau khi detect nó lớn hơn 25mb nên em úp lên drive để nộp ạ. 
https://drive.google.com/file/d/19ZqS2mufBsaYakv-ptRN-lRXImB5G2Zg/view?usp=sharing

