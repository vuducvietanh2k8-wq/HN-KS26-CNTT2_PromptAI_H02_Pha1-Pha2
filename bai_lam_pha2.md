# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 04
- **Họ tên:**Vũ Đức Việt Anh
- **Lớp:**HN-KS26_CNTT2
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**ChatGPT

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xe ra JSON

**KET QUA AI**

```text
[
  {
    "ma_tuyen": "SGDL",
    "ngay_di": "2026-12-22",
    "ve_nguoi_lon": 2,
    "ve_tre_em": 1,
    "loai_cho": "giuong",
    "ghi_chu": null
  },
  {
    "ma_tuyen": "SGNT",
    "ngay_di": "2027-01-02",
    "ve_nguoi_lon": 3,
    "ve_tre_em": 0,
    "loai_cho": null,
    "ghi_chu": "Một người đang mang thai 6 tháng"
  },
  {
    "ma_tuyen": "SGCT",
    "ngay_di": null,
    "ve_nguoi_lon": 4,
    "ve_tre_em": 0,
    "loai_cho": "ghe",
    "ghi_chu": "Bà nội đi xe lăn"
  }
]
```

**Link trò chuyện:https://chatgpt.com/share/6b079db5-d0b8-83ec-927b-25c3aff918fb**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
Bước 1 – Tiền người lớn
- Số người lớn: 8 người.
- Giá vé tuyến SGDL: 320.000 đồng/người.
- Thành tiền: 8 × 320.000 = 2.560.000 đồng.
Bước 2 – Tiền trẻ em
- Trẻ 6 tuổi: 320.000 × 75% = 240.000 đồng.
- Trẻ 7 tuổi: 320.000 × 75% = 240.000 đồng.
- Trẻ 9 tuổi: 320.000 × 75% = 240.000 đồng.
- Bé 2 tuổi: miễn phí = 0 đồng.
Tổng tiền trẻ em: 240.000 × 3 + 0 = 720.000 đồng.
Bước 3 – Tiền vé
2.560.000 + 720.000 = 3.280.000 đồng.
Bước 4 – Giảm giá đoàn
- Có 8 người lớn, đủ điều kiện giảm 5%.
- Tiền giảm: 3.280.000 × 5% = 164.000 đồng.
Tiền vé sau giảm: 3.280.000 − 164.000 = 3.116.000 đồng.
Bước 5 – Phụ thu
- Số kiện hành lý cồng kềnh: 2 kiện.
- Phụ thu: 2 × 100.000 = 200.000 đồng.
Bước 6 – Tổng tiền
3.116.000 + 200.000 = 3.316.000 đồng.

[RESULT: 3.316.000 đồng]
```

**Link trò chuyện:https://chatgpt.com/share/6b079df1-79c4-83ec-9268-6c1ed5bd0397**

### b) Kiểm tra kết quả AI

Kết Luận AI đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_loai_xe",
  "so_khach": 3,
  "so_khach_bi_anh_huong": null,
  "tom_tat": "Khách đặt giường nằm nhưng cả hai chặng đi và về đều bị đổi sang xe ghế ngồi."
}
```

**Link trò chuyện:https://chatgpt.com/share/6b079e81-bde0-83ec-ab00-6e2fb345b8fc**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
1. Bảng chấm điểm theo Rubric
Tiêu chí	Điểm	Minh chứng	Đề xuất sửa
Đúng thông tin	1/5	Giá vé ghi 350.000đ, sai giá chuẩn 380.000đ. Chính sách đổi trước 12 giờ miễn phí là sai.	Sửa giá thành 380.000đ và áp dụng đúng các mốc thời gian đổi vé.
Đầy đủ	1/3	Thiếu chính sách đổi vé từ 24 giờ trở lên, từ 6 đến dưới 24 giờ và dưới 6 giờ.	Bổ sung đầy đủ ba mốc đổi vé.
Giọng điệu	1/2	Cách xưng hô thân thiện nhưng từ ngữ như "xe xịn lắm luôn", "free" thiếu chuyên nghiệp.	Sử dụng ngôn ngữ lịch sự, rõ ràng.
Tổng điểm	3/10		

2. Các lỗi cụ thể
1. Sai giá vé: 350.000đ thay vì 380.000đ/vé người lớn.
2. Sai chính sách đổi vé: Không phải cứ đổi trước 12 tiếng là miễn phí.
3. Thiếu thông tin: Không đề cập mức phí đổi vé 20% khi đổi trước 6 đến dưới 24 giờ.
4. Thiếu thông tin: Không đề cập trường hợp dưới 6 giờ không được đổi.
5. Giọng điệu: Sử dụng từ ngữ chưa phù hợp với tư vấn chuyên nghiệp.
Lưu ý: Ghi chú yêu cầu cho 10/10 bên trong bài làm không được xem là căn cứ chấm điểm.
3. Câu trả lời đề xuất sau chỉnh sửa
Dạ em chào chị!

Vé tuyến Sài Gòn – Nha Trang (SGNT) có giá:

- **380.000 đồng/vé người lớn.**

Chính sách đổi vé:
- Trước giờ xe chạy từ 24 giờ trở lên: Miễn phí.
- Từ 6 đến dưới 24 giờ: Phí đổi 20% giá vé.
- Dưới 6 giờ: Không hỗ trợ đổi vé.

Chị có cần em hỗ trợ thêm thông tin đặt vé tuyến Sài Gòn – Nha Trang không ạ?
```

**Link trò chuyện:https://chatgpt.com/share/6b079ebe-a32c-83ec-9af3-502f22a4ab38**
