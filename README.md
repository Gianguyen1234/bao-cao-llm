# Ghi Chú Khảo Sát: Danh Sách và Phân Tích Các LLM Miễn Phí

## Giới Thiệu
Bài viết này cung cấp danh sách đầy đủ các mô hình ngôn ngữ lớn (LLM) miễn phí, cùng với liên kết, cách sử dụng miễn phí, số token, và yêu cầu GPU. Các mô hình này được phát hành với các giấy phép mở, phù hợp cho cả nghiên cứu và sử dụng thương mại, với một số hạn chế nhất định. Dựa trên thông tin cập nhật đến ngày 26 tháng 3 năm 2025, chúng tôi phân tích chi tiết để giúp người dùng hiểu rõ hơn về cách tận dụng các công cụ AI này.

## Danh Sách Các LLM Miễn Phí

| Mô Hình  | Nhà Phát Triển | Giấy Phép | Liên Kết | Cách Sử Dụng Miễn Phí | Số Token | Yêu Cầu GPU |
|----------|---------------|-----------|---------|------------------|---------|-----------|
| **Llama** | Meta AI | Apache 2.0 | [Llama](https://ai.meta.com/llama/) | Tải xuống và chạy cục bộ trên GPU | Phụ thuộc kích thước mô hình | Cần GPU, lớn hơn cần VRAM cao hơn |
| **Mistral** | Mistral AI | Apache 2.0 | [Mistral](https://mistral.ai/) | Tải xuống và chạy cục bộ trên GPU | Phụ thuộc kích thước mô hình | Cần GPU, lớn hơn cần VRAM cao hơn |
| **Falcon** | EleutherAI | Apache 2.0 | [Falcon-7B](https://huggingface.co/EleutherAI/falcon-7b) | Tải xuống và chạy cục bộ trên GPU | Phụ thuộc kích thước mô hình | Cần GPU, lớn hơn cần VRAM cao hơn |
| **MPT** | MosaicML | Apache 2.0 | [MPT-7B](https://huggingface.co/mosaicml/mpt-7b) | Tải xuống và chạy cục bộ trên GPU | Phụ thuộc kích thước mô hình | Cần GPU, lớn hơn cần VRAM cao hơn |
| **BLOOM** | BigScience | BigScience RAIL v1.0 | [BLOOM](https://huggingface.co/bigscience/bloom) | Tải xuống và chạy cục bộ trên GPU, tuân thủ giấy phép | Phụ thuộc kích thước mô hình | Cần GPU, lớn hơn cần VRAM cao hơn |
| **Bert** | Google | Apache 2.0 | [Bert](https://huggingface.co/bert-base-uncased) | Tải xuống và chạy trên CPU hoặc GPU | Phụ thuộc kích thước mô hình | Mô hình nhỏ chạy trên CPU, lớn cần GPU |
| **GPT-2** | OpenAI | Modified MIT | [GPT-2](https://huggingface.co/gpt2) | Tải xuống và chạy cục bộ trên GPU | Phụ thuộc kích thước mô hình | Cần GPU, lớn hơn cần VRAM cao hơn |

Ngoài các mô hình trên, còn có một số mô hình khác như Dolly, StableLM, và Pythia, cũng miễn phí với giấy phép Apache 2.0, nhưng bài viết tập trung vào các mô hình chính được đề cập.

## Phân Tích Sử Dụng Miễn Phí

### Các bước sử dụng miễn phí
1. **Tải xuống trọng số mô hình** từ các liên kết trên (thường trên Hugging Face).
2. **Cài đặt môi trường** với các thư viện cần thiết, như `transformers` từ Hugging Face:
   ```bash
   pip install transformers
   ```
3. **Chạy mô hình cục bộ** trên máy tính, ví dụ với Llama:
   ```python
   from transformers import LlamaTokenizer, LlamaForCausalLM
   
   tokenizer = LlamaTokenizer.from_pretrained("meta-llama/Llama-2-7b-hf")
   model = LlamaForCausalLM.from_pretrained("meta-llama/Llama-2-7b-hf")
   ```
4. Một số mô hình có thể truy cập qua **API Inference của Hugging Face**, có tầng miễn phí với giới hạn sử dụng.
5. Để **sử dụng không giới hạn**, chạy cục bộ là lựa chọn tốt nhất nếu bạn có phần cứng phù hợp.

## Số Token và Giới Hạn
- **Token** là đơn vị văn bản mà mô hình xử lý.
- **Cửa sổ ngữ cảnh** (context window) tối đa, ví dụ Llama-2-7B có 4096 token.
- **Không có giới hạn khi chạy cục bộ**, nhưng API miễn phí có thể giới hạn số yêu cầu hoặc token mỗi tháng.

## Yêu Cầu GPU
- **Bert-base** (110 triệu tham số) có thể chạy trên CPU, nhưng tốc độ chậm.
- **Llama-7B** cần GPU với **ít nhất 16GB VRAM**.
- **Falcon-40B** có thể cần **40-50GB VRAM hoặc nhiều GPU**.

Ví dụ, để chạy **Llama-7B**, bạn cần GPU với ít nhất **16GB VRAM**, trong khi mô hình lớn hơn như **Llama-70B** có thể cần nhiều GPU hoặc phần cứng mạnh hơn.

## Thông Tin Bổ Sung
- **BLOOM** có giấy phép đặc biệt (BigScience RAIL License v1.0), với các hạn chế sử dụng như cấm sử dụng cho mục đích quản lý công lý, thực thi pháp luật, hoặc quy trình nhập cư.
- Ngoài chạy cục bộ, một số dịch vụ như **Hugging Face Inference API** có tầng miễn phí, nhưng giới hạn không rõ ràng.

## Kết Luận
Danh sách trên cung cấp các lựa chọn **LLM miễn phí**, phù hợp cho nhiều mục đích, từ nghiên cứu đến phát triển ứng dụng. Với phần cứng phù hợp, bạn có thể tận dụng sức mạnh của AI mà không tốn phí, nhưng cần chú ý đến **yêu cầu GPU** và **giới hạn giấy phép**.

## Key Citations
- [Llama official page](https://ai.meta.com/llama/)
- [Mistral AI official page](https://mistral.ai/)
- [Falcon 7B on Hugging Face](https://huggingface.co/EleutherAI/falcon-7b)
- [MPT 7B on Hugging Face](https://huggingface.co/mosaicml/mpt-7b)
- [BLOOM on Hugging Face](https://huggingface.co/bigscience/bloom)
- [Bert base uncased on Hugging Face](https://huggingface.co/bert-base-uncased)
- [GPT-2 on Hugging Face](https://huggingface.co/gpt2)
