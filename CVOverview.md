# Computer Vision

## Siamese Network
Siamese Network là một mạng nơ-ron được thiết kế để so sánh hai đầu vào và đưa ra dự đoán dựa trên sự tương đồng hoặc khác biệt của chúng. Mạng bao gồm hai nhánh mạng con (subnetworks) giống nhau, mỗi nhánh xử lý một đầu vào. Sau khi xử lý, đầu ra của mỗi nhánh được đưa vào một lớp kết hợp (merge layer) để tạo ra một vectơ biểu diễn mối quan hệ giữa hai đầu vào. Lớp cuối cùng của mạng sẽ đưa ra dự đoán dựa trên vectơ này.

### Cách làm việc:

1. **Đầu vào**: Hai đầu vào được đưa vào mạng, mỗi đầu vào được xử lý bởi một nhánh mạng con riêng biệt.
2. **Xử lý**: Mỗi nhánh mạng con sử dụng các lớp convolutional neural network (CNN) và pooling layers để trích xuất các đặc điểm quan trọng từ đầu vào.
3. **Kết hợp**: Đầu ra của hai nhánh mạng con được kết hợp với nhau bằng một lớp merge layer.
4. **Dự đoán**: Lớp cuối cùng của mạng sử dụng một lớp fully connected layer để đưa ra dự đoán dựa trên vectơ biểu diễn mối quan hệ giữa hai đầu vào.

### Ứng dụng:

Siamese Network được sử dụng trong nhiều ứng dụng khác nhau, bao gồm:

* **Xác thực khuôn mặt**: So sánh hai hình ảnh khuôn mặt để xác định xem chúng có cùng một người hay không.
* **Xác định đối tượng**: So sánh hai hình ảnh để xác định xem chúng có cùng một đối tượng hay không.
* **Xác định vị trí**: So sánh hai hình ảnh để xác định xem chúng có được chụp từ cùng một vị trí hay không.
* **Dịch máy**: So sánh hai câu để xác định xem chúng có cùng nghĩa hay không.
### Lợi ích:
* **Khả năng so sánh**: Siamese Network có khả năng so sánh hai đầu vào một cách hiệu quả và chính xác.
* **Tính linh hoạt**: Mạng có thể được áp dụng cho nhiều ứng dụng khác nhau.
* **Hiệu quả**: Siamese Network có thể được huấn luyện và sử dụng một cách hiệu quả.
### Hạn chế:
* **Yêu cầu dữ liệu**: Siamese Network yêu cầu một lượng lớn dữ liệu để huấn luyện hiệu quả.
* **Khả năng khái quát**: Mạng có thể gặp khó khăn trong việc khái quát hóa cho các trường hợp mới.
