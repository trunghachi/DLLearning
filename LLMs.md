# [Large Language Models](https://www.manning.com/books/build-a-large-language-model-from-scratch)
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/269260be-6e47-48c9-a8f7-0bd1a55aa083" alt="LLMs"  style="width:100%; height:100%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 1.1. Cây đời của các mô hình ngôn ngữ lớn (LLMs).</p>
    </td>
  </tr>
</table>

## 1 Hiểu về mô hình ngôn ngữ lớn (LLMs)
Các mô hình ngôn ngữ lớn (LLMs) như ChatGPT của OpenAI đã cách mạng hóa Xử lý Ngôn ngữ Tự nhiên (NLP) bằng cách xuất sắc trong các nhiệm vụ ngôn ngữ phức tạp mà các mô hình truyền thống không thể xử lý. Các LLM này là các mạng neural tiên tiến được huấn luyện trên lượng lớn dữ liệu văn bản, cho phép chúng hiểu, tạo và diễn giải ngôn ngữ con người với khả năng xuất sắc. Khác với các mô hình NLP trước đây chỉ tập trung vào các nhiệm vụ cụ thể, LLMs thể hiện khả năng rộng rãi trong nhiều nhiệm vụ NLP nhờ kiến trúc transformer và các tiến bộ trong học sâu. Chương này nhằm đặt nền tảng để hiểu và triển khai một LLM giống ChatGPT dựa trên kiến trúc transformer.
### 1.1 LLM là gì?
Một mô hình ngôn ngữ lớn (LLM) là một mạng neural được thiết kế để hiểu, tạo ra và phản hồi văn bản giống con người. Các mô hình này là các mạng neural sâu được huấn luyện trên lượng lớn dữ liệu văn bản, đôi khi bao gồm cả phần lớn văn bản có sẵn trên internet. Từ "lớn" trong LLM đề cập đến cả kích thước của mô hình với hàng chục hoặc hàng trăm tỷ tham số, và tập dữ liệu khổng lồ mà nó được huấn luyện. Các tham số này được tối ưu hóa trong quá trình huấn luyện để dự đoán từ tiếp theo trong một chuỗi, tận dụng tính tuần tự của ngôn ngữ để hiểu ngữ cảnh, cấu trúc và các mối quan hệ trong văn bản.

LLMs sử dụng kiến trúc transformer, cho phép chúng tập trung vào các phần khác nhau của đầu vào khi đưa ra dự đoán, giúp chúng xử lý tốt các phức tạp của ngôn ngữ. LLMs là một dạng trí tuệ nhân tạo (AI) tạo sinh, có khả năng tạo văn bản và thực hiện các nhiệm vụ đòi hỏi trí thông minh giống con người như hiểu ngôn ngữ, nhận dạng mẫu và đưa ra quyết định. Chương này sẽ thảo luận và triển khai quy trình huấn luyện từ tiếp theo từng bước một.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/28dda535-2a38-41e9-b7ca-749e946c8773" alt="LLMs"  style="width:50%; height:50%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 1.2. Các mô hình ngôn ngữ lớn (LLM) là một ứng dụng cụ thể của các kỹ thuật học sâu, sử dụng khả năng xử lý và tạo văn bản giống như con người. Học sâu là một nhánh chuyên biệt của học máy, tập trung vào việc sử dụng các mạng nơ-ron nhiều lớp. Cả học máy và học sâu đều nhằm mục đích triển khai các thuật toán cho phép máy tính học từ dữ liệu và thực hiện các nhiệm vụ thường yêu cầu trí tuệ con người.</p>
    </td>
  </tr>
</table>

Triển khai **AI** dựa vào các thuật toán **Học máy**, học từ dữ liệu để dự đoán hoặc ra quyết định mà không cần lập trình từng bước tường minh. Ví dụ, bộ lọc thư rác sử dụng **ML** để phân loại email dựa trên các ví dụ được gán nhãn, giảm thiểu sai sót để nhận diện mẫu thư rác. **DL**, một phần của Học máy sử dụng mạng nơ-ron với nhiều lớp, tự động hóa nhận diện mẫu phức tạp mà không cần trích xuất đặc trưng thủ công. **AI** cũng bao gồm các hệ thống dựa trên quy tắc (_rule-based systems_), thuật toán di truyền (_genetic algorithms_), hệ chuyên gia (_expert systems_), logic mờ (_fuzzy logic_) và suy luận biểu tượng (_symbolic reasoning_). Khác với các phương pháp truyền thống yêu cầu trích xuất đặc trưng thủ công, Học sâu tối ưu hóa quá trình này.

