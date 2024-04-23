# Learning statistics using Python 

https://github.com/Pegah-Ardehkhani/Statistics-and-Probability-in-Python?tab=readme-ov-file

Dưới đây là một số dạng phổ biến của các phương pháp kiểm định:

1. **Kiểm định t:**
   - **Kiểm định t độc lập:** Sử dụng để so sánh giá trị trung bình của hai nhóm độc lập. Ví dụ: so sánh giá trị trung bình chiều cao của nam và nữ.
   - **Kiểm định t phụ thuộc:** Sử dụng khi bạn muốn so sánh giá trị trung bình của một nhóm trước và sau một can thiệp. Ví dụ: so sánh trọng lượng của nhóm người trước và sau khi tham gia chương trình giảm cân.

2. **Kiểm định ANOVA:**
   - **ANOVA một chiều:** Sử dụng khi bạn muốn so sánh giá trị trung bình của ba nhóm trở lên. Ví dụ: so sánh hiệu suất trung bình của ba phương pháp điều trị khác nhau.
   - **ANOVA hai chiều:** Một biến phụ thuộc được so sánh giữa các nhóm trên hai biến độc lập. Ví dụ: so sánh doanh số bán hàng của các cửa hàng (biến phụ thuộc) dựa trên vị trí địa lý và loại sản phẩm (hai biến độc lập).

3. **Kiểm định chi bình phương (Chi-square test):**
   - **Kiểm định chi bình phương độc lập:** Sử dụng để xác định mức độ phụ thuộc giữa hai biến phân loại. Ví dụ: xem xét mối quan hệ giữa việc hút thuốc lá và việc phát triển ung thư phổi.
   - **Kiểm định chi bình phương phi thứ bậc:** Sử dụng để xác định mức độ phụ thuộc giữa ba biến phân loại trở lên. Ví dụ: xem xét mối quan hệ giữa mức độ vận động (thấp, trung bình, cao) và trạng thái sức khỏe (sống sót, bệnh nặng, tử vong) sau một cuộc phẫu thuật.

4. **Kiểm định Mann-Whitney U (Wilcoxon rank-sum test):**
   - Sử dụng để so sánh phân phối của hai nhóm độc lập khi dữ liệu không tuân theo phân phối chuẩn hoặc có sự nghi ngờ về sự độc lập của mẫu. Ví dụ: so sánh thời gian phản ứng của hai phương pháp thử nghiệm khác nhau.

5. **Kiểm định Kruskal-Wallis:**
   - Một phiên bản không tham số của kiểm định ANOVA, sử dụng khi dữ liệu không tuân theo phân phối chuẩn hoặc có sự nghi ngờ về sự độc lập của mẫu.

Các kiểm định thống kê này chỉ là một phần nhỏ trong danh sách rất nhiều phương pháp có sẵn. Lựa chọn kiểm định thích hợp phụ thuộc vào loại dữ liệu của bạn, giả thuyết bạn đang kiểm tra, 
và các giả định của phương pháp thống kê bạn đang sử dụng.

Các kiểm định để kiểm tra tính phân phối của dữ liệu:
xem thêm [statistics with python](https://github.com/trangel/stats-with-python/tree/master)

1. **Q - Q plot (Quantile-Quantile plot):**
   - Một biểu đồ được sử dụng để so sánh phân phối của dữ liệu với một phân phối chuẩn. Nếu các điểm trên biểu đồ nằm trên đường chéo, có nghĩa là dữ liệu của bạn tuân theo phân phối chuẩn.

2. **Skewness và Kurtosis test:**
   - **Skewness:** Đo mức độ lệch của phân phối dữ liệu so với phân phối chuẩn. Một giá trị skewness bằng 0 cho thấy phân phối là đối xứng.
   - **Kurtosis:** Đo mức độ đỉnh của phân phối so với phân phối chuẩn. Một giá trị kurtosis bằng 3 cho thấy phân phối là chuẩn.

3. **Kolmogorov-Smirnov test:**
   - Sử dụng để kiểm tra xem một mẫu có tuân theo một phân phối cụ thể hay không. Nó so sánh cấu trúc của phân phối dữ liệu với phân phối mong muốn.

4. **Shapiro-Wilk test:**
   - Một kiểm định thống kê sử dụng để kiểm tra xem một mẫu có tuân theo phân phối chuẩn hay không. Đây là một trong những kiểm định phổ biến nhất để kiểm tra tính phân phối của dữ liệu.

5. **Anderson-Darling test:**
   - Một kiểm định thống kê sử dụng để kiểm tra xem một mẫu có tuân theo một phân phối cụ thể hay không (thường là phân phối chuẩn). Nó có thể kiểm tra cho nhiều loại phân phối khác nhau.

Các kiểm định này hữu ích để kiểm tra tính phân phối của dữ liệu, điều này có thể quan trọng trong việc lựa chọn phương pháp thống kê phù hợp và giải thích kết quả của nghiên cứu. Tuy nhiên, cần lưu ý rằng việc dùng một phương pháp kiểm định không thể nói lên mọi điều về tính chính xác của dữ liệu và kết quả.
