# 💻 Bài Tập Ngày 4

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Truy Cập Ký Tự

Tạo file `day_4_string_basics.py`:

```python
# Ngày 4 - Chuỗi

# Tạo chuỗi
text = "Python"

# Truy cập ký tự
print(text[0])      # P
print(text[1])      # y
print(text[-1])     # n (ký tự cuối)
print(text[-2])     # o

# Độ dài
print(len(text))    # 6

# Slicing
print(text[0:2])    # Py
print(text[2:])     # thon
print(text[::-1])   # nohtyP (đảo ngược)
```

---

### Bài 1.2: Phương Thức Chuỗi Cơ Bản

```python
# Phương thức chuỗi
text = "hello python"

print(text.upper())         # HELLO PYTHON
print(text.lower())         # hello python
print(text.capitalize())    # Hello python
print(text.title())         # Hello Python

# Tìm kiếm
print(text.find('python'))  # 6
print(text.count('l'))      # 3

# Kiểm tra
print(text.startswith('hello'))  # True
print(text.endswith('python'))   # True
```

---

### Bài 1.3: Tách & Nối Chuỗi

```python
# split() - tách
fruits_text = "Chuối,Cam,Xoài"
fruits = fruits_text.split(',')
print(fruits)  # ['Chuối', 'Cam', 'Xoài']

# join() - nối
result = ' - '.join(fruits)
print(result)  # Chuối - Cam - Xoài

# replace() - thay thế
text = "Tôi yêu Python"
new_text = text.replace("Python", "JavaScript")
print(new_text)  # Tôi yêu JavaScript
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Format Chuỗi

Tạo file `day_4_string_format.py`:

```python
# Format chuỗi

# 1. F-String (khuyến khích)
name = "Nguyễn"
age = 20
print(f"Tên: {name}, Tuổi: {age}")

# 2. Format số
price = 1500000
print(f"Giá: {price:,} VND")

# 3. Format thập phân
score = 8.7654
print(f"Điểm: {score:.2f}")

# 4. format() method
print("Hello {}, you are {} years old".format(name, age))

# 5. Concatenation
greeting = "Xin chào " + name
print(greeting)
```

---

### Bài 2.2: Xử Lý Email

```python
# Xử lý email

email = input("Nhập email: ")

# Kiểm tra
if "@" not in email or "." not in email:
    print("Email không hợp lệ")
else:
    # Tách phần tên
    username = email.split("@")[0]
    domain = email.split("@")[1]
    
    print(f"Tên người dùng: {username}")
    print(f"Domain: {domain}")
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Xử Lý Tên Người

Tạo file `day_4_advanced.py`:

```python
# Xử lý thông tin cá nhân

print("=== XỬ LÝ TÊN ===\n")

# Nhập tên
full_name = input("Nhập họ tên: ")

# Xử lý
clean_name = full_name.strip()
title_name = clean_name.title()

# Tách thành phần
parts = title_name.split()

print(f"\nHộ tên gốc: {full_name}")
print(f"Họ tên sạch: {clean_name}")
print(f"Định dạng: {title_name}")
print(f"Số từ: {len(parts)}")

if len(parts) >= 2:
    print(f"Họ: {' '.join(parts[:-1])}")
    print(f"Tên: {parts[-1]}")

# Thống kê
print(f"\nThống kê:")
print(f"Độ dài: {len(title_name)} ký tự")
print(f"Chữ in hoa: {sum(1 for c in title_name if c.isupper())}")
print(f"Chữ in thường: {sum(1 for c in title_name if c.islower())}")
```

---

### Bài 3.2: Xác Thực Mật Khẩu

```python
# Kiểm tra mật khẩu

print("=== KIỂM TRA MẬT KHẨU ===\n")

password = input("Nhập mật khẩu: ")

# Kiểm tra
is_long = len(password) >= 8
has_upper = any(c.isupper() for c in password)
has_lower = any(c.islower() for c in password)
has_digit = any(c.isdigit() for c in password)

print(f"\nKiểm tra:")
print(f"Độ dài >= 8: {is_long}")
print(f"Có chữ hoa: {has_upper}")
print(f"Có chữ thường: {has_lower}")
print(f"Có chữ số: {has_digit}")

# Đánh giá
if is_long and has_upper and has_lower and has_digit:
    print("\n✓ Mật khẩu mạnh")
elif is_long and (has_upper or has_digit):
    print("\n~ Mật khẩu trung bình")
else:
    print("\n✗ Mật khẩu yếu")
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Truy cập ký tự trong chuỗi
- [ ] Dùng slicing để cắt chuỗi
- [ ] Sử dụng upper(), lower()
- [ ] Sử dụng split(), join()
- [ ] Sử dụng replace()
- [ ] Sử dụng find(), count()
- [ ] Sử dụng f-string format
- [ ] Hoàn thành bài tập cơ bản
- [ ] Hoàn thành bài tập nâng cao

---

## 💡 Mẹo Quan Trọng

**1. Index chuỗi:**
```python
text = "Python"
print(text[0])    # P (từ đầu)
print(text[-1])   # n (từ cuối)
```

**2. Slicing:**
```python
text = "Python"
print(text[0:3])  # Pyt
print(text[::-1]) # nohtyP (đảo)
```

**3. F-string tốt nhất:**
```python
name = "Nam"
age = 20
print(f"Tôi là {name}, {age} tuổi")
```

**4. Một số phương thức hữu ích:**
```python
"hello".capitalize()      # Hello
"hello world".title()     # Hello World
"  hello  ".strip()       # hello
"a,b,c".split(',')        # ['a','b','c']
```
