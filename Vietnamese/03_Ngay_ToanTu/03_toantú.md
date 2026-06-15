# 📘 Ngày 3 - Toán Tử

## 🎯 Mục Tiêu Ngày 3

- Hiểu các loại toán tử trong Python
- Sử dụng toán tử số học
- Sử dụng toán tử so sánh
- Sử dụng toán tử logic
- Hiểu ưu tiên toán tử

---

## 🔢 Toán Tử Số Học (Arithmetic Operators)

Toán tử số học được sử dụng để thực hiện các phép toán toán học.

| Toán Tử | Tên | Ví Dụ | Kết Quả |
|---------|-----|-------|---------|
| + | Cộng | 10 + 5 | 15 |
| - | Trừ | 10 - 5 | 5 |
| * | Nhân | 10 * 5 | 50 |
| / | Chia | 10 / 5 | 2.0 |
| // | Chia lấy phần nguyên | 10 // 3 | 3 |
| % | Chia lấy dư (modulo) | 10 % 3 | 1 |
| ** | Lũy thừa | 2 ** 3 | 8 |

### Ví Dụ Chi Tiết

```python
# Cộng, trừ, nhân, chia
print(10 + 5)      # 15
print(10 - 5)      # 5
print(10 * 5)      # 50
print(10 / 5)      # 2.0 (chia được float)

# Chia lấy phần nguyên
print(10 // 3)     # 3 (bỏ phần thập phân)
print(-10 // 3)    # -4 (làm tròn xuống)

# Chia lấy dư
print(10 % 3)      # 1
print(10 % 2)      # 0

# Lũy thừa
print(2 ** 3)      # 8
print(2 ** 10)     # 1024
```

---

## 🔗 Toán Tử Gán (Assignment Operators)

Toán tử gán được sử dụng để gán giá trị cho biến.

| Toán Tử | Ví Dụ | Tương Đương |
|---------|-------|------------|
| = | x = 5 | x = 5 |
| += | x += 3 | x = x + 3 |
| -= | x -= 3 | x = x - 3 |
| *= | x *= 3 | x = x * 3 |
| /= | x /= 3 | x = x / 3 |
| //= | x //= 3 | x = x // 3 |
| %= | x %= 3 | x = x % 3 |
| **= | x **= 3 | x = x ** 3 |

### Ví Dụ

```python
x = 10
x += 5      # x = x + 5 = 15
print(x)    # 15

x -= 3      # x = x - 3 = 12
print(x)    # 12

x *= 2      # x = x * 2 = 24
print(x)    # 24

x //= 5     # x = x // 5 = 4
print(x)    # 4
```

---

## 🔍 Toán Tử So Sánh (Comparison Operators)

Toán tử so sánh được sử dụng để so sánh hai giá trị. Kết quả là True hoặc False.

| Toán Tử | Tên | Ví Dụ | Kết Quả |
|---------|-----|-------|---------|
| == | Bằng | 5 == 5 | True |
| != | Không bằng | 5 != 3 | True |
| > | Lớn hơn | 5 > 3 | True |
| < | Nhỏ hơn | 5 < 3 | False |
| >= | Lớn hơn hoặc bằng | 5 >= 5 | True |
| <= | Nhỏ hơn hoặc bằng | 5 <= 3 | False |

### Ví Dụ Chi Tiết

```python
# Bằng và không bằng
print(5 == 5)      # True
print(5 != 3)      # True
print('a' == 'a')  # True

# Lớn hơn và nhỏ hơn
print(5 > 3)       # True
print(5 < 3)       # False

# Lớn hơn hoặc bằng, nhỏ hơn hoặc bằng
print(5 >= 5)      # True
print(5 <= 3)      # False

# So sánh chuỗi
print('apple' == 'apple')   # True
print('apple' < 'banana')   # True (so sánh bảng chữ cái)
```

---

## 🧠 Toán Tử Logic (Logical Operators)

Toán tử logic được sử dụng để kết hợp các điều kiện. Kết quả là True hoặc False.

| Toán Tử | Ý Nghĩa | Ví Dụ |
|---------|---------|-------|
| and | Cả hai điều kiện đều đúng | (5 > 3) and (3 > 1) |
| or | Ít nhất một điều kiện đúng | (5 > 3) or (3 > 10) |
| not | Phủ định | not(5 > 10) |

### Bảng Sự Thật

**AND (và):**
| A | B | A and B |
|---|---|---------|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | F |

