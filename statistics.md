# Statistics and Probability in Python

https://github.com/Pegah-Ardehkhani/Statistics-and-Probability-in-Python?tab=readme-ov-file

## Chapter 1:  Special Continuous Random Variables [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Pegah-Ardehkhani/Statistics-and-Probability-in-Python/blob/main/Chapter%201%20Special%20Continuous%20Random%20Variables.ipynb)


1. **Normal (Gaussian) Distribution:**
   - Phân phối chuẩn là một trong những phân phối phổ biến nhất trong thống kê. Nó có hình dạng đồng dạng, đối xứng và có trung bình, phương sai xác định. Đây là phân phối mà nhiều biến ngẫu nhiên trong tự nhiên và trong các quá trình thực tế tuân theo.

2. **Chi-square Distribution:**
   - Phân phối chi bình phương là một trong những phân phối quan trọng trong thống kê. Nó thường được sử dụng trong việc xây dựng các kiểm định thống kê và ước lượng khoảng tin cậy, đặc biệt trong các nghiên cứu về mô hình tuyến tính và phân tích phương sai.

3. **T-student Distribution:**
   - Phân phối t-Student là một phân phối đối với biến ngẫu nhiên có phương sai không biết và có kích thước mẫu nhỏ. Nó được sử dụng trong các kiểm định liên quan đến so sánh trung bình giữa hai nhóm dữ liệu.

4. **Fisher Distribution:**
   - Phân phối Fisher (còn gọi là phân phối F) thường được sử dụng trong kiểm định phương sai và các kiểm định hồi quy đa biến.

5. **Continuous Uniform Distribution:**
   - Phân phối liên tục đồng đều là một phân phối trong đó mọi giá trị trong một phạm vi nhất định có xác suất tương đồng nhau. Ví dụ: quán trình lựa chọn ngẫu nhiên từ một tập hợp các số.

6. **Exponential Distribution:**
   - Phân phối mũ là một phân phối liên tục mô tả thời gian giữa các sự kiện xảy ra độc lập theo một tỷ lệ hằng định. Nó thường được sử dụng trong mô hình về thời gian giữa các sự kiện.

7. **Gamma Distribution:**
   - Phân phối gamma là một phân phối liên tục mà thường được sử dụng để mô hình hóa thời gian giữa các sự kiện có thể xảy ra theo tỷ lệ không đổi.

8. **Beta Distribution:**
   - Phân phối beta là một phân phối liên tục có giới hạn giữa 0 và 1. Nó thường được sử dụng để mô hình hóa tỷ lệ hoặc xác suất trong các mô hình thống kê bayesian.

9. **Weibull Distribution:**
   - Phân phối Weibull là một phân phối liên tục được sử dụng để mô hình hóa thời gian hoặc tỷ lệ sống sót.

10. **Cauchy Distribution:**
    - Phân phối Cauchy là một phân phối liên tục có đuôi dài, không có giá trị kỳ vọng hoặc phương sai hữu hạn.

11. **Laplace Distribution:**
    - Phân phối Laplace là một phân phối liên tục với hai đỉnh và đuôi đu dài. Nó thường được sử dụng trong các mô hình đòi hỏi tính cân bằng giữa độ chính xác và tính đơn giản.

## Chapter 2: Special Discrete Random Variables

1. **Bernoulli Distribution:**
   - Phân phối Bernoulli mô tả kết quả của một thí nghiệm Bernoulli duy nhất, trong đó chỉ có hai kết quả có thể xảy ra: thành công (có xác suất p) hoặc thất bại (có xác suất q = 1 - p). Ví dụ: việc tung một đồng xu có thể cho kết quả là mặt sấp (thất bại) hoặc mặt ngửa (thành công).

2. **Binomial Distribution:**
   - Phân phối nhị thức mô tả số lần thành công trong n thí nghiệm Bernoulli độc lập với xác suất thành công p. Ví dụ: số lần đầu mặt ngửa xuất hiện khi tung một đồng xu n lần.

3. **Negative Binomial (Pascal) Distribution:**
   - Phân phối nhị thức âm mô tả số lần thử nghiệm Bernoulli độc lập cần thiết cho đạt được một số lượng cố định k thành công. Nó cho biết số lần thử nghiệm cho đến khi xảy ra k sự kiện thành công. Ví dụ: số lần tung một đồng xu cần thiết để có được 3 lần mặt ngửa.

4. **Geometric Distribution:**
   - Phân phối hình học mô tả số lần thử nghiệm Bernoulli độc lập cần thiết cho đến khi xảy ra lần thành công đầu tiên. Nó cho biết số lần thử nghiệm cho đến khi xảy ra sự kiện thành công đầu tiên. Ví dụ: số lần tung một đồng xu cần thiết để có được lần mặt ngửa đầu tiên.

