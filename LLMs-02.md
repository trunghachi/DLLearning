# [Large Language Models](https://www.manning.com/books/build-a-large-language-model-from-scratch)
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/269260be-6e47-48c9-a8f7-0bd1a55aa083" alt="LLMs"  style="width:100%; height:100%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 2.0. Cây đời của các mô hình ngôn ngữ lớn (LLMs).</p>
    </td>
  </tr>
</table>

## 2 Chuẩn bị dữ liệu text 
Trong phần này: 
1. Chuẩn bị văn bản cho việc huấn luyện mô hình ngôn ngữ lớn:
2. Chia văn bản thành các từ và các token con
3. Mã hóa byte pair (byte pair encoding) như một cách nâng cao hơn để token hóa văn bản
4. Lấy mẫu các ví dụ huấn luyện bằng phương pháp cửa sổ trượt (sliding window approach)
5. Chuyển đổi các token thành các vector để đưa vào mô hình ngôn ngữ lớn

Trong chương trước, chúng ta đã tìm hiểu về cấu trúc chung của các mô hình ngôn ngữ lớn (LLMs) và biết rằng chúng được huấn luyện trước trên một lượng lớn văn bản. Cụ thể, chúng ta tập trung vào các LLM chỉ sử dụng bộ giải mã dựa trên kiến trúc transformer, nền tảng của các mô hình như ChatGPT và các LLM giống GPT khác.

Trong giai đoạn huấn luyện trước, các LLM xử lý văn bản từng từ một. Việc huấn luyện các LLM với hàng triệu đến hàng tỷ tham số bằng nhiệm vụ dự đoán từ tiếp theo tạo ra các mô hình có khả năng ấn tượng. Các mô hình này sau đó có thể được điều chỉnh lại để tuân theo các hướng dẫn chung hoặc thực hiện các nhiệm vụ mục tiêu cụ thể. Tuy nhiên, trước khi chúng ta có thể triển khai và huấn luyện LLMs trong các chương tới, chúng ta cần chuẩn bị tập dữ liệu huấn luyện, đây là nội dung chính của chương này, như minh họa trong Hình 2.1.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/trunghachi/DLLearning/assets/45091486/70f37544-0e38-4aee-b45a-716b5ad3f5d7" alt="LLMs"  style="width:100%; height:100%;">
      <br>
      <p style="font-family: Arial, sans-serif; font-size: smaller; font-style: italic; text-align: center;">Hình 2.1.  Chương này chỉ tập trung vào phần chuẩn bị dữ liệu và sampling để đưa vào pretrain LLM.</p>
    </td>
  </tr>
</table>
