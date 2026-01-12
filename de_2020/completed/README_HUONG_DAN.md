# 📚 BỘ BÀI TẬP LUYỆN KPL - CHUẨN BỊ CHO KỲ THI

## 🎯 Mục tiêu
Bộ bài tập này giúp bạn làm quen với cú pháp KPL thông qua 6 bài tập có độ khó tương đương **bài tính giai thừa**, phù hợp cho kỳ thi.

---

## 📝 Danh sách bài tập

| Bài | Tên bài | Độ khó | Kiến thức | File |
|-----|---------|--------|-----------|------|
| 1 | Tính tổng 1→n | ★☆☆☆☆ | FOR loop | `bai1_tinh_tong_1_den_n.kpl` |
| 2 | Kiểm tra số nguyên tố | ★★☆☆☆ | FOR + IF | `bai2_kiem_tra_so_nguyen_to.kpl` |
| 3 | Fibonacci thứ n | ★★☆☆☆ | WHILE + logic | `bai3_fibonacci.kpl` |
| 4 | Đếm chữ số | ★☆☆☆☆ | WHILE loop | `bai4_dem_chu_so.kpl` |
| 5 | Tổng chẵn/lẻ | ★☆☆☆☆ | FOR + IF | `bai5_tong_chan_le.kpl` |
| 6 | Đảo ngược số | ★★☆☆☆ | WHILE + math | `bai6_dao_nguoc_so.kpl` |

---

## 🔧 Cách sử dụng

### Bước 1: Biên dịch
```bash
cd "d:\2025.1\Chuong trinh dich\code\de_2020\completed"
kplc.exe bai1_tinh_tong_1_den_n.kpl
```

### Bước 2: Chạy chương trình
```bash
kplrun.exe bai1_tinh_tong_1_den_n
```

### Bước 3: Nhập dữ liệu
```
Nhap n: 5
Tong = 15
```

---

## 📖 Kiến thức quan trọng cần nhớ

### 1. Cấu trúc chương trình KPL
```pascal
PROGRAM TenChuongTrinh;

(* Khai báo hằng *)
CONST MAX = 100;

(* Khai báo biến *)
VAR x, y: INTEGER;
    c: CHAR;

(* Khai báo hàm/thủ tục *)
FUNCTION add(a, b: INTEGER): INTEGER;
BEGIN
  add := a + b
END;

(* Chương trình chính *)
BEGIN
  (* Các câu lệnh *)
END.
```

### 2. Các vòng lặp

#### FOR Loop
```pascal
FOR i := 1 TO n DO
  sum := sum + i;

(* Hoặc với BEGIN-END cho nhiều lệnh *)
FOR i := 1 TO n DO
  BEGIN
    sum := sum + i;
    CALL WRITEI(i)
  END
```

#### WHILE Loop
```pascal
WHILE n > 0 DO
  BEGIN
    n := n / 10;
    count := count + 1
  END
```

### 3. Câu lệnh điều kiện

```pascal
(* IF đơn giản *)
IF x > 0 THEN
  y := 1;

(* IF-ELSE *)
IF x > 0 THEN
  y := 1
ELSE
  y := -1;

(* IF lồng nhau *)
IF x > 0 THEN
  IF x < 10 THEN
    y := 1
  ELSE
    y := 2
ELSE
  y := 0
```

### 4. Phép toán quan trọng

```pascal
(* Phép chia lấy phần nguyên *)
a := 7 / 2;  (* a = 3 *)

(* Phép chia lấy dư (modulo) *)
remainder := n - n / 10 * 10;  (* n % 10 *)

(* Giá trị tuyệt đối *)
IF x < 0 THEN
  x := 0 - x;  (* x = -x *)
```

### 5. Nhập/Xuất dữ liệu

```pascal
(* Nhập số nguyên *)
CALL READI(n);

(* Nhập ký tự *)
CALL READC(c);

(* Xuất số nguyên *)
CALL WRITEI(n);

(* Xuất ký tự *)
CALL WRITEC('A');

(* Xuất dòng mới *)
CALL WRITELN;
```

---

## 💡 Mẹo làm bài thi

### 1. Đọc kỹ đề bài
- Xác định input/output
- Xác định công thức/thuật toán
- Liệt kê các bước giải quyết

### 2. Viết code theo template
```pascal
PROGRAM TenBai;

VAR (* Khai báo biến *);

BEGIN
  (* Bước 1: Nhập dữ liệu *)
  
  (* Bước 2: Xử lý *)
  
  (* Bước 3: Xuất kết quả *)
END.
```

### 3. Kiểm tra các trường hợp đặc biệt
- n = 0
- n < 0 (số âm)
- n = 1
- Giá trị lớn

### 4. Debug
- In giá trị biến trung gian
- Kiểm tra logic từng bước
- Test với nhiều input khác nhau

---

## 🎓 Lộ trình học

### Tuần 1: Làm quen cú pháp
- ✅ Bài 1: Tính tổng (FOR loop cơ bản)
- ✅ Bài 4: Đếm chữ số (WHILE loop)
- ✅ Bài 5: Tổng chẵn/lẻ (FOR + IF)

### Tuần 2: Nâng cao
- ✅ Bài 2: Số nguyên tố (Logic phức tạp)
- ✅ Bài 3: Fibonacci (Kỹ thuật trượt)
- ✅ Bài 6: Đảo ngược số (Xây dựng số)

### Tuần 3: Ôn tập
- Làm lại tất cả bài không nhìn code
- Viết thêm test case
- Thử biến thể khác của bài

---

## ❓ Câu hỏi thường gặp

### Q1: KPL có hỗ trợ mảng không?
**A:** Có! Cú pháp:
```pascal
VAR arr: ARRAY [10] OF INTEGER;
BEGIN
  arr[0] := 5;
  CALL WRITEI(arr[0])
END.
```

### Q2: Làm sao in chuỗi trong KPL?
**A:** KPL không có kiểu STRING, phải in từng ký tự:
```pascal
CALL WRITEC('H');
CALL WRITEC('e');
CALL WRITEC('l');
CALL WRITEC('l');
CALL WRITEC('o');
```

### Q3: KPL có hỗ trợ đệ quy không?
**A:** Có! Ví dụ giai thừa đệ quy:
```pascal
FUNCTION factorial(n: INTEGER): INTEGER;
BEGIN
  IF n = 0 THEN
    factorial := 1
  ELSE
    factorial := n * factorial(n - 1)
END;
```

### Q4: Làm sao kiểm tra chẵn/lẻ?
**A:** Dùng phép modulo:
```pascal
IF n - n / 2 * 2 = 0 THEN
  (* n chẵn *)
ELSE
  (* n lẻ *)
```

---

## 📌 Checklist trước kỳ thi

- [ ] Biết cú pháp vòng lặp FOR, WHILE
- [ ] Biết cấu trúc IF-THEN-ELSE
- [ ] Biết khai báo biến, hằng, hàm
- [ ] Biết nhập/xuất dữ liệu (READI, WRITEI, WRITEC)
- [ ] Biết phép toán modulo (n % m)
- [ ] Biết xử lý số âm, số 0
- [ ] Biết BEGIN-END để nhóm lệnh
- [ ] Đã làm ít nhất 3 bài không nhìn code

---

## 🚀 Chúc bạn ôn tập tốt và đạt điểm cao!

**Lưu ý**: Tất cả bài tập đều có comment chi tiết giải thích từng bước. Hãy đọc kỹ comment để hiểu logic!
