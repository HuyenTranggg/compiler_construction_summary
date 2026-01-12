# 🚀 BỘ BÀI TẬP KPL BỔ SUNG - NÂNG CAO

## 📚 Tổng quan

Bộ bài tập này bổ sung **6 bài nâng cao** với độ khó tương đương hoặc nhỉnh hơn bài **tính giai thừa**, giúp bạn chuẩn bị tốt hơn cho kỳ thi.

---

## 📝 Danh sách bài tập bổ sung

| Bài | Tên bài | Độ khó | Kiến thức chính | File |
|-----|---------|--------|-----------------|------|
| 7 | USCLN (GCD) | ★★☆☆☆ | Thuật toán Euclid | `bai7_uscln_euclid.kpl` |
| 8 | BSCNN (LCM) | ★★☆☆☆ | GCD + công thức | `bai8_bscnn.kpl` |
| 9 | Số hoàn hảo | ★★☆☆☆ | Tìm ước + tích lũy | `bai9_so_hoan_hao.kpl` |
| 10 | Bảng cửu chương | ★☆☆☆☆ | Vòng lặp lồng | `bai10_bang_cuu_chuong.kpl` |
| 11 | Tổ hợp C(n,k) | ★★★☆☆ | 3 giai thừa | `bai11_to_hop_cnk.kpl` |
| 12 | Số Armstrong | ★★★☆☆ | Lũy thừa + chữ số | `bai12_so_armstrong.kpl` |

---

## 🎯 Phân loại theo mức độ

### 📗 Dễ (Tương đương giai thừa)
- **Bài 10**: Bảng cửu chương - Vòng lặp lồng cơ bản

### 📘 Trung bình (Ngang với giai thừa)
- **Bài 7**: USCLN - Thuật toán Euclid nổi tiếng
- **Bài 8**: BSCNN - Kết hợp với USCLN
- **Bài 9**: Số hoàn hảo - Tìm ước và cộng dồn

### 📙 Khó hơn một chút
- **Bài 11**: Tổ hợp C(n,k) - Tính 3 giai thừa
- **Bài 12**: Số Armstrong - Kết hợp nhiều kỹ thuật

---

## 💡 Kiến thức mới học được

### 1️⃣ Thuật toán Euclid (Bài 7, 8)
```pascal
(* Tìm USCLN của a và b *)
WHILE b > 0 DO
  BEGIN
    temp := a - a / b * b;  (* temp = a % b *)
    a := b;
    b := temp
  END;
(* Khi b = 0, a chính là USCLN *)
```

**Ứng dụng**:
- Rút gọn phân số
- Mật mã RSA
- Toán học số

### 2️⃣ Vòng lặp lồng nhau (Bài 10)
```pascal
FOR i := 1 TO n DO
  BEGIN
    FOR j := 1 TO 10 DO
      BEGIN
        (* Thực thi n × 10 lần *)
        CALL WRITEI(i * j)
      END
  END
```

**Ứng dụng**:
- Xử lý ma trận
- In bảng, hình
- Duyệt mảng 2D

### 3️⃣ Tính lũy thừa (Bài 12)
```pascal
(* Tính a^b *)
power := 1;
FOR i := 1 TO b DO
  power := power * a;
```

**Lưu ý**: KPL không có `pow()`, phải dùng vòng lặp!

### 4️⃣ Tích lũy giá trị (Bài 9, 11, 12)
```pascal
(* Cộng dồn *)
sum := 0;
FOR i := 1 TO n DO
  sum := sum + i;

(* Nhân dồn (giai thừa) *)
fact := 1;
FOR i := 1 TO n DO
  fact := fact * i;
```

---

## 🔥 Các bài QUAN TRỌNG cho thi

### ⭐⭐⭐ Rất quan trọng
- **Bài 7**: USCLN - Thuật toán kinh điển, hay ra thi
- **Bài 11**: Tổ hợp - Kết hợp nhiều kiến thức

### ⭐⭐ Quan trọng
- **Bài 9**: Số hoàn hảo - Pattern tìm ước phổ biến
- **Bài 10**: Bảng cửu chương - Vòng lặp lồng cơ bản

### ⭐ Tham khảo
- **Bài 8**: BSCNN - Dễ nếu biết USCLN
- **Bài 12**: Armstrong - Khó nhưng đẹp

---

## 📖 Lộ trình học (2 tuần)

### Tuần 1: Thuật toán cơ bản
**Ngày 1-2**: 
- ✅ Bài 7: USCLN (Hiểu thuật toán Euclid)
- ✅ Bài 8: BSCNN (Áp dụng USCLN)

**Ngày 3-4**:
- ✅ Bài 10: Bảng cửu chương (Vòng lặp lồng)
- ✅ Bài 9: Số hoàn hảo (Tìm ước)

### Tuần 2: Nâng cao
**Ngày 5-6**:
- ✅ Bài 11: Tổ hợp C(n,k) (Nhiều giai thừa)

**Ngày 7**:
- ✅ Bài 12: Armstrong (Thử thách)

---

## 🎓 Mẹo làm bài khó

### Mẹo 1: Chia nhỏ bài toán
```pascal
(* Bài tổ hợp C(n,k) *)
(* Thay vì nghĩ phức tạp, chia thành 3 bước: *)

(* Bước 1: Tính n! *)
factN := 1;
FOR i := 1 TO n DO
  factN := factN * i;

(* Bước 2: Tính k! *)
factK := 1;
FOR i := 1 TO k DO
  factK := factK * i;

(* Bước 3: Tính (n-k)! *)
factNK := 1;
FOR i := 1 TO n - k DO
  factNK := factNK * i;

(* Bước 4: Áp dụng công thức *)
result := factN / factK / factNK;
```

