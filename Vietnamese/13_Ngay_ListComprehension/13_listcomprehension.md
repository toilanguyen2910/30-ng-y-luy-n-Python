# 📘 Ngày 12 - List Comprehension

## 🎯 Mục Tiêu Ngày 12

- Hiểu List Comprehension
- Sử dụng điều kiện trong List Comprehension
- Dictionary Comprehension
- Set Comprehension

---

## 📝 List Comprehension Là Gì?

**List Comprehension** là cách ngắn gọn để tạo danh sách từ danh sách khác.

### Cú Pháp

```python
[biểu_thức for biến in iterable]
[biểu_thức for biến in iterable if điều_kiện]
```

### Ví Dụ Cơ Bản

```python
# Cách truyền thống
squares = []
for x in range(10):
    squares.append(x ** 2)

# List Comprehension
squares = [x ** 2 for x in range(10)]
print(squares)  # [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

---

## ✅ List Comprehension Với Điều Kiện

```python
# Chỉ số chẵn
evens = [x for x in range(10) if x % 2 == 0]
print(evens)  # [0, 2, 4, 6, 8]

# Chuyển thành chữ hoa
words = ['python', 'java', 'javascript']
upper_words = [w.upper() for w in words]
print(upper_words)  # ['PYTHON', 'JAVA', 'JAVASCRIPT']

# Lọc số dương
numbers = [-3, -1, 0, 2, 4, 6]
positives = [n for n in numbers if n > 0]
print(positives)  # [2, 4, 6]
```

---

## 🔀 If/Else Trong List Comprehension

```python
# Phân loại số
numbers = [-2, -1, 0, 1, 2]
labels = ['âm' if n < 0 else 'không' if n == 0 else 'dương' for n in numbers]
print(labels)  # ['âm', 'âm', 'không', 'dương', 'dương']

# Làm tròn
values = [1.1, 2.5, 3.7, 4.2]
rounded = [int(v) if v < 3 else round(v) for v in values]
print(rounded)  # [1, 2, 4, 4]
```

---

## 📖 Dictionary Comprehension

```python
# Tạo dict từ danh sách
words = ['python', 'java', 'go']
word_lengths = {w: len(w) for w in words}
print(word_lengths)  # {'python': 6, 'java': 4, 'go': 2}

# Đảo ngược key-value
original = {'a': 1, 'b': 2, 'c': 3}
reversed_dict = {v: k for k, v in original.items()}
print(reversed_dict)  # {1: 'a', 2: 'b', 3: 'c'}

# Với điều kiện
scores = {'A': 9, 'B': 7, 'C': 5, 'D': 3}
passed = {k: v for k, v in scores.items() if v >= 5}
print(passed)  # {'A': 9, 'B': 7, 'C': 5}
```

---

## 🔢 Set Comprehension

```python
# Loại bỏ trùng lặp
numbers = [1, 1, 2, 2, 3, 3]
unique = {n for n in numbers}
print(unique)  # {1, 2, 3}

# Bình phương các số duy nhất
squares = {x ** 2 for x in range(-3, 4)}
print(squares)  # {0, 1, 4, 9}
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Tính Bình Phương

```python
numbers = [1, 2, 3, 4, 5]
squares = [n ** 2 for n in numbers]
print(squares)  # [1, 4, 9, 16, 25]
```

### Ví Dụ 2: Lọc Chuỗi

```python
words = ['Python', 'Java', 'Go', 'JavaScript']
long_words = [w for w in words if len(w) > 4]
print(long_words)  # ['Python', 'JavaScript']
```

---

## 🚀 Tiếp Theo - Ngày 13

Ngày 13 bạn sẽ học:
- Higher Order Functions
- map(), filter(), reduce()
- Lambda