5. **Poisson Distribution:**
   - Phân phối Poisson mô tả số lần một sự kiện xảy ra trong một khoảng thời gian hoặc không gian cố định, với một tần suất cố định và độc lập với thời gian. Nó thường được sử dụng để mô hình hóa số lượng sự kiện hiếm thấy trong một khoảng thời gian nhất định. Ví dụ: số lần xe buýt đi qua một điểm dừng trong một giờ.

6. **Discrete Uniform Distribution:**
   - Phân phối đều rời rạc mô tả xác suất của mỗi giá trị rời rạc trong một tập hợp có số lượng hữu hạn các giá trị, mỗi giá trị có xác suất xuất hiện bằng nhau. Ví dụ: tung một con xúc xắc, mỗi mặt có xác suất xuất hiện là 1/6.

7. **Hypergeometric Distribution:**
   - Phân phối siêu hình học mô tả số lần thành công trong một mẫu rút ra từ một quần thể có số lượng hữu hạn các thành phần, mà không thay đổi kích thước mẫu sau mỗi lần rút. Nó được sử dụng khi mẫu không được thay thế. Ví dụ: số quân bài gốc là 52, và bạn rút ra 5 quân bài, bạn muốn biết xác suất rút được 3 quân bài đỏ.

## Chapter 3: Confidence Intervals

1. **Tín lượng khoảng (Confidence Interval) cho trung bình của một quần thể chuẩn:**
   - **3.1.1. Độ lệch tiêu chuẩn đã biết (Known Standard Deviation):** Khoảng tin cậy được sử dụng để ước lượng trung bình của một quần thể chuẩn khi độ lệch tiêu chuẩn của quần thể đã biết trước. Đây là trường hợp khi bạn đã biết giá trị của độ lệch tiêu chuẩn và muốn ước lượng giá trị trung bình của quần thể.
   - **3.1.2. Độ lệch tiêu chuẩn chưa biết (Unknown Standard Deviation):** Trong trường hợp bạn không biết độ lệch tiêu chuẩn của quần thể, mà bạn phải sử dụng một mẫu và ước lượng trung bình của quần thể dựa trên mẫu.

2. **Tín lượng khoảng cho phương sai của một quần thể chuẩn:**
   - **3.2.1. Giá trị trung bình của quần thể chưa biết (Unknown Mean of the Population):** Khoảng tin cậy được sử dụng để ước lượng phương sai của một quần thể chuẩn khi giá trị trung bình của quần thể không biết. 
   - **3.2.2. Giá trị trung bình của quần thể đã biết (Known Mean of the Population):** Khoảng tin cậy được sử dụng khi bạn biết giá trị trung bình của quần thể và muốn ước lượng phương sai của nó.

3. **Tín lượng khoảng cho sự khác biệt giữa trung bình của hai quần thể chuẩn:**
   - **3.3.1. Phương sai đã biết (Known Variances):** Sử dụng khi cả hai quần thể có phương sai đã biết trước và bạn muốn xác định khoảng tin cậy cho sự khác biệt giữa trung bình của chúng.
   - **3.3.2. Phương sai không biết nhưng bằng nhau (Unknown but Equal Variances):** Sử dụng khi cả hai quần thể có phương sai không biết nhưng có lẽ bằng nhau và bạn muốn xác định khoảng tin cậy cho sự khác biệt giữa trung bình của chúng.

4. **Tín lượng khoảng cho tỷ số của phương sai của hai quần thể chuẩn:**
   - **3.4. Confidence Interval for the Ratio of Variances of Two Normal Populations:** Sử dụng khi bạn muốn xác định khoảng tin cậy cho tỷ số của phương sai của hai quần thể chuẩn.

5. **Tín lượng khoảng cho trung bình của một biến ngẫu nhiên Bernoulli:**
   - **3.5. Confidence Interval for the Mean of a Bernoulli Random Variable:** Sử dụng khi bạn muốn xác định khoảng tin cậy cho trung bình của một biến ngẫu nhiên Bernoulli (ví dụ: xác suất thành công trong một loạt các thí nghiệm Bernoulli).

## Chapter 4: Parametric Hypothesis Testing
Dĩ nhiên! Đây là các khái niệm thường được sử dụng trong phân tích thống kê để kiểm tra các giả thuyết về trung bình, phương sai và xác suất của các quần thể phân phối chuẩn hoặc Bernoulli:

