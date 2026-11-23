# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ TÀI CHÍNH CÁ NHÂN)

- **Họ tên:** Nguyễn Minh Tùng
- **Lớp:** CNTT3
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký hội thảo ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "DT",
    "ngay_hoi_thao": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "hang_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "CB",
    "ngay_hoi_thao": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "hang_ve": null,
    "ghi_chu": "người dùng xe lăn cần lối đi riêng"
  },
  {
    "ma_goi": "VIP",
    "ngay_hoi_thao": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "hang_ve": null,
    "ghi_chu": "người mắt kém cần ngồi bàn đầu gần màn hình chiếu"
  }
]
```

**Link trò chuyện:** https://share.gemini.google/tT4vuPqIkJWA

## 4.3. Báo giá vé hội thảo bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền người lớn: 4 × 1.500.000 = 6.000.000 đồng

Tiền trẻ em: 2 × (1.500.000 × 50%) + 1 × 0 = 1.500.000 đồng (Trẻ 8 và 11 tuổi tính 50% giá người lớn; bé 4 tuổi dưới 6 tuổi được miễn phí)

Tiền vé (tạm tính): 6.000.000 + 1.500.000 = 7.500.000 đồng

Giảm giá nhóm: 7.500.000 × 10% = 750.000 đồng (Nhóm có 4 người lớn, đủ điều kiện từ 4 người lớn trở lên nên được giảm 10% trên tổng tiền vé)

Phụ thu: 2 × 200.000 = 400.000 đồng (Phụ thu 2 bộ sổ tay lập kế hoạch tài chính cá nhân, không áp dụng giảm giá)

Tổng tiền: 7.500.000 - 750.000 + 400.000 = 7.150.000 đồng

[RESULT: 7.150.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/86UuUMOVFLI5

### b) Kiểm tra kết quả AI

AI đúng.

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_hiep_bi_anh_huong": 2,
  "tom_tat": "Khách hàng bị xếp ngồi ở dãy ghế phụ phía sau không có bàn viết trong 2 phiên đầu."
}
```

**Link trò chuyện:** https://share.gemini.google/vbKidIFKC0iG

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 5.0 / 5.0 | Bài làm đã cung cấp thông tin về giá vé (*"1.200.000đ/người"*) và chính sách hủy vé (*"báo huỷ trước 4 ngày thì bên em hoàn lại đủ 100% tiền vé"*). *(Lưu ý: Do đề bài chưa cung cấp bảng thông tin chuẩn đối chiếu của ban tổ chức nên tạm tính trọn điểm dựa trên việc nhân viên đã nêu đầy đủ hai dữ kiện này).* | Giữ nguyên thông tin (nếu khớp với quy định của BTC), nhưng cần điều chỉnh cách diễn đạt lại cho chuyên nghiệp:<br>

<br>*"Hiện tại, vé gói Đầu Tư có mức giá là 1.200.000 VNĐ/người. Trong trường hợp cần thay đổi kế hoạch, anh/chị vui lòng thông báo hủy trước ngày diễn ra sự kiện ít nhất 04 ngày để được hoàn lại 100% giá trị vé."* |
| **Đầy đủ (30%)** | 1.5 / 3.0 | - **Đạt:** Trả lời đủ 2 thông tin về giá vé và chính sách hủy vé.<br>

<br>- **Lỗi thiếu ý:** Toàn bộ đoạn phản hồi không có nội dung mời khách hàng cung cấp thông tin đăng ký (ngày hội thảo, số lượng vé). | Bổ sung câu kêu gọi hành động ở cuối tin nhắn:<br>

<br>*"Để bên em hỗ trợ giữ chỗ, anh/chị vui lòng cho biết ngày tham dự hội thảo dự kiến và số lượng vé muốn đăng ký ạ."* |
| **Giọng điệu (20%)** | 0.0 / 2.0 | - **Lỗi 1 (Suồng sã):** *"Dạ chào anh/chị nha!"*, *"nha, cứ yên tâm chốt đơn đi ạ!"* — Sử dụng trợ từ ("nha") và từ ngữ bán hàng thiếu trang trọng ("chốt đơn").<br>

<br>- **Lỗi 2 (Hứa hẹn lợi nhuận quá đà):** *"đi học về đầu tư chứng khoán lời khủng luôn ạ"* — Cam kết lợi nhuận ("lời khủng") sai quy tắc tư vấn tài chính/đầu tư, gây rủi ro uy tín cho tổ chức. | - Thay lời chào và kết bằng văn phong lịch sự: *"Kính chào anh/chị,"* và *"Anh/chị có thể hoàn toàn yên tâm khi đăng ký tham dự chương trình."*<br>

<br>- Thay thế câu cam kết lợi nhuận bằng giá trị thực tế của khóa học: *"Khóa học sẽ cung cấp các kiến thức và phương pháp đầu tư chứng khoán bài bản, thực tế."* |
| **TỔNG ĐIỂM** | **6.5 / 10** |  |  |
```

**Link trò chuyện:** https://share.gemini.google/EWn7mZliui6X
