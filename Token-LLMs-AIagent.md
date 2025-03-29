## Key Points
- Nghiên cứu cho thấy token trong các mô hình ngôn ngữ lớn (LLM) là đơn vị nhỏ nhất của văn bản mà mô hình xử lý, thường là từ, ký tự hoặc tiểu từ, tùy thuộc vào phương pháp mã hóa.  
- Có vẻ như LLM đóng vai trò quan trọng trong các tác nhân AI (AI agents), cung cấp khả năng hiểu và tạo ngôn ngữ, giúp chúng tương tác với người dùng và thực hiện nhiệm vụ phức tạp.  
- Bằng chứng nghiêng về việc các tác nhân AI dựa trên LLM, như chatbot và trợ lý ảo, thường sử dụng token để xử lý và tạo phản hồi, tạo cầu nối giữa ngôn ngữ và hành động tự động.

---

## Giới thiệu về Token trong LLM và Mối Liên hệ với Tác nhân AI

### Token trong LLM
Token là các đơn vị cơ bản mà các mô hình ngôn ngữ lớn (LLM) sử dụng để xử lý và tạo văn bản. Chúng có thể là từ, ký tự hoặc tiểu từ, tùy thuộc vào phương pháp mã hóa được áp dụng. Có ba loại mã hóa chính:  
- **Mã hóa dựa trên từ**: Chia văn bản thành các từ, ví dụ "The quick brown fox" thành ['The', 'quick', 'brown', 'fox']. Phương pháp này dễ hiểu nhưng gặp khó khăn với từ hiếm hoặc không có trong từ điển.  
- **Mã hóa dựa trên ký tự**: Mỗi ký tự được coi là một token, ví dụ "The quick brown fox" thành ['T', 'h', 'e', ' ', 'q', 'u', 'i', 'c', 'k', ...]. Phương pháp này linh hoạt nhưng cần nhiều tài nguyên hơn do chuỗi dài.  
- **Mã hóa tiểu từ**: Phân tách từ thành các tiểu từ thường xuất hiện, ví dụ "vanquish" có thể thành ['van', 'qu', 'ish']. Phương pháp này, như Byte-Pair Encoding (BPE), giúp xử lý từ mới hiệu quả và được nhiều LLM hiện đại sử dụng.  

Token hóa quan trọng vì nó cho phép LLM xử lý văn bản đa dạng, bao gồm cả từ chưa từng thấy, bằng cách chia nhỏ chúng thành các đơn vị quen thuộc.  

### LLM và Tác nhân AI
Tác nhân AI là các hệ thống hoặc chương trình có thể tự động thực hiện nhiệm vụ, thường với một mức độ tự chủ, như chatbot hoặc trợ lý ảo. LLM đóng vai trò cốt lõi trong các tác nhân này, cung cấp khả năng hiểu và tạo ngôn ngữ để tương tác với người dùng.  
Ví dụ, một chatbot dựa trên LLM có thể trả lời câu hỏi của người dùng, trong khi một tác nhân lập kế hoạch có thể phân tích nhiệm vụ phức tạp, sử dụng công cụ và thực hiện hành động dựa trên ngôn ngữ. Các tác nhân này thường tích hợp thêm bộ nhớ, lập kế hoạch và sử dụng công cụ để mở rộng khả năng, như gọi API thời tiết để trả lời "Thời tiết ở Paris hôm nay thế nào?"  

### Ví dụ Bất Ngờ
Một chi tiết thú vị là các tác nhân AI dựa trên LLM không chỉ dừng lại ở ngôn ngữ mà còn có thể lập kế hoạch và thực hiện hành động, như tự động hóa quy trình trong nghiên cứu khoa học, chẳng hạn phát triển thuốc chống ung thư bằng cách truy vấn dữ liệu và lập kế hoạch thí nghiệm.  

---

## Báo cáo Chi tiết về Token trong LLM và Mối Liên hệ với Tác nhân AI

### Giới thiệu
Các mô hình ngôn ngữ lớn (LLM) là những hệ thống trí tuệ nhân tạo tiên tiến, được huấn luyện trên khối lượng lớn dữ liệu văn bản để hiểu và tạo ngôn ngữ con người. Các mô hình như GPT-3, GPT-4, BERT và LLaMA đã chứng minh khả năng vượt trội trong nhiều nhiệm vụ xử lý ngôn ngữ tự nhiên, bao gồm tạo văn bản, dịch thuật, tóm tắt và trả lời câu hỏi.  

### Token trong LLM: Định nghĩa và Phương pháp
Token là đơn vị nhỏ nhất mà LLM xử lý, đóng vai trò như các khối xây dựng để hiểu và tạo ngôn ngữ. Quá trình chuyển đổi văn bản thành token được gọi là token hóa, với các phương pháp chính như sau:  

| **Loại Mã hóa**         | **Mô tả**                                                                 | **Ví dụ**                                      |
|-------------------------|---------------------------------------------------------------------------|-----------------------------------------------|
| Dựa trên từ            | Chia văn bản thành các từ dựa trên khoảng trắng hoặc dấu câu.              | "The quick brown fox" → ['The', 'quick', 'brown', 'fox'] |
| Dựa trên ký tự         | Mỗi ký tự được coi là một token, cần chuỗi dài hơn để biểu diễn.           | "The quick brown fox" → ['T', 'h', 'e', ' ', 'q', ...] |
| Dựa trên tiểu từ       | Phân tách từ thành các tiểu từ thường xuất hiện, xử lý từ mới hiệu quả.    | "vanquish" → ['van', 'qu', 'ish']             |

