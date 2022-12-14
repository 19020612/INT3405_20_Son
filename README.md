# INT3405_20_Son
# Phân tích và xếp loại đánh giá Tiếng Việt trên Foody
### Mục lục
1. [Giới thiệu](#introduction)
2. [Tập dữ liệu](#dataset)
3. [Phương pháp](#method)
4. [Kết quả](#result)
5. [Thực thi](#run)
6. [Thành viên](#author)

## Giới thiệu<a name="introduction"></a>

Trong vài năm trở lại đây, dịch vụ vận chuyển nói chung hay giao và đặt đồ ăn nói riêng cực kỳ phát triển. Tuy nhiên cũng chính vì thế mà cũng không thể đảm bảo hết được mọi nguồn chất lượng dịch vụ. Chính vì thế chúng ta cần có những đánh giá review để người tiêu dùng có thể sử dụng những sản phầm chất lượng, phù hợp với bản thân. Tuy nhiên con người luôn bận rộn với những mục tiêu đề ra vì thế thời gian luôn là vấn đề nan giải với mỗi các nhân chúng ta. Chúng ta không thể tự trải nghiệm và tự đánh giá hết đồ ăn trên mạng được. Ứng dụng này sẽ giúp chúng ta tiết kiệm thời gian bằng cách đưa ra đánh giá rating của các comment về món ăn trên Foody bằng cách sử dụng mô hình LSTM

Bài báo cáo này được trình bày bởi nhóm INT3405_20_Son. Nhóm đang xếp hạng thứ 29 trên bảng xếp hạng của Kaggle với điểm số là 0.92096 tính đến thời điểm hiện tại (15h ngày 13/12/2022)  


## Dataset<a name="dataset"></a>

Trong project này, toàn bộ dữ liệu dùng cho đồ án được thu thâp từ Foody [dataset](https://www.kaggle.com/competitions/int3405-sentiment-analysis-problem/data) 

## Method<a name="method"></a>

A.	Recurrent Neural Network

Recurrent Neural Network (RNN – Mạng thần kinh hồi quy) là một lớp của mạng thần kinh nhân tạo mà trong đó đầu ra của bước trước là đầu vào cho bước này. Khác với các mạng thần kinh trước đó với đầu vào và đầu ra độc lập với nhau, khi cần tiên đoán trước các từ tiếp theo trong một câu, ta cần biết và lưu trữ từ trước đó. RNN đã được đưa ra để giải quyết vấn đề với Hidden Layer (tầng ẩn). Phần quan trọng nhất ở RNN là Hidden State (trạng thái ẩn) lưu trữ những thông tin về một chuỗi.

Các kiến trúc của RNN:
- Long short-term memory (LSTM)
- Gated recurrent units (GRUs)


B.	Long short-term memory (LSTM)

Mạng LSTM (Bộ nhớ ngắn hạn – dài hạn) là một loại RNN (Mạng thần kinh tái phát) được sử dụng rộng rãi để học các bài toán dự đoán dữ liệu tuần tự. Giống như mọi mạng thần kinh khác, LSTM cũng có một số lớp giúp nó học và nhận dạng mẫu để có hiệu suất tốt hơn

## Kết quả

* Các chỉ số đánh giá mô hình trong quá trình training được mô tả qua biểu đồ.

* Accuracy lớn nhất là 0.92096

* Từ epoch 10 trở đi thì accuracy trên tập test giảm do overfitting, loss tăng

![318003847_503997925040225_803384621463593818_n](https://user-images.githubusercontent.com/116366668/207346210-ee717322-0aaf-4b7f-a351-49dd92b0e4e1.png)


## Thực thi

### Cài đặt thư viện 
* Tất cả các thư viện yêu cầu được trình bày trong requirements.txt
* Để cài đặt thư viện, chạy các lệnh bên dưới
```bash

pip install requirements.txt
```
### Thực thi
  1. Vào trang [Kaggle trong sau](https://www.kaggle.com/code)
  
  2. Chọn <>Code -> Chọn New Notebook
      ![image](https://user-images.githubusercontent.com/116366668/207310763-0bc05b47-9c9a-4089-93a0-aec9f436874e.png)

  3. Chọn File -> Import Notebook -> Import from GitHub
     ![image](https://user-images.githubusercontent.com/116366668/207310637-49a46918-dd61-4dac-ab2c-9037158728e1.png)
     Dán dường link vào ô: https://github.com/19020612/INT3405_20_Son/blob/deb396b05f33e3ee7ea642999b5dd6f0a9b6181b/int3405-20-son.ipynb 
     ![image](https://user-images.githubusercontent.com/116366668/207310506-4e3d6f8b-fdf7-4426-a8b4-9550d2ce6ec1.png)

     Chọn Import 
  4. Chọn Add data -> Search từ khóa INT3405-sen -> Chọn Add competition
  
  ![image](https://user-images.githubusercontent.com/116366668/207311743-5727de6d-45c7-4a85-b0e2-18f81e95a15c.png)

     
  5. Chọn Run -> Run All để train model
  ![image](https://user-images.githubusercontent.com/116366668/207310217-12af6b59-0106-4bf6-bf23-1bcff409d109.png)

## Thành viên
```
Đỗ Thanh Nghị - 19020585@vnu.edu.vn
Trần Vũ Toàn - 19020637@vnu.edu.vn 
Nguyễn Ngọc Sơn - 19020612@vnu.edu.vn
Nguyễn Ngọc Trường Sơn - 19020610@vnu.edu.vn
Đào Duy Thuận - 19020635@vnu.edu.vn