Các phần tiếp theo sẽ khám phá các _ứng dụng_ hiện tại, _thách thức_ và _kiến trúc_ của các **mô hình ngôn ngữ lớn** (LLMs) được thảo luận trong tài liệu này.
### 1.2 Ứng dụng của LLMs
**LLMs**, với khả năng phân tích văn bản tiên tiến, có rất nhiều ứng dụng khác nhau trong các lĩnh vực đa dạng. Chúng **xuất sắc** trong các nhiệm vụ như _dịch máy_, _tạo ra văn bản mới_, _phân tích cảm xúc_ và _tóm tắt thông tin_. Gần đây, chúng còn được sử dụng để tạo nội dung như _viết truyện_ và _mã nguồn_ máy tính. LLMs cũng điều hành các _chatbot_ và _trợ lý ảo_ phức tạp có thể trả lời câu hỏi và _cải tiến các công cụ tìm kiếm_ truyền thống.

Trong các lĩnh vực chuyên môn như y học hoặc luật pháp, LLMs xuất sắc trong việc truy xuất và tóm tắt lượng lớn dữ liệu văn bản, làm cho chúng không thể thiếu trong các nhiệm vụ tự động hóa liên quan đến phân tích và tạo ra văn bản. Khi chúng ta khám phá các ứng dụng mới, LLMs có tiềm năng tái định nghĩa cách chúng ta tương tác với công nghệ, khiến cho nó trở nên hội thoại và trực quan hơn.

Trong tài liệu này, chúng ta sẽ tìm hiểu sâu về các khái niệm cơ bản của LLMs, bao gồm **lập trình một LLM** có thể tạo ra văn bản và khám phá các kỹ thuật để truy vấn, tóm tắt, dịch và nhiều ứng dụng khác. Qua các bước thực hành, chúng ta sẽ hiểu được cách các trợ lý LLMs phức tạp như ChatGPT hoạt động, mở ra những ứng dụng đổi mới trong các lĩnh vực khác nhau.

### 1.3 Các bước để xây dựng và sử dụng LLMs
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

Hai cách phổ biến nhất của việc điều chỉnh lại LLM bao gồm **điều chỉnh theo hướng dẫn** (instruction-finetuning) và điều chỉnh cho các tác vụ phân loại (finetuning for classification). Trong điều chỉnh theo hướng dẫn, tập dữ liệu đã được gán nhãn bao gồm các _cặp hướng dẫn và câu trả lời_, ví dụ như các truy vấn dịch văn bản kèm theo văn bản đã được dịch đúng. Trong điều chỉnh cho các nhiệm vụ phân loại, tập dữ liệu đã được gán nhãn bao gồm các _văn bản và nhãn lớp tương ứng_, ví dụ như email được gán nhãn là thư rác hoặc không phải thư rác.

Trong tài liệu này, chúng ta sẽ bao gồm cả việc lập trình tiền huấn luyện và điều chỉnh lại LLM, và chúng ta sẽ đi sâu vào các chi tiết cụ thể của điều chỉnh theo hướng dẫn và điều chỉnh cho các tác vụ phân loại sau khi tiền huấn luyện một LLM cơ bản.

### 1.4 Sử dụng LLMs cho các tác vụ khác nhau
Hầu hết các LLMs hiện đại sử dụng kiến trúc **transformer**, được giới thiệu trong bài báo năm 2017 "_Attention Is All You Need_". Ban đầu phát triển cho dịch máy, transformers bao gồm các mô-đun mã hóa và giải mã nối tiếp bởi **cơ chế tự chú ý** (self-attention). Các cơ chế này cho phép LLMs đánh giá sự quan trọng của các từ trong chuỗi, nắm bắt các phụ thuộc xa và nâng cao khả năng hiểu bối cảnh.

