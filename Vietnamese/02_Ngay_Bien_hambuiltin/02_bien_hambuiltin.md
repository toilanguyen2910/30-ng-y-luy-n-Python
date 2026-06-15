# 📘 Ngày 2 - Biến và Hàm Built-in

## 🎯 Mục Tiêu Ngày 2

- Hiểu biến là gì
- Đặt tên biến đúng
- Học các hàm built-in quan trọng
- Sử dụng input() nhận dữ liệu từ người dùng
- Chuyển đổi kiểu dữ liệu

---

## 📌 Biến (Variables) Là Gì?

**Biến** là một vùng bộ nhớ để lưu trữ dữ liệu. Nó giống như một chiếc hộp có nhãn - bạn có thể đặt dữ liệu vào hộp và sử dụng nhãn để truy cập nó.

### Tạo Biến

```python
# Khai báo biến
name = 'Nguyễn Văn A'
age = 20
height = 1.75
is_student = True

# In biến
print(name)
print(age)
```

**Lưu ý:** Trong Python, không cần khai báo kiểu dữ liệu - Python tự nhận dạng.

---

## 📝 Đặt Tên Biến Đúng

### Quy Tắc Đặt Tên

✅ **ĐƯỢC:**
- Chữ cái: `a-z, A-Z`
- Chữ số: `0-9` (nhưng không bắt đầu bằng số)
- Gạch dưới: `_`
- Chữ hoa ở giữa: `myVariableName` (camelCase)
- Gạch dưới: `my_variable_name` (snake_case - **khuyến khích**)

❌ **KHÔNG ĐƯỢC:**
- Bắt đầu bằng số: `2names` ❌
- Khoảng trắng: `my name` ❌
- Ký tự đặc biệt: `my-name`, `my@name` ❌
- Từ khóa Python: `if`, `for`, `while`, `class` ❌

### Ví Dụ Tốt

```python
# Python style (khuyến khích)
student_name = 'Nguyễn'
student_age = 20
is_active = True

# camelCase (JavaScript style - dùng được nhưng không khuyến khích)
studentName = 'Nguyễn'
studentAge = 20

# Tránh
x = 'Nguyễn'  # Tên quá ngắn, không rõ ý
StudentName = 'Nguyễn'  # PascalCase - chỉ dùng cho class
```

---

## 🔄 Gán Giá Trị Cho Biến

### Gán Giá Trị Đơn

```python
name = 'Nguyễn'
age = 20
height = 1.75
```

### Gán Nhiều Biến Cùng Lúc

```python
# Cách 1: Gán giá trị khác nhau
name, age, city = 'Nguyễn', 20, 'Hà Nội'

# Cách 2: Gán cùng một giá trị
x = y = z = 0
print(x, y, z)  # 0 0 0
```

### Hoán Đổi Giá Trị (Swap)

```python
a = 10
b = 20
print(a, b)  # 10 20

# Hoán đổi
a, b = b, a
print(a, b)  # 20 10
```

---

## 🔍 Kiểm Tra Kiểu Dữ Liệu

```python
name = 'Nguyễn'
age = 20
height = 1.75
is_student = True

print(type(name))      # <class 'str'>
print(type(age))       # <class 'int'>
print(type(height))    # <class 'float'>
print(type(is_student))  # <class 'bool'>
```

---

## 📤 Hàm input() - Nhận Dữ Liệu

`input()` dùng để nhận dữ liệu từ người dùng nhập từ bàn phím.

### Ví Dụ Cơ Bản

```python
# Nhận tên
name = input('Nhập tên: ')
print('Xin chào ' + name)

# Nhận tuổi (lưu ý: input trả về chuỗi)
age_str = input('Nhập tuổi: ')
age = int(age_str)  # Chuyển thành số
print(f'Tuổi: {age}')
```

**Chạy chương trình:**

```
Nhập tên: Nguyễn
Xin chào Nguyễn
Nhập tuổi: 20
Tuổi: 20
```

### input() Luôn Trả Về Chuỗi

