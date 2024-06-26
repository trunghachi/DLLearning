# [Large Language Models](https://www.manning.com/books/build-a-large-language-model-from-scratch)
![image](https://github.com/trunghachi/DLLearning/assets/45091486/269260be-6e47-48c9-a8f7-0bd1a55aa083)


## 1. Hiểu về mô hình ngôn ngữ lớn (LLMs)
Các mô hình ngôn ngữ lớn (LLMs) như ChatGPT của OpenAI đã cách mạng hóa Xử lý Ngôn ngữ Tự nhiên (NLP) bằng cách xuất sắc trong các nhiệm vụ ngôn ngữ phức tạp mà các mô hình truyền thống không thể xử lý. Các LLM này là các mạng neural tiên tiến được huấn luyện trên lượng lớn dữ liệu văn bản, cho phép chúng hiểu, tạo và diễn giải ngôn ngữ con người với khả năng xuất sắc. Khác với các mô hình NLP trước đây chỉ tập trung vào các nhiệm vụ cụ thể, LLMs thể hiện khả năng rộng rãi trong nhiều nhiệm vụ NLP nhờ kiến trúc transformer và các tiến bộ trong học sâu. Chương này nhằm đặt nền tảng để hiểu và triển khai một LLM giống ChatGPT dựa trên kiến trúc transformer.
### 1.1. LLM là gì?
Một mô hình ngôn ngữ lớn (LLM) là một mạng neural được thiết kế để hiểu, tạo ra và phản hồi văn bản giống con người. Các mô hình này là các mạng neural sâu được huấn luyện trên lượng lớn dữ liệu văn bản, đôi khi bao gồm cả phần lớn văn bản có sẵn trên internet. Từ "lớn" trong LLM đề cập đến cả kích thước của mô hình với hàng chục hoặc hàng trăm tỷ tham số, và tập dữ liệu khổng lồ mà nó được huấn luyện. Các tham số này được tối ưu hóa trong quá trình huấn luyện để dự đoán từ tiếp theo trong một chuỗi, tận dụng tính tuần tự của ngôn ngữ để hiểu ngữ cảnh, cấu trúc và các mối quan hệ trong văn bản.

LLMs sử dụng kiến trúc transformer, cho phép chúng tập trung vào các phần khác nhau của đầu vào khi đưa ra dự đoán, giúp chúng xử lý tốt các phức tạp của ngôn ngữ. LLMs là một dạng trí tuệ nhân tạo (AI) tạo sinh, có khả năng tạo văn bản và thực hiện các nhiệm vụ đòi hỏi trí thông minh giống con người như hiểu ngôn ngữ, nhận dạng mẫu và đưa ra quyết định. Chương này sẽ thảo luận và triển khai quy trình huấn luyện từ tiếp theo từng bước một.

<table>
  <tr>
    <td align="center">
      <img src="https://media.licdn.com/dms/image/D4E10AQF_Xuqi7XOKVA/image-shrink_800/0/1713776419761?e=1719554400&v=beta&t=d6oC7_APCBlssJi8pZJNFWDdNr_26TE2M6veclgS78A" alt="LLMs"  style="width:50%; height:50%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 1.2. Các mô hình ngôn ngữ lớn (LLM) là một ứng dụng cụ thể của các kỹ thuật học sâu, sử dụng khả năng xử lý và tạo văn bản giống như con người. Học sâu là một nhánh chuyên biệt của học máy, tập trung vào việc sử dụng các mạng nơ-ron nhiều lớp. Cả học máy và học sâu đều nhằm mục đích triển khai các thuật toán cho phép máy tính học từ dữ liệu và thực hiện các nhiệm vụ thường yêu cầu trí tuệ con người.</p>
    </td>
  </tr>
</table>

Triển khai **AI** dựa vào các thuật toán **Học máy**, học từ dữ liệu để dự đoán hoặc ra quyết định mà không cần lập trình từng bước tường minh. Ví dụ, bộ lọc thư rác sử dụng **ML** để phân loại email dựa trên các ví dụ được gán nhãn, giảm thiểu sai sót để nhận diện mẫu thư rác. **DL**, một phần của Học máy sử dụng mạng nơ-ron với nhiều lớp, tự động hóa nhận diện mẫu phức tạp mà không cần trích xuất đặc trưng thủ công. **AI** cũng bao gồm các hệ thống dựa trên quy tắc (_rule-based systems_), thuật toán di truyền (_genetic algorithms_), hệ chuyên gia (_expert systems_), logic mờ (_fuzzy logic_) và suy luận biểu tượng (_symbolic reasoning_). Khác với các phương pháp truyền thống yêu cầu trích xuất đặc trưng thủ công, Học sâu tối ưu hóa quá trình này.

Các phần tiếp theo sẽ khám phá các _ứng dụng_ hiện tại, _thách thức_ và _kiến trúc_ của các **mô hình ngôn ngữ lớn** (LLMs) được thảo luận trong tài liệu này.
### 1.2. Ứng dụng của LLMs
**LLMs**, với khả năng phân tích văn bản tiên tiến, có rất nhiều ứng dụng khác nhau trong các lĩnh vực đa dạng. Chúng **xuất sắc** trong các nhiệm vụ như _dịch máy_, _tạo ra văn bản mới_, _phân tích cảm xúc_ và _tóm tắt thông tin_. Gần đây, chúng còn được sử dụng để tạo nội dung như _viết truyện_ và _mã nguồn_ máy tính. LLMs cũng điều hành các _chatbot_ và _trợ lý ảo_ phức tạp có thể trả lời câu hỏi và _cải tiến các công cụ tìm kiếm_ truyền thống.

Trong các lĩnh vực chuyên môn như y học hoặc luật pháp, LLMs xuất sắc trong việc truy xuất và tóm tắt lượng lớn dữ liệu văn bản, làm cho chúng không thể thiếu trong các nhiệm vụ tự động hóa liên quan đến phân tích và tạo ra văn bản. Khi chúng ta khám phá các ứng dụng mới, LLMs có tiềm năng tái định nghĩa cách chúng ta tương tác với công nghệ, khiến cho nó trở nên hội thoại và trực quan hơn.

Trong tài liệu này, chúng ta sẽ tìm hiểu sâu về các khái niệm cơ bản của LLMs, bao gồm **lập trình một LLM** có thể tạo ra văn bản và khám phá các kỹ thuật để truy vấn, tóm tắt, dịch và nhiều ứng dụng khác. Qua các bước thực hành, chúng ta sẽ hiểu được cách các trợ lý LLMs phức tạp như ChatGPT hoạt động, mở ra những ứng dụng đổi mới trong các lĩnh vực khác nhau.

### 1.3. Các bước để xây dựng và sử dụng LLMs
Tại sao chúng ta nên tự xây dựng các LLMs? Xây dựng các LLMs tùy chỉnh từ đầu giúp chúng ta hiểu rõ cơ chế và giới hạn của chúng, và chuẩn bị cho việc tiền huấn luyện hoặc điều chỉnh lại các mô hình hiện có để phù hợp với các bộ dữ liệu hoặc nhiệm vụ cụ thể. Các LLMs chuyên biệt cho các lĩnh vực cụ thể thường vượt trội so với các mô hình đa dụng như ChatGPT, ví dụ như BloombergGPT cho tài chính hoặc các LLMs để trả lời câu hỏi y học.

Quá trình tổng quát của việc tạo ra một LLM bao gồm hai giai đoạn chính: tiền huấn luyện và điều chỉnh lại. Thuật ngữ "tiền" trong "tiền huấn luyện" đề cập đến giai đoạn ban đầu khi một mô hình như LLM được huấn luyện trên một tập dữ liệu lớn và đa dạng để phát triển một hiểu biết rộng về ngôn ngữ. Mô hình được tiền huấn luyện này sau đó trở thành một nguồn tài nguyên cơ bản có thể được tinh chỉnh thêm qua quá trình điều chỉnh lại, trong đó mô hình được huấn luyện cụ thể trên một tập dữ liệu hẹp hơn phù hợp với các nhiệm vụ hoặc lĩnh vực cụ thể. Phương pháp huấn luyện hai giai đoạn này được minh họa trong Hình 1.3.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/5e20ee36-2e07-47eb-88a6-a0c3885b6da1" alt="LLMs"  style="width:50%; height:50%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 1.3. Tiền huấn luyện một LLM bao gồm việc dự đoán từ tiếp theo trong các chuỗi từ tập dữ liệu văn bản lớn. Sau khi tiền huấn luyện, LLM có thể được điều chỉnh lại bằng cách sử dụng một tập dữ liệu nhỏ hơn và đã được gán nhãn để điều chỉnh chức năng của nó cho các nhiệm vụ hoặc lĩnh vực cụ thể. </p>
    </td>
  </tr>
</table>
