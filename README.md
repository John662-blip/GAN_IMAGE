# DCGAN Sinh Ảnh Phong Cảnh

## 📌 Giới thiệu
Dự án này triển khai **Deep Convolutional GAN (DCGAN)** để sinh ảnh phong cảnh.  
Mô hình học phân phối của ảnh phong cảnh thật và tạo ra ảnh giả trông giống ảnh thật.

## 📂 Dataset
- Bộ dữ liệu: [mertcobanov/nature-dataset](https://huggingface.co/datasets/mertcobanov/nature-dataset) (Hugging Face).  
- Ảnh được resize và chuẩn hóa về **64×64** trước khi huấn luyện.

## ⚙️ Mô hình
- **Generator**: Mạng CNN tích chập chuyển vị (transposed convolution) để sinh ảnh từ nhiễu ngẫu nhiên.  
- **Discriminator**: Mạng CNN để phân biệt ảnh thật và ảnh sinh.  
- **Loss**: Binary Cross-Entropy (BCE) với optimizer Adam.  

## 📊 Đánh giá
Đánh giá mô hình bằng **Fréchet Inception Distance (FID)** và **Kernel Inception Distance (KID)**, so sánh **10,000 ảnh thật** với **10,000 ảnh sinh**.

- **FID**: `30.1080`  
- **KID**: `0.0145 ± 0.0004`  

## 🚀 Kết quả
- Ảnh phong cảnh sinh ra tái hiện được cấu trúc tổng thể và phân bố màu sắc.  
- Chỉ số FID và KID cho thấy ảnh sinh tương đối gần với phân phối ảnh thật.
## Một số ảnh sinh 
<img width="1641" height="816" alt="image" src="https://github.com/user-attachments/assets/353de61d-ddc0-451c-9912-a1ac5dd1a199" />
