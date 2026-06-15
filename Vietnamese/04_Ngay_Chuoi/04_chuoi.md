# 📘 Ngày 4 - Chuỗi (String)

## 🎯 Mục Tiêu Ngày 4

- Hiểu chuỗi là gì
- Tạo và in chuỗi
- Truy cập ký tự trong chuỗi
- Cắt chuỗi (String Slicing)
- Sử dụng các phương thức chuỗi

---

## 📝 Chuỗi (String) Là Gì?

**Chuỗi** là tập hợp các ký tự được bao quanh bởi dấu ngoặc kép `" "` hoặc ngoặc đơn `' '`.

### Tạo Chuỗi

```python
# Chuỗi với ngoặc đơn
name = 'Nguyễn'

# Chuỗi với ngoặc kép
city = "Hà Nội"

# Chuỗi nhiều dòng
message = """
Xin chào!
Đây là chuỗi nhiều dòng.
"""

# Chuỗi rỗng
empty = ''
```

---

## 🔍 Truy Cập Ký Tự Trong Chuỗi

Mỗi ký tự trong chuỗi có một **chỉ số (index)** bắt đầu từ 0.

### Indexing

```python
text = "Python"
#      012345  (chỉ số từ 0)

print(text[0])    # P
print(text[1])    # y
print(text[2])    # t
print(text[5])    # n
print(text[-1])   # n (ký tự cuối)
print(text[-2])   # o (ký tự thứ 2 từ cuối)
```

### Độ Dài Chuỗi

```python
text = "Python"
print(len(text))  # 6
```

---

## ✂️ Cắt Chuỗi (String Slicing)

**Slicing** là lấy một phần của chuỗi.

### Cú Pháp

```python
string[start:end:step]
```

- `start`: vị trí bắt đầu (mặc định 0)
- `end`: vị trí kết thúc (không bao gồm)
- `step`: bước nhảy (mặc định 1)

### Ví Dụ

```python
text = "Python"
#      012345

# Lấy từ vị trí 0 đến 2 (không bao gồm 2)
print(text[0:2])    # Py

# Lấy từ vị trí 2 đến cuối
print(text[2:])     # thon

# Lấy từ đầu đến vị trí 4
print(text[:4])     # Pyth

# Lấy từ đầu đến cuối
print(text[:])      # Python

# Lấy với bước 2
print(text[::2])    # Pto

# Đảo ngược chuỗi
print(text[::-1])   # nohtyP

# Lấy 3 ký tự đầu tiên
print(text[:3])     # Pyt
```

---

## 🔤 Phương Thức Chuỗi Quan Trọng

### upper() & lower()

```python
text = "Hello World"
print(text.upper())    # HELLO WORLD
print(text.lower())    # hello world
```

### capitalize() & title()

```python
text = "hello world"
print(text.capitalize())  # Hello world
print(text.title())       # Hello World
```

### strip() & replace()

```python
# Xóa khoảng trắng đầu/cuối
text = "  hello  "
print(text.strip())       # hello
print(text.lstrip())      # hello   (xóa trái)
print(text.rstrip())      #   hello (xóa phải)

# Thay thế
text = "Hello World"
print(text.replace("World", "Python"))  # Hello Python
```

### split() & join()

```python
# split() - tách chuỗi thành danh sách
text = "Python,Java,JavaScript"
languages = text.split(',')
print(languages)  # ['Python', 'Java', 'JavaScript']

# join() - nối danh sách thành chuỗi
fruits = ['Chuối', 'Cam', 'Xoài']
result = ', '.join(fruits)
print(result)     # Chuối, Cam, Xoài
```

### find() & count()

```python
text = "Hello Python Python"

# find() - tìm vị trí
print(text.find('P'))      # 6
print(text.find('hello'))  # -1 (không tìm thấy)

# count() - đếm
print(text.count('Python'))  # 2
```

### startswith() & endswith()

```python
text = "Hello World"
print(text.startswith('Hello'))   # True
print(text.endswith('World'))     # True
print(text.endswith('.py'))       # False
```

### isdigit(), isalpha(), isalnum()

```python
print("123".isdigit())      # True
print("abc".isalpha())      # True
print("abc123".isalnum())   # True
print("abc 123".isalnum())  # False (có khoảng trắng)
```

---

## 🎨 Format Chuỗi

### 1. Concatenation (Nối Chuỗi)

```python
first_name = "Nguyễn"
last_name = "Văn A"
full_name = first_name + " " + last_name
print(full_name)  # Nguyễn Văn A
```

### 2. F-String (Khuyến Khích)

```python
name = "Nguyễn"
age = 20
print(f"Tên: {name}, Tuổi: {age}")  # Tên: Nguyễn, Tuổi: 20

# Với phép toán
x = 10
y = 5
print(f"Tổng: {x + y}")  # Tổng: 15

# Format số
price = 1500000
print(f"Giá: {price:,} VND")  # Giá: 1,500,000 VND
```

### 3. format() Method

```python
name = "Nguyễn"
age = 20
print("Tên: {}, Tuổi: {}".format(name, age))
print("Tuổi: {age}, Tên: {name}".format(name=name, age=age))
```

### 4. % Operator (Cũ)

```python
name = "Nguyễn"
print("Xin chào %s" % name)
```

---

## 📋 Tóm Tắt Phương Thức

| Phương Thức | Ý Nghĩa | Ví Dụ |
|------------|---------|-------|
| upper() | Chữ hoa | "hello".upper() → "HELLO" |
| lower() | Chữ thường | "HELLO".lower() → "hello" |
| strip() | Xóa khoảng trắng | "  hello  ".strip() → "hello" |
| split() | Tách chuỗi | "a,b,c".split(',') → ['a','b','c'] |
| join() | Nối danh sách | ','.join(['a','b']) → "a,b" |
| replace() | Thay thế | "abc".replace('a','x') → "xbc" |
| find() | Tìm vị trí | "hello".find('e') → 1 |
| startswith() | Bắt đầu với | "hello".startswith('h') → True |
| endswith() | Kết thúc với | "hello".endswith('o') → True |
| count() | Đếm | "aaa".count('a') → 3 |

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Xử Lý Tên

```python
full_name = "  NGUYỄN VĂN A  "

# Xử lý
clean_name = full_name.strip().lower().title()
print(clean_name)  # Nguyễn Văn A

# Tách tên
name_parts = clean_name.split()
print(f"Họ: {name_parts[0]}")      # Họ: Nguyễn
print(f"Tên: {name_parts[-1]}")    # Tên: A
```

### Ví Dụ 2: Xác Thực Email

```python
email = "user@example.com"

is_valid = "@" in email and "." in email
print(f"Email hợp lệ: {is_valid}")

# Tách tên người dùng
username = email.split("@")[0]
print(f"Tên người dùng: {username}")
```

---

## 🚀 Tiếp Theo - Ngày 5

Ngày 5 bạn sẽ học:
- Danh sách (List)
- Các phương thức danh sách
- Lặp qua danh sách
