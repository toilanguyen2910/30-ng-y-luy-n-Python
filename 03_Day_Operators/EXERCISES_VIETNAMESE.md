# 💻 Bài Tập Ngày 3

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Toán Tử Số Học

Tạo file `day_3_arithmetic.py`:

```python
# Ngày 3 - Toán Tử

# Toán tử số học
a = 10
b = 3

print(f'{a} + {b} = {a + b}')
print(f'{a} - {b} = {a - b}')
print(f'{a} * {b} = {a * b}')
print(f'{a} / {b} = {a / b}')
print(f'{a} // {b} = {a // b}')
print(f'{a} % {b} = {a % b}')
print(f'{a} ** {b} = {a ** b}')
```

---

### Bài 1.2: Toán Tử So Sánh

```python
# Toán tử so sánh
x = 10
y = 5

print(f'{x} == {y}: {x == y}')
print(f'{x} != {y}: {x != y}')
print(f'{x} > {y}: {x > y}')
print(f'{x} < {y}: {x < y}')
print(f'{x} >= {y}: {x >= y}')
print(f'{x} <= {y}: {x <= y}')
```

---

### Bài 1.3: Toán Tử Logic

```python
# Toán tử logic
a = True
b = False

print(f'{a} and {b} = {a and b}')
print(f'{a} or {b} = {a or b}')
print(f'not {a} = {not a}')

# Với điều kiện
age = 25
print((age >= 18) and (age < 65))  # True
print((age < 18) or (age >= 65))   # False
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Toán Tử Gán

Tạo file `day_3_assignment.py`:

```python
# Toán tử gán

# Gán cơ bản
x = 10
print(f'x = {x}')

# Toán tử gán kết hợp
x += 5   # x = x + 5
print(f'x += 5: {x}')

x -= 3   # x = x - 3
print(f'x -= 3: {x}')

x *= 2   # x = x * 2
print(f'x *= 2: {x}')

x //= 4  # x = x // 4
print(f'x //= 4: {x}')

x %= 3   # x = x % 3
print(f'x %= 3: {x}')
```

---

### Bài 2.2: Toán Tử Thuộc (Membership)

```python
# Toán tử thuộc

fruits = ['Chuối', 'Cam', 'Xoài', 'Dâu']

print('Chuối' in fruits)       # True
print('Táo' in fruits)         # False
print('Táo' not in fruits)     # True

# Với chuỗi
word = 'Python'
print('P' in word)             # True
print('z' in word)             # False
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Kiểm Tra Điều Kiện Phức Tạp

Tạo file `day_3_advanced.py`:

```python
# Chương trình kiểm tra điều kiện phức tạp

print('=== KIỂM TRA ĐIỀU KIỆN ===\n')

# Nhập dữ liệu
age = int(input('Nhập tuổi: '))
income = float(input('Nhập thu nhập (triệu): '))
has_diploma = input('Có bằng cấp? (yes/no): ').lower() == 'yes'

# Kiểm tra điều kiện
is_adult = age >= 18
has_good_income = income >= 10
is_qualified = has_diploma and is_adult

print(f'\nTuổi >= 18: {is_adult}')
print(f'Thu nhập >= 10 triệu: {has_good_income}')
print(f'Có bằng cấp: {has_diploma}')
print(f'Đủ điều kiện vay: {is_qualified}')

# Phân loại
if is_adult and has_good_income:
    print('→ Bạn đủ điều kiện vay tiền')
elif is_adult:
    print('→ Bạn chưa đủ thu nhập')
else:
    print('→ Bạn chưa thành niên')
```

---

### Bài 3.2: Tính Giá Trị Phần Trăm

```python
# Tính giá trị phần trăm

print('=== TÍNH GIẢM GIÁ ===\n')

original_price = float(input('Nhập giá gốc (VND): '))
discount_percent = float(input('Nhập % giảm giá: '))

# Tính
discount_amount = original_price * discount_percent / 100
final_price = original_price - discount_amount

# In kết quả
print(f'\nGiá gốc: {original_price:,.0f} VND')
print(f'Giảm giá: {discount_percent}%')
print(f'Tiền giảm: {discount_amount:,.0f} VND')
print(f'Giá cuối: {final_price:,.0f} VND')

# Kiểm tra
if discount_percent >= 50:
    print('→ Giảm giá lớn!')
elif discount_percent >= 20:
    print('→ Giảm giá khá')
else:
    print('→ Giảm giá nhỏ')
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Hiểu toán tử số học
- [ ] Hiểu toán tử so sánh
- [ ] Hiểu toán tử logic (and, or, not)
- [ ] Sử dụng toán tử gán kết hợp
- [ ] Biết toán tử thuộc (in, not in)
- [ ] Hoàn thành bài tập cơ bản
- [ ] Hoàn thành bài tập nâng cao
- [ ] Hoàn thành thách thức cao cấp

---

## 💡 Mẹo Quan Trọng

**1. Ưu tiên toán tử:**
```python
print(2 + 3 * 4)   # 14 (nhân trước)
print((2 + 3) * 4) # 20 (cộng trước)
```

**2. Toán tử logic:**
```python
# and - cả hai đều đúng
if age >= 18 and age < 65:
    print('Độ tuổi lao động')

# or - ít nhất một đúng
if score < 5 or score > 100:
    print('Điểm không hợp lệ')

# not - phủ định
if not is_student:
    print('Không phải sinh viên')
```

**3. So sánh chuỗi:**
```python
print('apple' < 'banana')  # True (so sánh bảng chữ cái)
```

---

## 🚀 Chuẩn Bị Cho Ngày 4

Ngày 4 bạn sẽ học:
- Chuỗi (String)
- Các phương thức chuỗi
- Slicing chuỗi
