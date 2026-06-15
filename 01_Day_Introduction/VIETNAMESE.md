# 📘 Ngày 1 - Giới Thiệu Python

## 🎯 Mục Tiêu Ngày 1

- Hiểu Python là gì
- Cài đặt Python và các công cụ cần thiết
- Chạy chương trình Python đầu tiên
- Học các kiểu dữ liệu cơ bản
- Làm quen với Python Interactive Shell

---

## 🐍 Python Là Gì?

**Python** là ngôn ngữ lập trình:
- **Mức cao** - cú pháp gần với ngôn ngữ tự nhiên
- **Mã nguồn mở** - miễn phí, công khai source code
- **Được giải thích** - thực thi dòng lệnh từng cái một
- **Hướng đối tượng** - hỗ trợ lập trình OOP
- **Đa mục đích** - dùng cho web, data science, AI, automation, ...

**Lịch sử:** Python được tạo bởi Guido van Rossum vào năm 1991. Tên gọi lấy từ bộ phim hài "Monty Python's Flying Circus".

---

## 🤔 Tại Sao Chọn Python?

✅ **Dễ Học** - Cú pháp đơn giản, gần giống tiếng Anh  
✅ **Mạnh Mẽ** - Dùng trong Google, Netflix, Instagram, Spotify  
✅ **Đa Dụng** - Web, Desktop, Mobile Backend, AI/ML, Data Science  
✅ **Cộng Đồng Lớn** - Nhiều thư viện, nhiều người hỗ trợ  
✅ **Tìm Việc Dễ** - Nhu cầu lập trình viên Python rất cao  

---

## 💻 Cài Đặt Python

### Trên Windows

**Bước 1:** Vào https://www.python.org/downloads/

**Bước 2:** Bấm nút "Download Python" (phiên bản mới nhất)

**Bước 3:** Chạy file `.exe` đã tải

**Bước 4:** ⚠️ **QUAN TRỌNG** - Chọn ☑️ "Add Python to PATH"

**Bước 5:** Click "Install Now"

**Bước 6:** Chờ cài đặt hoàn tất

### Trên macOS

**Bước 1:** Vào https://www.python.org/downloads/

**Bước 2:** Bấm nút macOS

**Bước 3:** Chạy file `.pkg`

**Bước 4:** Làm theo hướng dẫn trên màn hình

### Trên Linux (Ubuntu/Debian)

```bash
sudo apt-get update
sudo apt-get install python3 python3-pip
```

---

## ✅ Kiểm Tra Cài Đặt

Mở **Terminal** (macOS/Linux) hoặc **Command Prompt** (Windows) và gõ:

```bash
python3 --version
```

Nếu thấy phiên bản Python (ví dụ: `Python 3.9.0`), cài đặt thành công! 🎉

---

## 🖥️ Python Interactive Shell

Python Shell cho phép chạy code từng dòng một.

### Mở Python Shell

```bash
python3
```

Bạn sẽ thấy:

```
Python 3.x.x ...
>>> 
```

Dấu `>>>` là lời nhắc Python đang chờ bạn gõ lệnh.

### Ví Dụ Đầu Tiên

```python
>>> print("Xin chào Python!")
Xin chào Python!

>>> 2 + 3
5

>>> 10 * 5
50

>>> "Tôi" + " " + "yêu" + " " + "Python"
'Tôi yêu Python'
```

### Thoát Khỏi Python Shell

```python
>>> exit()
```

---

## 📝 Kiểu Dữ Liệu Cơ Bản

### 1. Số Nguyên (Integer)

```python
>>> age = 25
>>> type(age)
<class 'int'>
```

Số nguyên: ..., -2, -1, 0, 1, 2, ...

### 2. Số Thực (Float)

```python
>>> height = 1.75
>>> type(height)
<class 'float'>
```

Số thực: 1.5, 3.14, -2.5, ...

### 3. Chuỗi (String)

```python
>>> name = "Nguyễn Văn A"
>>> type(name)
<class 'str'>
```

Chuỗi: 'Hello', "Python", """Nhiều dòng"""

### 4. Boolean

```python
>>> is_student = True
>>> type(is_student)
<class 'bool'>
```

Boolean: `True` hoặc `False` (chữ hoa bắt buộc)