**BERT**, một biến thể của transformers, chuyên sâu trong việc dự đoán từ được ẩn trong câu và xuất sắc trong các nhiệm vụ như phân loại văn bản, phân tích cảm xúc và kiểm duyệt nội dung trên các nền tảng như Twitter.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/24bfe2b2-2124-4ba4-a9b4-2fe9ab355d92" alt="Transformer"  style="width:50%; height:50%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 1.4. Mô hình transformer gốc là một mô hình học sâu được thiết kế cho dịch ngôn ngữ. Nó bao gồm hai thành phần chính: bộ mã hóa, xử lý văn bản đầu vào để tạo ra một biểu diễn số học toàn diện (embedding), và bộ giải mã, sử dụng biểu diễn này để tạo ra văn bản dịch từng từ một. Bộ mã hóa bắt các chiều khác nhau của văn bản đầu vào, giúp bộ giải mã hoàn thành các bản dịch một cách hiệu quả, như minh họa trong hình vẽ nơi bộ giải mã tạo ra từ cuối cùng ("Beispiel") dựa trên văn bản đầu vào ("This is an example") và một câu dịch một phần ("Das ist ein"). </p>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/e317cda2-0ba8-4692-aaf1-a50c631acf68" alt="Transformer2"  style="width:50%; height:50%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 1.5. Một biểu đồ minh họa về các mô-đun mã hóa và giải mã của transformer. Ở bên trái, phần mã hóa mô tả các LLMs giống như BERT, tập trung vào dự đoán từ bị ẩn và chủ yếu được sử dụng cho các nhiệm vụ như phân loại văn bản. Ở bên phải, phần giải mã cho thấy các LLMs giống như GPT, được thiết kế cho các nhiệm vụ tạo sinh và tạo ra các chuỗi văn bản logic. </p>
    </td>
  </tr>
</table>

GPT, mặt khác, chỉ tập trung vào phần giải mã của kiến trúc transformer gốc và được thiết kế cho các nhiệm vụ yêu cầu tạo ra văn bản. Điều này bao gồm dịch máy, tóm tắt văn bản, viết truyện, viết mã máy tính và nhiều nhiệm vụ khác. Chúng ta sẽ thảo luận về kiến trúc GPT chi tiết hơn trong các phần còn lại của chương này và thực hiện từ đầu trong cuốn sách này.

Các mô hình GPT, được thiết kế và huấn luyện chủ yếu để thực hiện các nhiệm vụ hoàn thành văn bản, cũng thể hiện sự linh hoạt đáng kể trong khả năng của chúng. Các mô hình này khá thành thạo trong việc thực hiện các nhiệm vụ học không có mẫu (zero-shot) và học một vài mẫu (few-shot). Học không có mẫu đề cập đến khả năng tổng quát hóa cho các nhiệm vụ hoàn toàn chưa từng thấy mà không cần bất kỳ ví dụ cụ thể trước đó. Trong khi đó, học một vài mẫu liên quan đến việc học từ một số lượng tối thiểu các ví dụ mà người dùng cung cấp như đầu vào, như được minh họa trong Hình 1.6.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/f25f234b-70ad-4244-9426-6d2860cdd427" alt="fewshot"  style="width:50%; height:50%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 1.6. Ngoài việc hoàn thành văn bản, các LLMs giống như GPT cũng có thể giải quyết nhiều nhiệm vụ dựa trên dữ liệu đầu vào của chúng mà không cần thiết phải huấn luyện lại, điều chỉnh lại, hoặc thay đổi kiến trúc mô hình cụ thể cho từng nhiệm vụ. Đôi khi, việc cung cấp ví dụ của mục tiêu trong dữ liệu đầu vào được biết đến là thiết lập một vài mẫu. Tuy nhiên, các LLMs giống như GPT cũng có khả năng thực hiện các nhiệm vụ mà không cần ví dụ cụ thể, được gọi là thiết lập không có mẫu. </p>
    </td>
  </tr>
</table>

#### Transformers vs LLMs
Các LLM hiện nay chủ yếu dựa trên kiến trúc transformer được giới thiệu trong phần trước. Do đó, trong văn học, các thuật ngữ "transformers" và "LLMs" thường được sử dụng thay thế cho nhau. Tuy nhiên, cần lưu ý rằng không phải tất cả các transformers đều là LLMs, vì transformers cũng có thể được áp dụng vào các nhiệm vụ trong thị giác máy tính. Ngược lại, không phải tất cả các LLMs đều dựa trên transformers; một số sử dụng các kiến trúc tuần hoàn hoặc tích chập. Mục đích chính của những phương pháp thay thế này là cải thiện hiệu suất tính toán của LLMs. Việc liệu những kiến trúc LLM thay thế này có thể cạnh tranh với các khả năng của LLMs dựa trên transformer và liệu chúng sẽ được áp dụng rộng rãi trong thực tế hay không vẫn còn là một câu hỏi. (Độc giả quan tâm có thể tìm thấy các tài liệu tham khảo mô tả các kiến trúc này trong phần Đọc thêm ở cuối chương này.)

