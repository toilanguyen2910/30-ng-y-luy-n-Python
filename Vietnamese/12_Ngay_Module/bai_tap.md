# 💻 Bài Tập Ngày 11

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Module math

Tạo file `day_11_math.py`:

```python
# Ngày 11 - Module & Import

import math

# Hằng số
print(f'Pi: {math.pi}')
print(f'E: {math.e}')

# Hàm căn bậc hai
print(f'√16: {math.sqrt(16)}')
print(f'√25: {math.sqrt(25)}')

# Hàm lũy thừa
print(f'2^3: {math.pow(2, 3)}')
print(f'10^2: {math.pow(10, 2)}')

# Làm tròn
print(f'ceil(4.3): {math.ceil(4.3)}')
print(f'floor(4.8): {math.floor(4.8)}')

# Giá trị tuyệt đối
print(f'abs(-5): {math.fabs(-5)}')
```

---

### Bài 1.2: Module random

```python
import random

# Số ngẫu nhiên
print(f'Số 1-10: {random.randint(1, 10)}')
print(f'Số 0-1: {random.random()}')
print(f'Số 1-10 (float): {random.uniform(1, 10)}')

# Chọn ngẫu nhiên
fruits = ['Chuối', 'Cam', 'Xoài', 'Dâu']
print(f'Hoa quả: {random.choice(fruits)}')

# Xáo trộn
cards = [1, 2, 3, 4, 5]
random.shuffle(cards)
print(f'Xáo trộn: {cards}')

# Chọn k phần tử
print(f'Chọn 2: {random.sample(fruits, 2)}')
```

---

### Bài 1.3: Import Khác Nhau

```python
# Cách 1: Import toàn bộ
import math
print(math.sqrt(9))

# Cách 2: Import một phần
from math import sqrt, pi
print(sqrt(16))
print(pi)

# Cách 3: Import với tên khác
import random as rd
print(rd.randint(1, 10))

# Cách 4: Import *
from math import *
print(sqrt(25))
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Tính Toán Hình Học

Tạo file `day_11_geometry.py`:

```python
# Tính toán hình học

import math

print("=== TÍNH TOÁN HÌNH HỌC ===\n")

# Diện tích hình tròn
radius = float(input("Bán kính hình tròn: "))
circle_area = math.pi * radius ** 2
print(f"Diện tích: {circle_area:.2f}")

# Chu vi hình tròn
circle_perimeter = 2 * math.pi * radius
print(f"Chu vi: {circle_perimeter:.2f}")

# Diện tích hình cầu
sphere_area = 4 * math.pi * radius ** 2
print(f"Diện tích mặt cầu: {sphere_area:.2f}")
```

---

### Bài 2.2: Trò Chơi Đoán Số

```python
# Trò chơi đoán số

import random

print("=== ĐOÁN SỐ ===\n")

secret = random.randint(1, 100)
guesses = 0

while True:
    guess = int(input("Đoán số (1-100): "))
    guesses += 1
    
    if guess == secret:
        print(f"✓ Chính xác! Bạn đoán {guesses} lần")
        break
    elif guess < secret:
        print("→ Lớn hơn")
    else:
        print("→ Nhỏ hơn")
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Import module
- [ ] Sử dụng math.pi
- [ ] Sử dụng math.sqrt()
- [ ] Sử dụng random.randint()
- [ ] Sử dụng random.choice()
- [ ] Hoàn thành bài cơ bản
- [ ] Hoàn thành bài nâng cao

---

## 💡 Mẹo Quan Trọng

**1. Import module:**
```python
import math           # toàn bộ
from math import pi   # một phần
import math as m      # tên khác
```

**2. math thường dùng:**
```python
math.pi       # hằng số Pi
math.sqrt(x)  # căn bậc hai
math.pow(x,y) # x lũy thừa y
math.ceil()   # làm tròn lên
math.floor()  # làm tròn xuống
```

**3. random thường dùng:**
```python
random.randint(a,b)   # số nguyên
random.choice(list)   # chọn 1
random.shuffle(list)  # xáo trộn
```
