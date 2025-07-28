# Yolov5-Project-Team15 
- Họ tên sinh Viên : Trần Nghiêm Nhật Thiện, Bùi Hữu Tài, Lưu Võ Phương Mai, Nguyễn Hoàng Long
- Môn Học: Nhập Môn Xử Lý Ảnh Số
- Giảng viên: TS.Đỗ Hữu Quân
#  YOLOv5 - Nhận diện đối tượng thời gian thực

##  Tổng quan dự án

Dự án sử dụng YOLOv5 (You Only Look Once phiên bản 5) để thực hiện nhận diện đối tượng trong ảnh, video và nguồn webcam. Đây là một mô hình học sâu nổi tiếng nhờ tốc độ nhanh và độ chính xác cao, phù hợp cho các ứng dụng AI, giám sát an ninh, ô tô tự lái và nhiều hơn nữa.

##  Tính năng chính

- Nhận diện đối tượng từ:
  -  Ảnh tĩnh
  -  Video (.mp4, .avi, ...)
  -  Webcam thời gian thực (`--source 0`)
- Hỗ trợ nhiều mô hình: yolov5s, yolov5m, yolov5l, yolov5x
- Lưu kết quả nhận diện: bounding box, nhãn, độ tự tin
- Khả năng tùy chỉnh ngưỡng và kích thước hình ảnh đầu vào

##  Công nghệ sử dụng

| Công nghệ    | Mô tả                                       |
|--------------|---------------------------------------------|
| Python       | Ngôn ngữ chính để phát triển và triển khai |
| PyTorch      | Framework học sâu dùng cho huấn luyện/model|
| OpenCV       | Xử lý hình ảnh và video                    |
| YOLOv5       | Mô hình phát hiện đối tượng chính          |

## Môi trường ảo (có sẵn do Ultralytics cung cấp)
<a href="https://bit.ly/yolov5-paperspace-notebook" rel="nofollow"><img src="https://camo.githubusercontent.com/6df71b7d7e0b09a2e97776f416bcd40acf48fc87337f8bcce48e4235537daf1f/68747470733a2f2f6173736574732e706170657273706163652e696f2f696d672f6772616469656e742d62616467652e737667" alt="Run on Gradient" data-canonical-src="https://assets.paperspace.io/img/gradient-badge.svg" style="max-width: 100%;"></a>
<a href="https://colab.research.google.com/github/ultralytics/yolov5/blob/master/tutorial.ipynb" rel="nofollow"><img src="https://camo.githubusercontent.com/96889048f8a9014fdeba2a891f97150c6aac6e723f5190236b10215a97ed41f3/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667" alt="Open In Colab" data-canonical-src="https://colab.research.google.com/assets/colab-badge.svg" style="max-width: 100%;"></a>
<a href="https://www.kaggle.com/models/ultralytics/yolov5" rel="nofollow"><img src="https://camo.githubusercontent.com/c7135949c5c6882489e68f4af05a78a759460a4db256b86df3097e04419b4d9e/68747470733a2f2f6b6167676c652e636f6d2f7374617469632f696d616765732f6f70656e2d696e2d6b6167676c652e737667" alt="Open In Kaggle" data-canonical-src="https://kaggle.com/static/images/open-in-kaggle.svg" style="max-width: 100%;"></a>