Nhiều LLM hiện đại, như các mô hình sử dụng Byte-Pair Encoding (BPE), áp dụng mã hóa tiểu từ để cân bằng kích thước từ điển và khả năng xử lý từ hiếm hoặc chưa từng thấy. Ví dụ, từ "vanquish" có thể được chia thành các tiểu từ dựa trên tần suất xuất hiện, giúp mô hình linh hoạt hơn.  

Nghiên cứu cho thấy token hóa không chỉ ảnh hưởng đến hiệu suất mà còn liên quan đến cấu trúc ngôn ngữ, như sự tương đồng với đơn vị ngữ nghĩa nhỏ nhất (morpheme). Ví dụ, một số nghiên cứu cho thấy mã hóa dựa trên hình thái học (morphologically aware tokenization) có thể cải thiện khả năng xử lý từ mới, nhưng hiệu quả phụ thuộc vào ngôn ngữ, như tiếng Anh so với tiếng Đức ([Tokenization in large language models, explained](https://seantrott.substack.com/p/tokenization-in-large-language-models)).  

### Tác nhân AI: Định nghĩa và Vai trò của LLM
Tác nhân AI là các thực thể nhân tạo có thể tự động thực hiện nhiệm vụ, thường với mức độ tự chủ, từ chatbot đơn giản đến hệ thống lập kế hoạch phức tạp. LLM đóng vai trò cốt lõi trong các tác nhân này, cung cấp khả năng hiểu và tạo ngôn ngữ để tương tác với người dùng.  

Theo khảo sát, LLM-based AI agents thường được xây dựng với khung gồm ba thành phần chính: não bộ (brain, tức LLM), nhận thức (perception) và hành động (action), có thể tùy chỉnh cho nhiều ứng dụng ([The Rise and Potential of Large Language Model Based Agents: A Survey](https://arxiv.org/abs/2309.07864)). Ví dụ, một tác nhân AI có thể sử dụng LLM để phân tích câu hỏi, lập kế hoạch và gọi công cụ như API thời tiết để trả lời "Thời tiết ở Paris hôm nay thế nào?"  

### Ví dụ Thực tế về Tác nhân AI Dựa trên LLM
Có nhiều ví dụ minh họa cho tác nhân AI dựa trên LLM, bao gồm:  
- **Chatbot và Trợ lý Ảo**: Hỗ trợ khách hàng, trả lời câu hỏi, như chatbot trong ngành y tế cung cấp thông tin chẩn đoán dựa trên dữ liệu bệnh nhân ([Mastering LLM AI Agents: Building and Using AI Agents in Python with Real-World Use Cases](https://medium.com/@jagadeesan.ganesh/mastering-llm-ai-agents-building-and-using-ai-agents-in-python-with-real-world-use-cases-c578eb640e35)).  
- **Công cụ Tạo Nội dung**: Tự động tạo văn bản, như viết bài báo hoặc mã code, dựa trên yêu cầu người dùng.  
- **Trợ lý Nghiên cứu**: Tóm tắt thông tin, trả lời câu hỏi từ cơ sở dữ liệu lớn, hỗ trợ nghiên cứu khoa học.  
- **Tác nhân Lập kế hoạch**: Phân tích nhiệm vụ phức tạp, như lập kế hoạch thí nghiệm khoa học, như phát triển thuốc chống ung thư bằng cách truy vấn dữ liệu và lập kế hoạch hành động ([LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)).  

Các tác nhân này thường tích hợp thêm bộ nhớ, lập kế hoạch và sử dụng công cụ để mở rộng khả năng, như gọi API hoặc thực hiện mã code, giúp xử lý các nhiệm vụ đa bước.  

### Kết luận
Token là nền tảng cho hoạt động của LLM, cho phép chúng xử lý và tạo văn bản hiệu quả. LLM, đến lượt nó, là thành phần cốt lõi của nhiều tác nhân AI, đặc biệt trong các ứng dụng cần xử lý ngôn ngữ, như chatbot, trợ lý ảo và hệ thống lập kế hoạch. Hiểu rõ về token trong LLM và mối liên hệ với tác nhân AI là bước quan trọng để phát triển và ứng dụng công nghệ này, với tiềm năng lớn trong tương lai, đặc biệt trong nghiên cứu và tự động hóa.  

---

## Key Citations
- [Tokenization in large language models, explained](https://seantrott.substack.com/p/tokenization-in-large-language-models)  
- [The Rise and Potential of Large Language Model Based Agents: A Survey](https://arxiv.org/abs/2309.07864)  
- [What are AI agents?](https://www.ibm.com/think/topics/ai-agents)  
- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)  
- [Mastering LLM AI Agents: Building and Using AI Agents in Python with Real-World Use Cases](https://medium.com/@jagadeesan.ganesh/mastering-llm-ai-agents-building-and-using-ai-agents-in-python-with-real-world-use-cases-c578eb640e35)