**OR (hoặc):**
| A | B | A or B |
|---|---|---------|
| T | T | T |
| T | F | T |
| F | T | T |
| F | F | F |

**NOT (phủ định):**
| A | not A |
|---|-------|
| T | F |
| F | T |

### Ví Dụ

```python
# and - Cả hai điều kiện đều đúng
print((5 > 3) and (3 > 1))      # True (đúng AND đúng)
print((5 > 3) and (3 > 10))     # False (đúng AND sai)

# or - Ít nhất một điều kiện đúng
print((5 > 3) or (3 > 10))      # True (đúng OR sai)
print((5 > 10) or (3 > 10))     # False (sai OR sai)

# not - Phủ định
print(not(5 > 3))               # False (phủ định của đúng)
print(not(5 > 10))              # True (phủ định của sai)

# Kết hợp
age = 25
print((age >= 18) and (age < 65))  # True (người trong độ tuổi lao động)
```

---

## 📊 Toán Tử Nhận Dạng (Identity Operators)

Toán tử này kiểm tra xem hai biến có cùng object không.

| Toán Tử | Ý Nghĩa |
|---------|---------|
| is | Cùng object |
| is not | Không cùng object |

```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a

print(a == b)       # True (giá trị bằng nhau)
print(a is b)       # False (không cùng object)
print(a is c)       # True (cùng object)
```

---

## 📍 Toán Tử Thuộc (Membership Operators)

Toán tử này kiểm tra xem giá trị có trong danh sách hay không.

| Toán Tử | Ý Nghĩa |
|---------|---------|
| in | Có trong |
| not in | Không có trong |

```python
fruits = ['Chuối', 'Cam', 'Xoài']
print('Chuối' in fruits)         # True
print('Táo' in fruits)           # False
print('Táo' not in fruits)       # True

# Với chuỗi
print('P' in 'Python')           # True
print('z' in 'Python')           # False
```

---

## ⚖️ Ưu Tiên Toán Tử (Operator Precedence)

Khi có nhiều toán tử, Python thực thi theo thứ tự ưu tiên (từ cao đến thấp):

1. ** (lũy thừa)
2. +, -, ~ (dấu dương, âm, bitwise NOT)
3. *, /, //, % (nhân, chia)
4. +, - (cộng, trừ)
5. ==, !=, <, >, <=, >= (so sánh)
6. not (phủ định logic)
7. and (logic AND)
8. or (logic OR)

### Ví Dụ

```python
# Ví dụ 1
print(2 + 3 * 4)     # 14 (3*4=12, 12+2=14, không phải 5*4=20)

# Ví dụ 2
print(10 - 5 - 2)    # 3 (từ trái sang phải: 10-5=5, 5-2=3)

# Ví dụ 3
print(2 ** 3 ** 2)   # 512 (lũy thừa từ phải sang trái: 3**2=9, 2**9=512)

# Ví dụ 4
print(5 > 3 and 2 < 4)  # True

# Dùng ngoặc để thay đổi ưu tiên
print((2 + 3) * 4)   # 20 (2+3=5, 5*4=20)
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Kiểm Tra Tuổi

```python
age = int(input('Nhập tuổi: '))

# Kiểm tra
if age >= 18:
    print('Bạn đủ tuổi thành niên')
else:
    print('Bạn chưa thành niên')

# Kiểm tra phạm vi
if 18 <= age < 65:
    print('Bạn trong độ tuổi lao động')
```

### Ví Dụ 2: Kiểm Tra Điều Kiện Hàng Loạt

```python
score = float(input('Nhập điểm: '))

# Sử dụng and, or
if score >= 0 and score <= 100:
    if score >= 8:
        print('Giỏi')
    elif score >= 6.5:
        print('Khá')
    else:
        print('Trung bình')
else:
    print('Điểm không hợp lệ')
```

---

## 📋 Tóm Tắt

| Loại | Toán Tử | Ví Dụ |
|------|---------|-------|
| Số học | +, -, *, /, //, %, ** | 10 + 5 = 15 |
| So sánh | ==, !=, >, <, >=, <= | 5 > 3 = True |
| Logic | and, or, not | (5>3) and (3>1) = True |
| Gán | =, +=, -=, *=, /= | x += 5 |
| Thuộc | in, not in | 'a' in 'abc' = True |
| Nhận dạng | is, is not | a is b |

---

## 🚀 Tiếp Theo - Ngày 4

Ngày 4 bạn sẽ học:
- Chuỗi (String)
- Phương thức chuỗi
- Format chuỗi