1. **Kiểm định liên quan đến trung bình của một quần thể chuẩn:**
   - **4.2.1. Độ lệch tiêu chuẩn đã biết (Known Standard Deviation):** Sử dụng khi độ lệch chuẩn của quần thể đã biết trước và bạn muốn kiểm tra giả thuyết về trung bình của quần thể.
   - **4.2.2. Độ lệch tiêu chuẩn chưa biết (Unknown Standard Deviation):** Sử dụng khi độ lệch chuẩn của quần thể không biết và bạn muốn kiểm tra giả thuyết về trung bình của quần thể.

2. **Kiểm định liên quan đến sự bằng nhau của hai trung bình của hai quần thể chuẩn:**
   - **4.3.1. Phương sai đã biết (Known Variances):** Sử dụng khi cả hai quần thể có phương sai đã biết trước và bạn muốn kiểm tra xem trung bình của chúng có bằng nhau hay không.
   - **4.3.2. Phương sai chưa biết nhưng bằng nhau (Unknown but Equal Variances):** Sử dụng khi cả hai quần thể có phương sai không biết nhưng có lẽ bằng nhau và bạn muốn kiểm tra xem trung bình của chúng có bằng nhau hay không.

3. **Kiểm định t-test ghép (Paired t-test):**
   - Sử dụng khi bạn muốn so sánh sự khác biệt giữa các cặp quan sát được đo trước và sau một can thiệp. Ví dụ: so sánh trọng lượng của một nhóm người trước và sau khi tham gia một chương trình giảm cân.

4. **Kiểm định liên quan đến phương sai của một quần thể chuẩn:**
   - **4.5. Test Concerning the Variance of a Normal Population:** Sử dụng để kiểm tra giả thuyết về phương sai của một quần thể chuẩn.

5. **Kiểm định liên quan đến sự bằng nhau của phương sai của hai quần thể chuẩn:**
   - **4.6. Test Concerning the Equality of Variances of Two Normal Populations:** Sử dụng để kiểm tra xem hai quần thể có phương sai bằng nhau hay không.

6. **Kiểm định liên quan đến P trong các quần thể Bernoulli:**
   - **4.7. Test Concerning P in Bernoulli Populations:** Sử dụng để kiểm tra giả thuyết về xác suất thành công (P) trong một quần thể Bernoulli.

7. **Kiểm định liên quan đến sự bằng nhau của P trong hai quần thể Bernoulli:**
   - **4.8. Test Concerning the Equality of P in Two Bernoulli Populations:** Sử dụng để kiểm tra xem xác suất thành công (P) có bằng nhau giữa hai quần thể Bernoulli hay không.
  
## Chapter 5: Statistical Hypothesis Testing

Dưới đây là giải thích cho mỗi khái niệm trong các phần của đoạn mà bạn đã đề cập:

1. **Kiểm tra tính chuẩn (Normality Tests):**
   - **5.1.1. Kiểm tra Shapiro-Wilk:** Sử dụng để kiểm tra xem một mẫu có tuân theo phân phối chuẩn hay không. 
   - **5.1.2. Kiểm tra D’Agostino:** Kiểm tra tính chuẩn của một mẫu dữ liệu bằng cách kiểm tra độ lệch và độ nhọn của phân phối.
   - **5.1.3. Kiểm tra Anderson-Darling:** Kiểm tra xem một mẫu có tuân theo một phân phối cụ thể hay không, thường được sử dụng để kiểm tra tính chuẩn.

2. **Kiểm tra tương quan (Correlation Tests):**
   - **5.2.1. Hệ số tương quan Pearson:** Đánh giá mối tương quan tuyến tính giữa hai biến liên tục.
   - **5.2.2. Tương quan hạng Spearman:** Đánh giá mối tương quan giữa hai biến dựa trên thứ hạng của các giá trị của chúng.
   - **5.2.3. Tương quan hạng Kendall:** Đánh giá mối tương quan giữa hai biến dựa trên thứ hạng của các giá trị của chúng.
   - **5.2.4. Kiểm định Chi-squared:** Sử dụng để kiểm tra xem hai biến phân loại có liên quan không.

3. **Kiểm tra tĩnh lặp (Stationary Tests):**
   - **5.3.1. Kiểm tra gốc đơn Dickey-Fuller tăng cường:** Sử dụng để kiểm tra xem một chuỗi thời gian có tính chất gốc đơn hay không.
   - **5.3.2. Kiểm tra Kwiatkowski-Phillips-Schmidt-Shin:** Sử dụng để kiểm tra xem một chuỗi thời gian có tính chất gốc đơn hay không.

