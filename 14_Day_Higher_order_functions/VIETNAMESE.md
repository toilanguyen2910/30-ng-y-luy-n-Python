# 📘 Ngày 13 - Hàm Bậc Cao (Higher Order Functions)

## 🎯 Mục Tiêu Ngày 13

- Hiểu Hàm Bậc Cao (HOF)
- Sử dụng hàm Lambda
- Sử dụng map(), filter(), reduce()
- Hiểu closures và decorators cơ bản

---

## 🔝 Hàm Bậc Cao (HOF) Là Gì?

**Hàm bậc cao** là hàm có thể:
1. Nhận hàm khác làm tham số
2. Trả về một hàm

### Ví Dụ Nhận Hàm Làm Tham Số

```python
def square(x):
    return x ** 2

def apply_func(f, x):
    return f(x)

print(apply_func(square, 5))  # 25
```

---

## ƛ Hàm Lambda (Anonymous Functions)

**Lambda** là hàm ẩn danh (không tên), dùng cho các thao tác đơn giản.

### Cú Pháp
```python
lambda tham_số: biểu_thức
```

### Ví Dụ
```python
# Cách thông thường
def add(a, b):
    return a + b

# Cách Lambda
add_lambda = lambda a, b: a + b
print(add_lambda(5, 3))  # 8

# Bình phương
square = lambda x: x ** 2
print(square(5))  # 25
```

---

## 🗺️ Hàm map()

**map()** áp dụng một hàm lên tất cả các phần tử của một list (iterable).

### Cú Pháp
```python
map(hàm, iterable)
```

### Ví Dụ
```python
numbers = [1, 2, 3, 4, 5]

# Bình phương các số
squares = list(map(lambda x: x ** 2, numbers))
print(squares)  # [1, 4, 9, 16, 25]

# Chuyển sang chữ hoa
words = ['python', 'java', 'js']
upper = list(map(str.upper, words))
print(upper)  # ['PYTHON', 'JAVA', 'JS']
```

---

## 🧪 Hàm filter()

**filter()** lọc các phần tử dựa trên một điều kiện (hàm trả về True/False).

### Cú Pháp
```python
filter(hàm_điều_kiện, iterable)
```

### Ví Dụ
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Lọc số chẵn
evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)  # [2, 4, 6, 8, 10]

# Lọc từ dài
words = ['Go', 'Python', 'C', 'Java']
long_words = list(filter(lambda w: len(w) > 3, words))
print(long_words)  # ['Python', 'Java']
```

---

## 📉 Hàm reduce()

**reduce()** thực hiện tính toán tích lũy trên một list để trả về **một giá trị duy nhất**.
(Lưu ý: phải import từ `functools`)

### Cú Pháp
```python
from functools import reduce
reduce(hàm_tích_lũy, iterable)
```

### Ví Dụ
```python
from functools import reduce

numbers = [1, 2, 3, 4, 5]

# Tính tổng
total = reduce(lambda x, y: x + y, numbers)
print(total)  # 15

# Tìm số lớn nhất
maximum = reduce(lambda x, y: x if x > y else y, numbers)
print(maximum)  # 5
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Xử Lý Dữ Liệu Sinh Viên

```python
students = [
    {'name': 'Nam', 'score': 8.5},
    {'name': 'An', 'score': 4.0},
    {'name': 'Bình', 'score': 7.0},
    {'name': 'Chi', 'score': 9.0}
]

# Lọc sinh viên đậu (score >= 5)
passed = list(filter(lambda s: s['score'] >= 5, students))

# Lấy danh sách tên sinh viên đậu
passed_names = list(map(lambda s: s['name'], passed))

print(f"Sinh viên đậu: {passed_names}")
# ['Nam', 'Bình', 'Chi']
```

### Ví Dụ 2: Tính Giai Thừa Với reduce

```python
from functools import reduce

def factorial(n):
    if n == 0: return 1
    return reduce(lambda x, y: x * y, range(1, n + 1))

print(factorial(5))  # 120
```

---

## 🚀 Tiếp Theo - Ngày 14

Ngày 14 bạn sẽ học:
- Python Type Errors
- Xử lý ngoại lệ (Exception Handling)
- Try/Except/Finally
- Các loại lỗi phổ biến
