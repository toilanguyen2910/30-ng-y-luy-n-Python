# 💻 Bài Tập Ngày 1

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Kiểm Tra Phiên Bản Python

Mở Terminal/Command Prompt và chạy:

```bash
python3 --version
```

**Kết quả kỳ vọng:** Phiên bản Python 3.x.x (ví dụ: Python 3.9.0)

---

### Bài 1.2: Phép Toán Trong Python Shell

Mở Python Shell (`python3`) và thực hiện các phép toán với số 3 và 4:

```python
>>> 3 + 4       # Cộng
>>> 4 - 3       # Trừ
>>> 3 * 4       # Nhân
>>> 4 / 3       # Chia
>>> 4 % 3       # Chia lấy dư
>>> 3 ** 4      # Lũy thừa
>>> 4 // 3      # Chia lấy phần nguyên
```

**Kết quả kỳ vọng:**

```
7
1
12
1.3333...
1
81
1
```

---

### Bài 1.3: Chuỗi Trong Python Shell

Gõ các chuỗi sau vào Python Shell:

```python
>>> 'Tên của tôi là Nguyễn Văn A'
>>> 'Quê quán của tôi ở Hà Nội'
>>> 'Tôi đến từ Việt Nam'
```

**Kết quả kỳ vọng:** Mỗi chuỗi sẽ được in ra như vừa nhập

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Tạo File `day_1.py`

Tạo file mới tên `day_1.py` và viết code:

```python
# Ngày 1 - Thử thách 30 ngày Python

# Thông tin cá nhân
name = 'Nguyễn Văn A'
age = 20
height = 1.75

print(f'Tên: {name}')
print(f'Tuổi: {age}')
print(f'Chiều cao: {height}m')

# Tính diện tích hình tròn (bán kính = 10)
import math
radius = 10
area = math.pi * radius ** 2
print(f'Diện tích hình tròn: {area}')

# Tính chu vi hình tròn
circumference = 2 * math.pi * radius
print(f'Chu vi hình tròn: {circumference}')
```

**Chạy file:**

```bash
python3 day_1.py
```

---

### Bài 2.2: Kiểm Tra Kiểu Dữ Liệu

Thêm vào file `day_1.py`:

```python
# Kiểm tra kiểu dữ liệu
print(type('Tôi yêu Python'))
print(type(42))
print(type(3.14))
print(type(True))
print(type(['Python', 'Java', 'JavaScript']))
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Tính Tuổi

Viết code tính tuổi dựa trên năm sinh:

```python
# Năm hiện tại
current_year = 2026

# Năm sinh của bạn
birth_year = 2007

# Tính tuổi
age = current_year - birth_year
print(f'Tuổi của tôi: {age}')
```

---

### Bài 3.2: Tính Số Ngày Sống

```python
# Giả sử bạn sinh ngày 29/10/2007
birth_year = 2007
birth_month = 10
birth_day = 29

current_year = 2026
current_month = 6
current_day = 15

# Tính năm sống
years = current_year - birth_year

# Tính ngày xấp xỉ (1 năm = 365 ngày)
days_lived = years * 365
print(f'Số ngày đã sống: {days_lived}')
```

---

### Bài 3.3: Tạo Hồ Sơ Cá Nhân

```python
# Hồ sơ cá nhân
profile = {
    'name': 'Nguyễn Văn A',
    'age': 19,
    'birth_year': 2007,
    'major': 'Công Nghệ Thông Tin',
    'skills': ['Python', 'JavaScript', 'HTML/CSS', 'SQL']
}

print('=== HỒ SƠ CÁ NHÂN ===')
print(f'Tên: {profile["name"]}')
print(f'Tuổi: {profile["age"]}')
print(f'Năm sinh: {profile["birth_year"]}')
print(f'Ngành học: {profile["major"]}')
print(f'Kỹ năng:')
for skill in profile['skills']:
    print(f'  - {skill}')
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Cài đặt Python thành công
- [ ] Kiểm tra phiên bản Python
- [ ] Mở Python Shell thành công
- [ ] Chạy các phép toán trong Shell
- [ ] Tạo file Python đầu tiên
- [ ] Chạy file Python thành công
- [ ] Hoàn thành tất cả bài tập

---

## 💡 Mẹo & Lưu Ý

1. **Đặt tên file Python:** Dùng chữ thường, dùng gạch dưới thay vì khoảng trắng (ví dụ: `day_1.py`, không phải `Day 1.py`)

2. **Indent (thụt lề):** Python yêu cầu thụt lề đúng. Dùng 4 khoảng trắng hoặc 1 Tab.

3. **Print:** Để in dữ liệu ra màn hình, dùng `print()`. Nó rất quan trọng!

4. **Chú ý viết hoa:** Python phân biệt hoa/thường (`print` không phải `Print`)

5. **f-string:** Cách hiện đại để format chuỗi:
   ```python
   name = 'Nam'
   age = 20
   print(f'Tôi là {name}, {age} tuổi')  # Tôi là Nam, 20 tuổi
   ```

6. **Thư viện math:** Để sử dụng hằng số π hoặc hàm toán học, import math:
   ```python
   import math
   print(math.pi)  # 3.14159...
   ```

---

## 🎯 Mục Tiêu Sau Ngày 1

✅ Hiểu Python là gì  
✅ Cài đặt Python  
✅ Chạy được Python Shell  
✅ Biết 8 kiểu dữ liệu cơ bản  
✅ Viết được chương trình Python đơn giản  
✅ Chạy được file Python  

---

## 🚀 Chuẩn Bị Cho Ngày 2

Ngày 2 bạn sẽ học:
- **Biến (Variables)** - Cách lưu trữ dữ liệu
- **Hàm input()** - Nhận dữ liệu từ người dùng
- **Hàm Built-in** - Các hàm có sẵn trong Python