4. **Các kiểm tra khác (Other Tests):**
   - **5.4.1. Kiểm định U Mann-Whitney:** Sử dụng để so sánh phân phối của hai mẫu độc lập khi dữ liệu không tuân theo phân phối chuẩn hoặc có sự nghi ngờ về sự độc lập của mẫu.
   - **5.4.2. Kiểm định Wilcoxon Signed-Rank:** Sử dụng để so sánh hai điều kiện hoặc thời điểm khác nhau của cùng một nhóm thí nghiệm khi dữ liệu không tuân theo phân phối chuẩn.
   - **5.4.3. Kiểm định Kruskal-Wallis H:** Sử dụng để kiểm tra xem có sự khác biệt giữa ba hoặc nhiều nhóm dữ liệu độc lập.
   - **5.4.4. Kiểm định Friedman:** Sử dụng để kiểm tra xem có sự khác biệt giữa ba hoặc nhiều điều kiện khác nhau của cùng một nhóm thí nghiệm.

## Chapter 6: Regression

1. **Ước lượng bằng phương pháp bình phương nhỏ nhất của các tham số hồi quy (Least Squares Estimators of the Regression Parameters):**
   - Các ước lượng bình phương nhỏ nhất là cách tiếp cận phổ biến nhất để ước lượng các tham số của mô hình hồi quy bằng cách tối thiểu hóa tổng bình phương của sai số giữa dữ liệu thực tế và giá trị được dự đoán bởi mô hình.

2. **Suy diễn thống kê về các tham số hồi quy (Statistical Inferences about the Regression Parameters):**
   - Suy diễn thống kê giúp đưa ra các kết luận về các tham số của mô hình hồi quy dựa trên dữ liệu mẫu.

3. **Các kiểm định t cho các tham số hồi quy với statsmodels (T-tests for Regression Parameters with statsmodels):**
   - Kiểm định t được sử dụng để kiểm tra xem các tham số của mô hình hồi quy có ý nghĩa thống kê hay không.

4. **F-statistic cho ý nghĩa tổng thể trong hồi quy (F-statistic for Overall Significance in Regression):**
   - F-statistic được sử dụng để kiểm tra ý nghĩa tổng thể của mô hình hồi quy, tức là xác định xem mô hình có tốt hơn so với một mô hình hồi quy không có biến độc lập không.

5. **Khoảng tin cậy liên quan đến các mô hình hồi quy (Confidence Intervals Concerning Regression Models):**
   - Khoảng tin cậy được sử dụng để ước lượng độ chính xác của các tham số trong mô hình hồi quy.

6. **Các giá trị còn lại (Residuals):**
   - Các giá trị còn lại là sai số giữa các giá trị thực tế và giá trị được dự đoán bởi mô hình hồi quy.

7. **Kiểm tra chẩn đoán hồi quy (Regression Diagnostic):**
   - Kiểm tra chẩn đoán được sử dụng để đánh giá sự phù hợp của mô hình hồi quy với dữ liệu, bao gồm kiểm tra tính đồng nhất của phương sai, phân phối của giá trị còn lại, và các điều kiện khác.

8. **Đa tuyến (Multicollinearity):**
   - Đa tuyến là hiện tượng khi hai hoặc nhiều biến độc lập trong mô hình hồi quy có mức độ tương quan cao, gây khó khăn trong việc ước lượng và diễn giải các ảnh hưởng riêng của từng biến.
  
## Chapter 7: Analysis of Variance (ANOVA)

1. **One-Way Analysis of Variance (ANOVA một chiều):**
   - **7.1.1. Equal Sample Sizes (Kích thước mẫu bằng nhau):** Trong trường hợp kích thước mẫu của tất cả các nhóm là như nhau, One-Way ANOVA được sử dụng để kiểm tra xem có sự khác biệt có ý nghĩa nào đối với ít nhất một trong các nhóm đó không.
   - **7.1.2. Unequal Sample Sizes (Kích thước mẫu không bằng nhau):** Trong trường hợp kích thước mẫu của các nhóm không đều nhau, One-Way ANOVA cũng có thể được sử dụng, nhưng một số điều chỉnh cần được thực hiện để đảm bảo tính chính xác của kết quả.

2. **Two-Way Analysis of Variance (ANOVA hai chiều):**
   - Two-Way ANOVA được sử dụng khi có hai yếu tố ảnh hưởng đến biến phụ thuộc. Ví dụ, nó có thể được sử dụng để kiểm tra sự ảnh hưởng của liều lượng và giới tính đến hiệu quả của một phương pháp điều trị. Trong phần này, không có sự phân chia cụ thể giữa kích thước mẫu bằng nhau và kích thước mẫu không bằng nhau như trong One-Way ANOVA. Thay vào đó, nó nghiên cứu sự ảnh hưởng của hai yếu tố trên kết quả.


**Dưới đây là tóm tắt một số dạng phổ biến của các phương pháp kiểm định:**

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
