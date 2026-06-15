# 💻 Bài Tập Ngày 8

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: If/Else Cơ Bản

Tạo file `day_8_if_basics.py`:

```python
# Ngày 8 - Điều Kiện

# If cơ bản
age = 20
if age >= 18:
    print('Bạn đủ tuổi')

# If/Else
score = 7
if score >= 8:
    print('Giỏi')
else:
    print('Không giỏi')

# If/Elif/Else
number = 0
if number > 0:
    print('Dương')
elif number < 0:
    print('Âm')
else:
    print('Không')
```

---

### Bài 1.2: Điều Kiện Phức Tạp

```python
# Với and/or
age = 25
income = 15000000

if age >= 18 and income >= 10000000:
    print('Đủ điều kiện vay')
else:
    print('Không đủ điều kiện')

# Với or
status = 'student'
if status == 'student' or status == 'employee':
    print('Có bảo hiểm')
else:
    print('Không có bảo hiểm')
```

---

### Bài 1.3: Ternary If

```python
# Inline if
age = 20
msg = 'Thành niên' if age >= 18 else 'Chưa thành niên'
print(msg)

# Với số
x = 10
result = 'Dương' if x > 0 else 'Không dương'
print(result)
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Phân Loại Điểm

Tạo file `day_8_grading.py`:

```python
# Phân loại điểm

print("=== PHÂN LOẠI ĐIỂM ===\n")

score = float(input("Nhập điểm (0-100): "))

# Kiểm tra hợp lệ
if score < 0 or score > 100:
    print("Điểm không hợp lệ")
elif score >= 9:
    grade = 'A+'
    label = 'Xuất sắc'
elif score >= 8.5:
    grade = 'A'
    label = 'Rất tốt'
elif score >= 8:
    grade = 'A-'
    label = 'Tốt'
elif score >= 7:
    grade = 'B'
    label = 'Khá'
elif score >= 6:
    grade = 'C'
    label = 'Trung bình'
else:
    grade = 'D'
    label = 'Yếu'

print(f"Điểm: {score}")
print(f"Xếp loại: {grade} ({label})")
```

---

### Bài 2.2: Kiểm Tra Năm Nhuận

```python
# Kiểm tra năm nhuận

year = int(input("Nhập năm: "))

if year % 400 == 0:
    is_leap = True
elif year % 100 == 0:
    is_leap = False
elif year % 4 == 0:
    is_leap = True
else:
    is_leap = False

if is_leap:
    print(f"{year} là năm nhuận")
    print("Tháng 2 có 29 ngày")
else:
    print(f"{year} không phải năm nhuận")
    print("Tháng 2 có 28 ngày")
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Máy Tính Đơn Giản

Tạo file `day_8_calculator.py`:

```python
# Máy tính đơn giản

print("=== MÁY TÍNH ===\n")

num1 = float(input("Số thứ nhất: "))
op = input("Phép toán (+, -, *, /): ")
num2 = float(input("Số thứ hai: "))

result = None

if op == '+':
    result = num1 + num2
elif op == '-':
    result = num1 - num2
elif op == '*':
    result = num1 * num2
elif op == '/':
    if num2 == 0:
        print("Lỗi: Không thể chia cho 0")
    else:
        result = num1 / num2
else:
    print("Phép toán không hợp lệ")

if result is not None:
    print(f"\n{num1} {op} {num2} = {result}")
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Sử dụng if cơ bản
- [ ] Sử dụng if/else
- [ ] Sử dụng if/elif/else
- [ ] Kết hợp and/or
- [ ] Lồng if
- [ ] Ternary if
- [ ] Hoàn thành bài cơ bản
- [ ] Hoàn thành bài nâng cao
- [ ] Hoàn thành thách thức

---

## 💡 Mẹo Quan Trọng

**1. If/Elif/Else:**
```python
if condition1:
    # code
elif condition2:
    # code
else:
    # code
```

**2. Logic operators:**
```python
if x > 0 and x < 10:  # cả hai đúng
    pass

if x < 0 or x > 100:  # ít nhất một đúng
    pass
```

**3. Ternary:**
```python
x = 5
msg = 'Dương' if x > 0 else 'Không dương'
```