### 5. Danh Sách (List)

```python
>>> fruits = ['Chuối', 'Cam', 'Xoài']
>>> type(fruits)
<class 'list'>
```

Danh sách các phần tử: `[1, 2, 3]` hoặc `['a', 'b', 'c']`

### 6. Từ Điển (Dictionary)

```python
>>> person = {'name': 'Nguyễn', 'age': 25}
>>> type(person)
<class 'dict'>
```

Cặp key-value: `{'key': 'value'}`

### 7. Bộ Giá Trị (Tuple)

```python
>>> coordinates = (10, 20)
>>> type(coordinates)
<class 'tuple'>
```

Bộ cố định: `(1, 2, 3)` - không thể thay đổi

### 8. Tập Hợp (Set)

```python
>>> unique_numbers = {1, 2, 3}
>>> type(unique_numbers)
<class 'set'>
```

Tập hợp duy nhất: `{1, 2, 3}`

---

## 🔍 Kiểm Tra Kiểu Dữ Liệu

Sử dụng hàm `type()`:

```python
>>> print(type(42))
<class 'int'>

>>> print(type(3.14))
<class 'float'>

>>> print(type('Xin chào'))
<class 'str'>

>>> print(type([1, 2, 3]))
<class 'list'>

>>> print(type((1, 2)))
<class 'tuple'>

>>> print(type({1, 2, 3}))
<class 'set'>

>>> print(type({'name': 'Nam'}))
<class 'dict'>

>>> print(type(True))
<class 'bool'>
```

---

## 📝 Bình Luận (Comments)

Bình luận không được thực thi - dùng để giải thích code.

### Bình Luận Một Dòng

```python
# Đây là bình luận một dòng
x = 5  # Bình luận ở cuối dòng
```

### Bình Luận Nhiều Dòng

```python
"""
Đây là bình luận nhiều dòng.
Bạn có thể viết trên nhiều dòng.
Hữu ích khi giải thích hàm.
"""

'''
Cách khác để bình luận nhiều dòng
sử dụng dấu ngoặc kép đơn.
'''
```

---

## 🎯 Phép Toán Cơ Bản

```python
>>> 2 + 3       # Cộng: 5
>>> 10 - 3      # Trừ: 7
>>> 4 * 5       # Nhân: 20
>>> 10 / 2      # Chia: 5.0
>>> 10 // 3     # Chia lấy phần nguyên: 3
>>> 10 % 3      # Chia lấy dư: 1
>>> 2 ** 3      # Lũy thừa: 8
```

---

## 📄 Tạo File Python Đầu Tiên

### Bước 1: Mở Text Editor

Mở Visual Studio Code (hoặc editor yêu thích)

### Bước 2: Tạo File Mới

Tạo file tên `hello.py`

### Bước 3: Viết Code

```python
# Ngày 1 - Lần đầu học Python

print(2 + 3)             # Phép cộng
print(3 - 1)             # Phép trừ
print(2 * 3)             # Phép nhân
print(3 / 2)             # Phép chia
print(3 ** 2)            # Phép lũy thừa
print(3 % 2)             # Phép chia lấy dư
print(3 // 2)            # Phép chia lấy phần nguyên

# Kiểm tra kiểu dữ liệu
print(type(10))          # <class 'int'>
print(type(3.14))        # <class 'float'>
print(type('Xin chào'))  # <class 'str'>
print(type([1, 2, 3]))   # <class 'list'>
print(type({'name': 'Nam'}))  # <class 'dict'>
```

### Bước 4: Chạy File

Mở Terminal trong thư mục có file `hello.py` và gõ:

```bash
python3 hello.py
```

**Kết Quả:**

```
5
2
6
1.5
9
1
1
<class 'int'>
<class 'float'>
<class 'str'>
<class 'list'>
<class 'dict'>
```

---

## 🎓 Tóm Tắt Ngày 1

✅ Python là gì  
✅ Cài đặt Python thành công  
✅ Mở Python Shell  
✅ Học 8 kiểu dữ liệu cơ bản  
✅ Viết chương trình Python đầu tiên  
✅ Chạy file Python  

---

## 🚀 Tiếp Theo

Ngày 2 bạn sẽ học:
- Biến (Variables)
- Hàm Built-in
- Input/Output
