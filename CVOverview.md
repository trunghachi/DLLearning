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

Một số kiến trúc hiệu quả hơn so với Seamese Networks: Triplet Network, LSTM

## Triplet Network
Triplet Networks là một kiểu kiến trúc mạng nơ-ron được sử dụng cho các tác vụ học tập khoảng cách (metric learning), đặc biệt là để so sánh tính tương đồng giữa các đầu vào. Trong khi Siamese Network chỉ so sánh hai đầu vào, Triplet Network sử dụng ba đầu vào để học được các biểu diễn vector có ý nghĩa hơn cho dữ liệu. Ba đầu vào này được gọi là:
### Đầu vào mạng:
* Anchor (A): Đầu vào tham chiếu.
* Positive (P): Đầu vào có cùng bản chất với Anchor (tức là chúng tương đồng).
* Negative (N): Đầu vào có bản chất khác biệt với Anchor (tức là chúng không tương đồng).
 
Triplet Loss là hàm mất mát (loss function) được sử dụng để huấn luyện Triplet Network. Hàm này nhằm mục đích kéo gần khoảng cách giữa Anchor (A) và Positive (P) trong không gian vector, đồng thời đẩy xa khoảng cách giữa Anchor (A) và Negative (N).

### Cách hoạt động:

1. Xử lý đầu vào: Ba đầu vào (A, P, N) được đưa vào mạng, mỗi đầu vào được xử lý bởi một nhánh mạng con riêng biệt trích xuất các đặc điểm quan trọng.
2. Biểu diễn vector: Quá trình xử lý tạo ra ba vector biểu diễn tương ứng cho Anchor (fA), Positive (fP), và Negative (fN).
3. Triplet Loss: Hàm Triplet Loss tính toán khoảng cách giữa các vector, thường sử dụng Euclidean distance. Mục tiêu là giảm thiểu biểu thức sau:
    L(A, P, N) = max( ||fA - fP||^2 - ||fA - fN||^2 +  m, 0)
* || ||^2 ký hiệu bình phương độ dài (Euclidean distance).
* m là một tham số margin, đảm bảo khoảng cách giữa Anchor-Positive luôn nhỏ hơn một giá trị nhất định so với Anchor-Negative.

Giải thích:

* Hàm Triplet Loss phạt mạng khi khoảng cách giữa Anchor và Positive lớn hơn khoảng cách giữa Anchor và Negative cộng với một margin (m).
* Trong quá trình huấn luyện, mạng điều chỉnh các tham số để giảm thiểu Triplet Loss, do đó ép các vector của Anchor và Positive gần nhau trong không gian vector, đồng thời đẩy vector của Negative ra xa.

### Ưu điểm:
* Triplet Network học được các biểu diễn vector phản ánh tốt hơn về mức độ tương đồng giữa các đầu vào.
* So với Siamese Network, Triplet Network có thể học được các mối quan hệ phức tạp hơn giữa các đầu vào.

### Nhược điểm:
* Huấn luyện Triplet Network đòi hỏi dữ liệu phức tạp hơn. Cần tạo ra các triplet (A, P, N) phù hợp, điều này có thể tốn nhiều công sức hơn so với Siamese Network chỉ cần cặp dữ liệu.
* Tính toán Triplet Loss phức tạp hơn so với hàm mất mát của Siamese Network, dẫn đến chi phí tính toán cao hơn trong quá trình huấn luyện.

### Triplet Network phù hợp cho:
* Các tác vụ đòi hỏi học mức độ tương đồng theo thứ bậc giữa các đầu vào (ví dụ: xếp hạng các mục tương tự).
* Trường hợp dữ liệu có sẵn để tạo các triplet phù hợp.