### 1.5 Sử dụng các bộ dữ liệu lớn
### 1.6 Kiến trúc GPT
### 1.7 Xây dựng một LLM từ đầu
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/5d099a4d-9432-4f71-aa41-f8d521a7bc47" alt="LLM"  style="width:50%; height:50%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 1.9. Các bước xây dựng và triển khai một LLM ví dụ. </p>
    </td>
  </tr>
</table>

Trong chương này, chúng ta đã đặt nền tảng để hiểu về các mô hình ngôn ngữ lớn (LLMs). Trong phần còn lại của cuốn sách, chúng ta sẽ lập trình một LLM từ đầu. Chúng ta sẽ lấy ý tưởng cơ bản đằng sau GPT làm bản thiết kế và thực hiện điều này trong ba giai đoạn.

- **Giai đoạn 1**: Tìm hiểu về các bước tiền xử lý dữ liệu cơ bản và lập trình cơ chế attention, thành phần cốt lõi của mọi LLM.
- **Giai đoạn 2**: Lập trình và huấn luyện trước một LLM tương tự GPT có khả năng tạo ra văn bản mới và tìm hiểu về cách đánh giá LLM. Việc huấn luyện trước một LLM lớn từ đầu đòi hỏi chi phí tính toán rất lớn, vì vậy giai đoạn này sẽ tập trung vào việc huấn luyện cho mục đích giáo dục với tập dữ liệu nhỏ. Cuốn sách cũng sẽ cung cấp các ví dụ về cách tải trọng số của các mô hình có sẵn.
- **Giai đoạn 3**: Sử dụng một LLM đã được huấn luyện trước và tinh chỉnh nó để thực hiện các nhiệm vụ như trả lời câu hỏi hoặc phân loại văn bản, những nhiệm vụ phổ biến nhất trong các ứng dụng thực tế và nghiên cứu.
### 1.8 Tổng kết
Các mô hình ngôn ngữ lớn (LLMs) đã biến đổi lĩnh vực xử lý ngôn ngữ tự nhiên, trước đây chủ yếu dựa vào các hệ thống dựa trên quy tắc rõ ràng và các phương pháp thống kê đơn giản hơn. Sự ra đời của LLMs đã mang đến các phương pháp mới dựa trên học sâu, góp phần đẩy mạnh sự hiểu biết, tạo ra và dịch ngôn ngữ con người.

Các LLM hiện đại được huấn luyện theo hai bước chính. Đầu tiên, chúng được huấn luyện trước trên một tập dữ liệu lớn chứa văn bản không gán nhãn bằng cách dự đoán từ tiếp theo trong câu như một "nhãn". Sau đó, chúng được điều chỉnh lại trên một tập dữ liệu mục tiêu nhỏ hơn, có nhãn để thực hiện các hướng dẫn hoặc nhiệm vụ phân loại.

LLMs dựa trên kiến trúc transformer. Ý tưởng chính của kiến trúc transformer là cơ chế attention, cho phép LLM có quyền truy cập chọn lọc vào toàn bộ chuỗi đầu vào khi tạo ra đầu ra từng từ một.

Kiến trúc gốc của transformer bao gồm một bộ mã hóa để phân tích văn bản và một bộ giải mã để tạo ra văn bản.

LLMs để tạo ra văn bản và tuân theo hướng dẫn, chẳng hạn như GPT-3 và ChatGPT, chỉ thực hiện các mô-đun giải mã, đơn giản hóa kiến trúc.

Tập dữ liệu lớn bao gồm hàng tỷ từ là cần thiết cho việc huấn luyện trước LLMs. Trong cuốn sách này, chúng tôi sẽ thực hiện và huấn luyện LLMs trên các tập dữ liệu nhỏ cho mục đích giáo dục nhưng cũng xem xét cách chúng ta có thể tải trọng số mô hình có sẵn.

Trong khi nhiệm vụ huấn luyện trước chung cho các mô hình giống GPT là dự đoán từ tiếp theo trong câu, những LLM này có các thuộc tính "phát sinh" như khả năng phân loại, dịch hoặc tóm tắt văn bản.

Khi một LLM được huấn luyện trước, mô hình cơ sở kết quả có thể được điều chỉnh tinh tế hơn cho các nhiệm vụ phụ thuộc dòng chảy.

LLMs được điều chỉnh lại trên các tập dữ liệu tùy chỉnh có thể vượt trội hơn so với LLMs chung trên các nhiệm vụ cụ thể.
