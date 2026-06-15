# 📘 Ngày 8 - Điều Kiện (Conditional Statements)

## 🎯 Mục Tiêu Ngày 8

- Hiểu câu lệnh if/elif/else
- Sử dụng điều kiện boolean
- Lồng điều kiện
- Sử dụng toán tử logic

---

## 🔀 Câu Lệnh If/Elif/Else

### If - Nếu

```python
age = 20

if age >= 18:
    print('Bạn đủ tuổi thành niên')
```

### If/Else - Nếu...Nếu không

```python
age = 15

if age >= 18:
    print('Đủ tuổi')
else:
    print('Chưa đủ tuổi')
```

### If/Elif/Else - Nếu...Nếu khác...Nếu không

```python
score = 7.5

if score >= 8:
    print('Giỏi')
elif score >= 6.5:
    print('Khá')
elif score >= 5:
    print('Trung bình')
else:
    print('Yếu')
```

---

## 📊 Ví Dụ Điều Kiện

### Ví Dụ 1: Phân Loại Tuổi

```python
age = int(input('Nhập tuổi: '))

if age < 13:
    print('Trẻ em')
elif age < 18:
    print('Thiếu niên')
elif age < 60:
    print('Người lớn')
else:
    print('Người cao tuổi')
```

### Ví Dụ 2: Phân Loại Số

```python
number = int(input('Nhập số: '))

if number > 0:
    print('Số dương')
elif number < 0:
    print('Số âm')
else:
    print('Số không')
```

### Ví Dụ 3: Kiểm Tra Năm Nhuận

```python
year = int(input('Nhập năm: '))

if year % 4 == 0 and year % 100 != 0:
    print(f'{year} là năm nhuận')
elif year % 400 == 0:
    print(f'{year} là năm nhuận')
else:
    print(f'{year} không phải năm nhuận')
```

---

## 🔗 Lồng Điều Kiện (Nested If)

```python
age = 25
income = 15000000

if age >= 18:
    print('Đủ tuổi thành niên')
    
    if income >= 10000000:
        print('Thu nhập đủ cao')
        print('Đủ điều kiện vay tiền')
    else:
        print('Thu nhập không đủ')
else:
    print('Chưa thành niên')
```

---

## ✅ Điều Kiện Ternary (Inline If)

```python
age = 20
status = 'Thành niên' if age >= 18 else 'Chưa thành niên'
print(status)

# Ví dụ khác
x = 10
result = 'x dương' if x > 0 else 'x không dương'
print(result)
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Kiểm Tra Mật Khẩu

```python
password = input('Nhập mật khẩu: ')

if len(password) < 8:
    print('Mật khẩu quá ngắn')
elif not any(c.isupper() for c in password):
    print('Cần có chữ hoa')
elif not any(c.isdigit() for c in password):
    print('Cần có chữ số')
else:
    print('Mật khẩu mạnh ✓')
```

### Ví Dụ 2: Máy Tính Đơn Giản

```python
print('=== MÁY TÍNH ===')
a = float(input('Số thứ nhất: '))
op = input('Phép toán (+, -, *, /): ')
b = float(input('Số thứ hai: '))

if op == '+':
    result = a + b
elif op == '-':
    result = a - b
elif op == '*':
    result = a * b
elif op == '/':
    if b == 0:
        print('Lỗi: Chia cho 0')
    else:
        result = a / b
else:
    print('Phép toán không hợp lệ')
    result = None

if result is not None:
    print(f'Kết quả: {result}')
```

---

## 🚀 Tiếp Theo - Ngày 9

Ngày 9 bạn sẽ học:
- Vòng lặp For
- Vòng lặp While
- Break & Continue
