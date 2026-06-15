# 📘 Ngày 14 - Lỗi Trong Python & Xử Lý Ngoại Lệ

## 🎯 Mục Tiêu Ngày 14

- Hiểu các loại lỗi phổ biến
- Sử dụng try/except
- Sử dụng else, finally
- Bắt nhiều loại exception
- Tự tạo exception

---

## 🚫 Các Loại Error Phổ Biến

### SyntaxError - Lỗi Cú Pháp

```python
# ❌ Thiếu dấu hai chấm
# if x > 5
#     print(x)

# ✅ Đúng
if x > 5:
    print(x)
```

### NameError - Biến Chưa Định Nghĩa

```python
# ❌ print(x) -> NameError nếu x chưa định nghĩa
```

### TypeError - Sai Kiểu Dữ Liệu

```python
# ❌ print(len(5)) -> TypeError: len() expects iterable
print(len('hello'))  # ✅
```

### ValueError - Giá Trị Không Hợp Lệ

```python
# ❌ int('abc') -> ValueError: invalid literal
print(int('123'))  # ✅
```

### IndexError - Sai Index

```python
numbers = [1, 2, 3]
# ❌ print(numbers[5]) -> IndexError: list index out of range
```

### ZeroDivisionError - Chia Cho 0

```python
# ❌ print(10 / 0) -> ZeroDivisionError
```

---

## 🔧 try/except - Bắt Lỗi Cơ Bản

```python
try:
    # Code có thể gây lỗi
    num = int(input('Nhập số: '))
    result = 10 / num
    print(f'Kết quả: {result}')
except ZeroDivisionError:
    print('Lỗi: Chia cho 0!')
except ValueError:
    print('Lỗi: Định dạng số không hợp lệ!')
```

### try/except/else/finally

```python
try:
    num = int(input('Nhập số: '))
    result = 10 / num
except ZeroDivisionError:
    print('Không thể chia cho 0')
except ValueError:
    print('Nhập sai định dạng')
else:
    print(f'Kết quả: {result}')  # Chạy nếu không có lỗi
finally:
    print('Kết thúc')  # Luôn chạy
```

---

## 🎯 Bắt Nhiều Exception

```python
try:
    x = int(input('Số: '))
    y = [1, 2, 3]
    print(y[x])
except (ValueError, IndexError) as e:
    print(f'Lỗi: {e}')
```

### Exception Tổng Quát (Không Nên)

```python
try:
    file = open('data.txt')
    content = file.read()
except:  # Bắt tất cả
    print('Có lỗi!')
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Xử Lý Nhập Dữ Liệu

```python
def get_number(prompt):
    while True:
        try:
            num = float(input(prompt))
            return num
        except ValueError:
            print('Số không hợp lệ! Nhập lại.')

age = get_number('Nhập tuổi: ')
print(f'Tuổi: {age}')
```

### Ví Dụ 2: Xử Lý File

```python
try:
    file = open('data.txt', 'r')
    data = file.read()
    print(data)
except FileNotFoundError:
    print('Không tìm thấy file')
except PermissionError:
    print('Không có quyền đọc')
finally:
    try:
        file.close()
    except:
        pass
```

---

## 🚀 Tiếp Theo - Ngày 15

Ngày 15 bạn sẽ học:
- File Handling
- Đọc và ghi file
- with statement
- Các mode xử lý file
