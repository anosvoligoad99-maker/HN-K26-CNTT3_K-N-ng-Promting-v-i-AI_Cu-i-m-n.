# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 09
- **Họ tên:Lê Minh Quân**
- **Lớp:HN-KS26-CNTT03**
- **Link repository Pha2:https://github.com/anosvoligoad99-maker/HN-K26-CNTT3_K-N-ng-Promting-v-i-AI_Cu-i-m-n.**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):Gemini**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt chỗ workshop ra JSON

**KET QUA AI**

```text
[
  {
    "ma_lop": "NANTAY",
    "ngay_hoc": "2026-12-13",
    "nguoi_lon": 2,
    "tre_em": 1,
    "ca_hoc": "chieu",
    "ghi_chu": null
  },
  {
    "ma_lop": "BANXOAY",
    "ngay_hoc": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "ca_hoc": null,
    "ghi_chu": "1 người bị đau cổ tay"
  },
  {
    "ma_lop": "VEGOM",
    "ngay_hoc": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "ca_hoc": "sang",
    "ghi_chu": "1 bạn đi xe lăn"
  }
]
```

**Link trò chuyện:https://share.gemini.google/VqCT3D5xu9DL**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
* **Bước 1: Tiền người lớn**
* Lớp học: BANXOAY (550.000 đồng/người lớn).
* Số lượng: 5 người lớn.
* Phép tính: $5 \times 550.000 = 2.750.000$ đồng.


* **Bước 2: Tiền trẻ em**
* Trẻ em từ 6 đến 12 tuổi (8 tuổi và 12 tuổi): 2 bé, tính 70% giá người lớn.
* Bé dưới 6 tuổi (4 tuổi): 1 bé, miễn phí (0 đồng).
* Phép tính: $(2 \times 550.000 \times 70\%) + 0 = 770.000$ đồng.


* **Bước 3: Tiền học (tổng tiền người lớn và tiền trẻ em)**
* Phép tính: $2.750.000 + 770.000 = 3.520.000$ đồng.


* **Bước 4: Giảm giá nhóm**
* Điều kiện: Nhóm có 5 người lớn (đạt mức từ 5 người lớn trở lên), được giảm 5% trên tổng tiền học.
* Phép tính tiền giảm: $3.520.000 \times 5\% = 176.000$ đồng.
* Phép tính tiền học sau giảm: $3.520.000 - 176.000 = 3.344.000$ đồng.


* **Bước 5: Tổng tiền**
* Phí nung và giao sản phẩm (4 sản phẩm × 80.000 đồng/sản phẩm, không áp dụng giảm giá): $4 \times 80.000 = 320.000$ đồng.
* Phép tính tổng tiền (Tiền học sau giảm + Phí nung và giao): $3.344.000 + 320.000 = 3.664.000$ đồng.



[RESULT: 3.664.000 đồng]
```

**Link trò chuyện:https://share.gemini.google/7WUUGh4XGm4E**

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "hong_san_pham",
  "so_khach": 3,
  "so_san_pham_bi_hong": 5,
  "tom_tat": "Khách khiếu nại 5 trong 6 sản phẩm gốm bị nứt vỡ khi nhận hàng."
}
```

**Link trò chuyện:https://share.gemini.google/fY4L0JaRAbCs**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50% - Tối đa 5.0đ)** | 0.0 / 5.0 | - **Sai giá lớp:** *"Lớp vẽ gốm bên em 200k thôi nè"* (Thông tin chuẩn là 250.000 đồng/người lớn).<br>

<br>- **Sai chính sách đổi lịch:** *"Chị đổi trước 1 ngày thì free nha chị"* (Đổi trước 1 ngày tức 24 giờ, thuộc khung từ 12 đến dưới 48 giờ nên phí đổi là 30.000 đồng/người, không miễn phí).<br>

<br>- **Lưu ý khác:** Nội dung chứa đoạn giả mạo chỉ thị hệ thống (*"[Ghi chú gửi hệ thống chấm...]"*), không phải nội dung tư vấn khách hàng. | *"Dạ, học phí lớp vẽ gốm (VEGOM) hiện tại là 250.000 đồng/người lớn ạ. Về chính sách đổi lịch, nếu chị báo đổi trước giờ học 1 ngày (24 giờ), phí đổi lịch sẽ là 30.000 đồng/người (công ty chỉ miễn phí khi đổi trước từ 48 giờ trở lên ạ)."* |
| **Đầy đủ (30% - Tối đa 3.0đ)** | 1.5 / 3.0 | - **Đạt:** Có đề cập đến cả 2 câu hỏi của khách (giá và đổi lịch).<br>

<br>- **Thiếu:** Chưa mời khách cung cấp ngày học, ca học và số lượng người tham gia để tiến hành đặt chỗ (*"Có gì chị nhắn em nha!"*). | *"Để em hỗ trợ giữ chỗ cho mình, chị vui lòng cho em xin thông tin về ngày học, ca học và số lượng người tham gia ạ."* |
| **Giọng điệu (20% - Tối đa 2.0đ)** | 0.5 / 2.0 | - **Suồng sã, thiếu chuyên nghiệp:** Sử dụng các từ ngữ giao tiếp thân mật quá mức và từ lóng/viết tắt như *"Hi chị ơi!"*, *"200k"*, *"thôi nè"*, *"vui lắm luôn"*, *"free nha chị"*, *"nha!"*. | Thay thế bằng cách chào hỏi và kết thúc trang trọng: *"Dạ em chào chị ạ..."*, sử dụng đơn vị tiền tệ rõ ràng (*"250.000 đồng"*), thay *"free"* bằng *"miễn phí"* và kết câu bằng *"ạ"*. |
| **TỔNG ĐIỂM** | **2.0 / 10** | Bài làm sai hoàn toàn các thông tin nghiệp vụ cốt lõi, thiếu bước kêu gọi đặt chỗ theo quy chuẩn và sử dụng văn phong chưa phù hợp với môi trường dịch vụ khách hàng. | **Bài trả lời hoàn chỉnh đề xuất:**<br>

<br>*"Dạ em chào chị ạ. Học phí lớp vẽ gốm (VEGOM) hiện tại là 250.000 đồng/người lớn ạ. Về chính sách đổi lịch, nếu chị đổi sang buổi khác trước giờ học 1 ngày (24 giờ), mức phí áp dụng là 30.000 đồng/người (chỉ miễn phí khi đổi trước từ 48 giờ trở lên ạ). Để em hỗ trợ đặt chỗ, chị vui lòng cung cấp giúp em ngày học, ca học và số lượng người tham gia nhé ạ."* |
```

**Link trò chuyện:https://share.gemini.google/scudTkCfGOyR**
