# BÀI LÀM PHA 2 

- **Họ tên:Nguyễn Đức Hiếu**
- **Lớp:CNTT2**
- **Link repository Pha2:https://github.com/hn3443723-max/HN-KS26-CNTT2_KyNangPromptingVoiAI_H02_Pha2.git**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):ChatGPT**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```text
[{"ma_goi":"SVT","ngay_su_kien":"2026-12-20","nguoi_lon":2,"tre_em":1,"loai_ve":"thuong","ghi_chu":null},{"ma_goi":"FZ","ngay_su_kien":"2027-01-05","nguoi_lon":3,"tre_em":0,"loai_ve":"thuong","ghi_chu":"hỗ trợ xe lăn"},{"ma_goi":"VIP","ngay_su_kien":null,"nguoi_lon":4,"tre_em":0,"loai_ve":"vip","ghi_chu":"hỗ trợ tìm chỗ cho người khiếm thị"}]
```

**Link trò chuyện:https://chatgpt.com/share/6b05537c-b1f4-83ec-9232-ca083dfb57a4**

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
1. Tiền người lớn
   5 người lớn × 1.200.000 = 6.000.000 đồng
2. Tiền trẻ em
   Mỗi trẻ em từ 5–11 tuổi tính 70% giá người lớn:
   1.200.000 × 70% = 840.000 đồng/trẻ
   2 trẻ × 840.000 = 1.680.000 đồng
   Bé 3 tuổi: 0 đồng (miễn phí)
3. Tiền vé (tiền người lớn + tiền trẻ em)
   6.000.000 + 1.680.000 = 7.680.000 đồng
4. Giảm giá nhóm
   Có 5 người lớn nên được giảm 5%:
   7.680.000 × 5% = 384.000 đồng
   Tiền vé sau giảm = 7.680.000 − 384.000 = 7.296.000 đồng
5. Phụ thu
   1 người lớn chọn ghế ưu tiên:
   1 × 300.000 = 300.000 đồng
6. Tổng tiền
   7.296.000 + 300.000 = 7.596.000 đồng
[RESULT: 7.596.000 đồng]
```

**Link trò chuyện:https://chatgpt.com/share/6b05541e-1348-83ec-8446-44698c374d40**

### b) Kiểm tra kết quả AI

 Kết luận AI đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{"loai_su_co":"sai_khu_vuc","so_khach":2,"so_hiep_bi_anh_huong":2,"tom_tat":"Hai khách bị xếp vào khu không mái trong 2 hiệp đầu dù mua vé khu có mái."}
```

**Link trò chuyện:https://chatgpt.com/c/6b055480-d634-83ec-8248-e2cad992ab38**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**


| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
|---|---|---|---|
| Đúng thông tin | 0,0/5,0 | **Lỗi 1:** “Vé Sân Vận Động bên em giá 1.000.000đ/người” → Sai vì giá chuẩn SVT là **1.200.000 đồng/người lớn**. **Lỗi 2:** “Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh.” → Sai vì huỷ **từ 3 đến 6 ngày trước sự kiện chỉ được hoàn 50%**, không phải 100%. | **Câu sửa:** “Vé Sân Vận Động có giá 1.200.000 đồng/người lớn. Nếu anh huỷ trước trận 3 ngày thì được hoàn 50% giá trị vé.” |
| Đầy đủ | 2,0/3,0 | Nhân viên đã trả lời cả **giá vé** và **chính sách huỷ**, nhưng không thực hiện yêu cầu mời khán giả cung cấp **ngày trận đấu và số lượng vé để đặt**. | **Câu sửa:** “Anh vui lòng cung cấp ngày trận đấu và số lượng vé cần đặt để em hỗ trợ anh ạ.” |
| Giọng điệu | 1,0/2,0 | **Lỗi:** “xem rất đã luôn ạ” và “nha anh” → Cách diễn đạt khá suồng sã, chưa phù hợp hoàn toàn với phong cách tư vấn bán vé chuyên nghiệp. | **Câu sửa:** “Dạ, em rất sẵn lòng hỗ trợ anh. Anh vui lòng cho em biết ngày trận đấu và số lượng vé cần đặt ạ.” |
| **Tổng** | **3,0/10** | Bài làm sai cả **giá vé** và **mức hoàn tiền**, đồng thời thiếu thông tin cần thiết để tiếp tục đặt vé. | — |


**Link trò chuyện:https://chatgpt.com/c/6b0554ca-840c-83ec-adb5-5ed63a56cc1d**
