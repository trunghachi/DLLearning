# [Large Language Models](https://www.manning.com/books/build-a-large-language-model-from-scratch)
![image](https://github.com/trunghachi/DLLearning/assets/45091486/269260be-6e47-48c9-a8f7-0bd1a55aa083)


## 1. Hiểu về mô hình ngôn ngữ lớn (LLMs)
Các mô hình ngôn ngữ lớn (LLMs) như ChatGPT của OpenAI đã cách mạng hóa Xử lý Ngôn ngữ Tự nhiên (NLP) bằng cách xuất sắc trong các nhiệm vụ ngôn ngữ phức tạp mà các mô hình truyền thống không thể xử lý. Các LLM này là các mạng neural tiên tiến được huấn luyện trên lượng lớn dữ liệu văn bản, cho phép chúng hiểu, tạo và diễn giải ngôn ngữ con người với khả năng xuất sắc. Khác với các mô hình NLP trước đây chỉ tập trung vào các nhiệm vụ cụ thể, LLMs thể hiện khả năng rộng rãi trong nhiều nhiệm vụ NLP nhờ kiến trúc transformer và các tiến bộ trong học sâu. Chương này nhằm đặt nền tảng để hiểu và triển khai một LLM giống ChatGPT dựa trên kiến trúc transformer.

Một mô hình ngôn ngữ lớn (LLM) là một mạng neural được thiết kế để hiểu, tạo ra và phản hồi văn bản giống con người. Các mô hình này là các mạng neural sâu được huấn luyện trên lượng lớn dữ liệu văn bản, đôi khi bao gồm cả phần lớn văn bản có sẵn trên internet. Từ "lớn" trong LLM đề cập đến cả kích thước của mô hình với hàng chục hoặc hàng trăm tỷ tham số, và tập dữ liệu khổng lồ mà nó được huấn luyện. Các tham số này được tối ưu hóa trong quá trình huấn luyện để dự đoán từ tiếp theo trong một chuỗi, tận dụng tính tuần tự của ngôn ngữ để hiểu ngữ cảnh, cấu trúc và các mối quan hệ trong văn bản.

LLMs sử dụng kiến trúc transformer, cho phép chúng tập trung vào các phần khác nhau của đầu vào khi đưa ra dự đoán, giúp chúng xử lý tốt các phức tạp của ngôn ngữ. LLMs là một dạng trí tuệ nhân tạo (AI) tạo sinh, có khả năng tạo văn bản và thực hiện các nhiệm vụ đòi hỏi trí thông minh giống con người như hiểu ngôn ngữ, nhận dạng mẫu và đưa ra quyết định. Chương này sẽ thảo luận và triển khai quy trình huấn luyện từ tiếp theo từng bước một.

<div style="text-align:center;">
    <img src="https://media.licdn.com/dms/image/D4E10AQF_Xuqi7XOKVA/image-shrink_800/0/1713776419761?e=1719554400&v=beta&t=d6oC7_APCBlssJi8pZJNFWDdNr_26TE2M6veclgS78A" alt="LLMs" style="width:50%; height:50%;">
    <figcaption>Hình 1.2. Các mô hình ngôn ngữ lớn (LLM) là một ứng dụng cụ thể của các kỹ thuật học sâu, sử dụng khả năng xử lý và tạo văn bản giống như con người. Học sâu là một nhánh chuyên biệt của học máy, tập trung vào việc sử dụng các mạng nơ-ron nhiều lớp. Cả học máy và học sâu đều nhằm mục đích triển khai các thuật toán cho phép máy tính học từ dữ liệu và thực hiện các nhiệm vụ thường yêu cầu trí tuệ con người.</figcaption>
</div>

