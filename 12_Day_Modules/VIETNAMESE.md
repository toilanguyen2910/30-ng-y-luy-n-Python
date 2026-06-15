# 📘 Ngày 11 - Module & Import

## 🎯 Mục Tiêu Ngày 11

- Hiểu module là gì
- Import module
- Sử dụng thư viện math
- Sử dụng thư viện random
- Tạo module riêng

---

## 📦 Module Là Gì?

**Module** là file Python chứa các hàm, biến, class có thể tái sử dụng.

---

## 🔌 Import - Nhập Module

### Import Toàn Bộ Module

```python
import math

print(math.pi)        # 3.14159...
print(math.sqrt(16))  # 4.0
```

### Import Một Phần

```python
from math import pi, sqrt

print(pi)             # 3.14159...
print(sqrt(16))       # 4.0
```

### Import Với Tên Khác

```python
import math as m

print(m.pi)
print(m.sqrt(25))
```

---

## 🔢 Thư Viện math

```python
import math

# Hằng số
print(math.pi)        # 3.14159...
print(math.e)         # 2.71828...

# Hàm cơ bản
print(math.sqrt(16))  # 4.0
print(math.pow(2, 3)) # 8.0
print(math.abs(-5))   # 5
print(math.ceil(4.3)) # 5 (làm tròn lên)
print(math.floor(4.8))# 4 (làm tròn xuống)

# Lượng giác
print(math.sin(math.pi/2))  # 1.0
print(math.cos(0))          # 1.0
```

---

## 🎲 Thư Viện random

```python
import random

# Số ngẫu nhiên
print(random.randint(1, 10))    # 1-10
print(random.random())           # 0.0-1.0
print(random.uniform(1, 10))    # 1.0-10.0

# Chọn từ danh sách
fruits = ['Chuối', 'Cam', 'Xoài']
print(random.choice(fruits))     # một trong ba

# Xáo trộn
cards = [1, 2, 3, 4, 5]
random.shuffle(cards)
print(cards)

# Chọn k phần tử
print(random.sample(fruits, 2))  # chọn 2
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Tính Diện Tích Hình Tròn

```python
import math

radius = float(input('Bán kính: '))
area = math.pi * radius ** 2
print(f'Diện tích: {area:.2f}')
```

### Ví Dụ 2: Trò Chơi Đoán Số

```python
import random

secret = random.randint(1, 100)
guesses = 0

while True:
    guess = int(input('Đoán số (1-100): '))
    guesses += 1
    
    if guess == secret:
        print(f'✓ Đúng rồi! ({guesses} lần)')
        break
    elif guess < secret:
        print('Lớn hơn')
    else:
        print('Nhỏ hơn')
```

---

## 🚀 Tiếp Theo - Ngày 12

Ngày 12 bạn sẽ học:
- List Comprehension
- Dictionary Comprehension
- Set Comprehension