```python
# Lưu ý: input() luôn trả về chuỗi
age = input('Tuổi: ')  # '20' (chuỗi)
print(type(age))       # <class 'str'>

# Phải chuyển đổi kiểu
age = int(age)         # 20 (số)
print(type(age))       # <class 'int'>
```

---

## 🔄 Chuyển Đổi Kiểu Dữ Liệu (Casting)

### int() - Chuyển Thành Số Nguyên

```python
print(int('10'))      # 10
print(int(10.5))      # 10 (bỏ phần thập phân)
print(int(True))      # 1
print(int(False))     # 0
```

### float() - Chuyển Thành Số Thực

```python
print(float('3.14'))  # 3.14
print(float(10))      # 10.0
print(float(True))    # 1.0
```

### str() - Chuyển Thành Chuỗi

```python
print(str(10))        # '10'
print(str(3.14))      # '3.14'
print(str(True))      # 'True'
```

### bool() - Chuyển Thành Boolean

```python
print(bool(1))        # True
print(bool(0))        # False
print(bool(''))       # False (chuỗi rỗng)
print(bool('text'))   # True
print(bool([]))       # False (danh sách rỗng)
```

---

## 🔧 Các Hàm Built-in Quan Trọng

### len() - Độ Dài

```python
print(len('Xin chào'))      # 8
print(len([1, 2, 3, 4]))    # 4
print(len({'a': 1, 'b': 2}))  # 2
```

### max() & min() - Lớn Nhất & Nhỏ Nhất

```python
print(max(10, 20, 5))       # 20
print(min(10, 20, 5))       # 5
print(max([1, 5, 3, 9]))    # 9
print(min([1, 5, 3, 9]))    # 1
```

### sum() - Tổng

```python
print(sum([1, 2, 3, 4]))    # 10
print(sum([10, 20, 30]))    # 60
```

### abs() - Giá Trị Tuyệt Đối

```python
print(abs(-5))              # 5
print(abs(-3.14))           # 3.14
```

### round() - Làm Tròn

```python
print(round(3.14159))       # 3
print(round(3.14159, 2))    # 3.14 (làm tròn 2 chữ số)
print(round(3.5))           # 4
```

### sorted() - Sắp Xếp

```python
print(sorted([3, 1, 4, 1, 5]))  # [1, 1, 3, 4, 5]
print(sorted(['c', 'a', 'b']))  # ['a', 'b', 'c']
```

### reversed() - Đảo Ngược

```python
print(list(reversed([1, 2, 3])))    # [3, 2, 1]
print(list(reversed('ABC')))        # ['C', 'B', 'A']
```

### pow() - Lũy Thừa

```python
print(pow(2, 3))            # 8
print(pow(2, 3, 5))         # (2^3) % 5 = 3
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Tính Diện Tích

```python
# Nhập thông tin
radius = float(input('Nhập bán kính: '))

# Tính diện tích
import math
area = math.pi * radius ** 2

# In kết quả
print(f'Diện tích hình tròn: {area:.2f}')
```

### Ví Dụ 2: Tính Mức Lương

```python
# Nhập thông tin
name = input('Nhập tên: ')
salary = float(input('Nhập lương (triệu): '))
tax_rate = float(input('Nhập thuế (%): '))

# Tính
tax = salary * tax_rate / 100
net_salary = salary - tax

# In kết quả
print(f'Tên: {name}')
print(f'Lương: {salary:.1f} triệu')
print(f'Thuế: {tax:.1f} triệu')
print(f'Lương ròng: {net_salary:.1f} triệu')
```

---

## 📋 Tóm Tắt

| Khái Niệm | Ví Dụ |
|-----------|-------|
| Tạo biến | `name = 'Nguyễn'` |
| input() | `age = input('Tuổi: ')` |
| Chuyển đổi | `age = int(age)` |
| len() | `len('ABC')` → 3 |
| max() | `max(1, 5, 3)` → 5 |
| min() | `min(1, 5, 3)` → 1 |
| sum() | `sum([1, 2, 3])` → 6 |
| round() | `round(3.14, 1)` → 3.1 |

---

## 🚀 Tiếp Theo - Ngày 3

Ngày 3 bạn sẽ học:
- Toán tử số học
- Toán tử so sánh
- Toán tử logic