##  Các mô hình đã huấn luyện sẵn (Pretrained Checkpoints)
- Bảng sau đây hiển thị các chỉ số hiệu suất của các mô hình YOLOv5 khác nhau được huấn luyện trên bộ dữ liệu COCO
<markdown-accessiblity-table data-catalyst=""><table tabindex="0">
<thead>
<tr>
<th>Model</th>
<th>Size<br><sup>(pixels)</sup></th>
<th>mAP<sup>val<br>50-95</sup></th>
<th>mAP<sup>val<br>50</sup></th>
<th>Speed<br><sup>CPU b1<br>(ms)</sup></th>
<th>Speed<br><sup>V100 b1<br>(ms)</sup></th>
<th>Speed<br><sup>V100 b32<br>(ms)</sup></th>
<th>Params<br><sup>(M)</sup></th>
<th>FLOPs<br><sup>@640 (B)</sup></th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5n.pt">YOLOv5n</a></td>
<td>640</td>
<td>28.0</td>
<td>45.7</td>
<td><strong>45</strong></td>
<td><strong>6.3</strong></td>
<td><strong>0.6</strong></td>
<td><strong>1.9</strong></td>
<td><strong>4.5</strong></td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5s.pt">YOLOv5s</a></td>
<td>640</td>
<td>37.4</td>
<td>56.8</td>
<td>98</td>
<td>6.4</td>
<td>0.9</td>
<td>7.2</td>
<td>16.5</td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5m.pt">YOLOv5m</a></td>
<td>640</td>
<td>45.4</td>
<td>64.1</td>
<td>224</td>
<td>8.2</td>
<td>1.7</td>
<td>21.2</td>
<td>49.0</td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5l.pt">YOLOv5l</a></td>
<td>640</td>
<td>49.0</td>
<td>67.3</td>
<td>430</td>
<td>10.1</td>
<td>2.7</td>
<td>46.5</td>
<td>109.1</td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5x.pt">YOLOv5x</a></td>
<td>640</td>
<td>50.7</td>
<td>68.9</td>
<td>766</td>
<td>12.1</td>
<td>4.8</td>
<td>86.7</td>
<td>205.7</td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5n6.pt">YOLOv5n6</a></td>
<td>1280</td>
<td>36.0</td>
<td>54.4</td>
<td>153</td>
<td>8.1</td>
<td>2.1</td>
<td>3.2</td>
<td>4.6</td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5s6.pt">YOLOv5s6</a></td>
<td>1280</td>
<td>44.8</td>
<td>63.7</td>
<td>385</td>
<td>8.2</td>
<td>3.6</td>
<td>12.6</td>
<td>16.8</td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5m6.pt">YOLOv5m6</a></td>
<td>1280</td>
<td>51.3</td>
<td>69.3</td>
<td>887</td>
<td>11.1</td>
<td>6.8</td>
<td>35.7</td>
<td>50.0</td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5l6.pt">YOLOv5l6</a></td>
<td>1280</td>
<td>53.7</td>
<td>71.3</td>
<td>1784</td>
<td>15.8</td>
<td>10.5</td>
<td>76.8</td>
<td>111.4</td>
</tr>
<tr>
<td><a href="https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5x6.pt">YOLOv5x6</a><br>+ <a href="https://docs.ultralytics.com/yolov5/tutorials/test_time_augmentation/" rel="nofollow">[TTA]</a></td>
<td>1280<br>1536</td>
<td>55.0<br><strong>55.8</strong></td>
<td>72.7<br><strong>72.7</strong></td>
<td>3136<br>-</td>
<td>26.2<br>-</td>
<td>19.4<br>-</td>
<td>140.7<br>-</td>
<td>209.8<br>-</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>

## ⚙️ Cài đặt chi tiết

###  Clone repository YOLOv5 và các thư viện cần thiết

```bash
git clone https://github.com/ultralytics/yolov5.git
cd yolov5
pip install -r requirements.txt
```
## Cấu trúc dự án
```plaintext
yolov5/
├── data/               # Cấu hình tập dữ liệu
├── models/             # Cấu trúc mô hình YOLOv5
├── utils/              # Hàm tiện ích (vẽ, xử lý ảnh,...)
├── detect.py           # Script nhận diện đối tượng
├── train.py            # Huấn luyện mô hình
├── val.py              # Đánh giá mô hình
├── weights/            # File model đã huấn luyện (.pt)
└── README.md           # Mô tả dự án
```
## Các câu lệnh nhận diện (img,video,cam,..etc)
```bash
python detect.py --weights yolov5s.pt --source 0                              # webcam
python detect.py --weights yolov5s.pt --source image.jpg                      # image
python detect.py --weights yolov5s.pt --source video.mp4                      # video
python detect.py --weights yolov5s.pt --source screen                         # screenshot
python detect.py --weights yolov5s.pt --source path/                          # directory
python detect.py --weights yolov5s.pt --source list.txt                       # list of images
python detect.py --weights yolov5s.pt --source list.streams                   # list of streams
python detect.py --weights yolov5s.pt --source 'path/*.jpg'                   # glob pattern
python detect.py --weights yolov5s.pt --source 'https://youtu.be/LNwODJXcvt4' # YouTube video
python detect.py --weights yolov5s.pt --source 'rtsp://example.com/media.mp4' # RTSP, RTMP, HTTP stream
```
## Một số demo thực hiện của nhóm
![Kết quả mô hình](images/ketqua_saukhitrain500.png)
![Kết quả mô hình](images/results.png)
![Kết quả mô hình](images/val_batch0_pred.jpg)
![Kết quả mô hình](images/cats.jpg)
![Kết quả mô hình](images/chovameo1.jpg)
![Kết quả mô hình](images/chovameo4.jpg)
![Kết quả mô hình](images/chovameo5.jpg)
![Kết quả mô hình](images/chovameo6.jpeg)

# Tài liệu tham khảo thêm :
- [All about YOLOv5 Docs](https://docs.ultralytics.com/vi/yolov5/)
- [Github Ultralytics YOLOv5](https://github.com/ultralytics/yolov5)
- [Youtube using YOLOv5 for train custom datasets ver VIE](https://www.youtube.com/watch?v=eSS0EnCX1A0)
- [Train YOLOv5 custom dataset](https://viblo.asia/p/su-dung-colab-train-yolov5-voi-custom-dataset-phat-hien-cac-doi-tuong-dac-thu-Az45bqv6lxY)
- [Google](https://www.google.com/)
- Slide bài giảng Nhập môn Xử lý ảnh số - Văn Lang University