### Mẹo 2: Dùng biến temp để giữ giá trị gốc
```pascal
(* Cần dùng n nhiều lần nhưng n bị thay đổi? *)
temp := n;
(* ... tính toán với temp ... *)
(* n vẫn giữ nguyên để dùng sau *)
```

### Mẹo 3: Kiểm tra điều kiện đầu vào
```pascal
(* Luôn kiểm tra input hợp lệ *)
IF k > n THEN
  CALL WRITEC('L');  (* Lỗi *)
ELSE
  BEGIN
    (* Xử lý bình thường *)
  END
```

### Mẹo 4: Test từng bước
```pascal
(* In giá trị trung gian để debug *)
CALL WRITEC('D');
CALL WRITEC('e');
CALL WRITEC('b');
CALL WRITEC('u');
CALL WRITEC('g');
CALL WRITEC(':');
CALL WRITEI(temp);
CALL WRITELN;
```

---

## 🧪 Bài tập thực hành

### Bài tập 1: Sửa đổi bài USCLN
Viết hàm tính USCLN của 3 số a, b, c
```pascal
(* Gợi ý: GCD(a,b,c) = GCD(GCD(a,b), c) *)
```

### Bài tập 2: Cải tiến số hoàn hảo
Tối ưu bài 9 bằng cách chỉ duyệt đến `sqrt(n)`
```pascal
(* Gợi ý: Nếu i là ước thì n/i cũng là ước *)
```

### Bài tập 3: Biến thể Armstrong
Tìm tất cả số Armstrong từ 1 đến n
```pascal
(* Gợi ý: Vòng lặp ngoài FOR i := 1 TO n DO *)
```

---

## 📊 So sánh độ khó

| Bài tập | Vòng lặp | Điều kiện | Toán học | Tổng điểm |
|---------|----------|-----------|----------|-----------|
| Giai thừa | ★★☆☆☆ | ★☆☆☆☆ | ★☆☆☆☆ | ★★☆☆☆ |
| Bài 7: USCLN | ★★★☆☆ | ★★☆☆☆ | ★★☆☆☆ | ★★★☆☆ |
| Bài 11: C(n,k) | ★★★☆☆ | ★★☆☆☆ | ★★★☆☆ | ★★★☆☆ |
| Bài 12: Armstrong | ★★★★☆ | ★★☆☆☆ | ★★★★☆ | ★★★★☆ |

---

## ⚠️ Những lỗi thường gặp

### Lỗi 1: Quên reset biến tích lũy
```pascal
❌ SAI:
sum := 5;  (* Khởi tạo sai *)
FOR i := 1 TO n DO
  sum := sum + i;

✅ ĐÚNG:
sum := 0;  (* Luôn reset về 0 *)
FOR i := 1 TO n DO
  sum := sum + i;
```

### Lỗi 2: Chia trước khi nhân (tổ hợp)
```pascal
❌ SAI:
result := n / k / (n - k);  (* Chia nguyên mất độ chính xác *)

✅ ĐÚNG:
result := n / (k * (n - k));  (* Hoặc tính giai thừa riêng *)
```

### Lỗi 3: Không xử lý số âm
```pascal
❌ SAI:
WHILE n > 0 DO  (* Vòng lặp vô hạn nếu n < 0 *)

✅ ĐÚNG:
IF n < 0 THEN
  n := 0 - n;  (* Lấy giá trị tuyệt đối *)
WHILE n > 0 DO
```

---

## 🏆 Checklist trước kỳ thi (Bổ sung)

- [ ] Biết thuật toán Euclid tính USCLN
- [ ] Biết công thức BSCNN = (a×b) / GCD
- [ ] Biết cách tìm ước số
- [ ] Biết vòng lặp lồng nhau (nested loop)
- [ ] Biết tính lũy thừa bằng vòng lặp
- [ ] Biết tách chữ số: digit = n % 10
- [ ] Biết đếm chữ số
- [ ] Đã làm ít nhất 2 bài khó (11 hoặc 12)

---

## 📌 Tổng kết

### Bộ bài tập GỐC (Bài 1-6):
- Làm quen cú pháp KPL
- Pattern cơ bản (FOR, WHILE, IF)
- Độ khó: ★☆☆☆☆ đến ★★☆☆☆

### Bộ bài tập BỔ SUNG (Bài 7-12):
- Thuật toán nổi tiếng (Euclid)
- Kết hợp nhiều kỹ thuật
- Độ khó: ★★☆☆☆ đến ★★★★☆

### Tổng cộng: **12 bài tập hoàn chỉnh**
✅ Đủ để chuẩn bị tốt cho kỳ thi KPL!

---

## 🎯 Kế hoạch ôn tập 3 tuần

### Tuần 1: Cơ bản (Bài 1-6)
- Làm quen FOR, WHILE, IF
- Tập viết code KPL đúng cú pháp

### Tuần 2: Nâng cao (Bài 7-12)
- Học thuật toán Euclid
- Thực hành vòng lặp lồng
- Làm bài tổ hợp và Armstrong

### Tuần 3: Ôn tập tổng hợp
- Làm lại TẤT CẢ không nhìn code
- Tự viết biến thể của các bài
- Mock test với giới hạn thời gian

---

## 💪 Động viên

> "Thuật toán Euclid đã hơn 2300 năm tuổi nhưng vẫn là cách tốt nhất tính USCLN!"

> "Số Armstrong rất hiếm, nhưng code được thì bạn rất giỏi!"

> "12 bài tập = 12 pattern quan trọng = Đủ để ACE kỳ thi!"

---

## 🚀 Chúc bạn học tốt và thi đạt điểm cao!

Có thắc mắc gì cứ hỏi nhé! 😊
