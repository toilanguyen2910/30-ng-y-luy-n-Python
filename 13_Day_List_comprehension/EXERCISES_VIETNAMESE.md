# 💻 Bài Tập Ngày 12

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: List Comprehension Cơ Bản

Tạo file `day_12_list_basics.py`:

```python
# Ngày 12 - List Comprehension

# Tạo danh sách bình phương từ 0-9
squares = [x ** 2 for x in range(10)]
print(f'Bình phương: {squares}')

# Tạo danh sách số chẵn từ 0-20
evens = [x for x in range(21) if x % 2 == 0]
print(f'Số chẵn: {evens}')

# Chuyển chuỗi thành chữ hoa
words = ['python', 'java', 'javascript', 'c++']
upper_words = [w.upper() for w in words]
print(f'Chữ hoa: {upper_words}')

# Lấy các từ có độ dài > 4
long_words = [w for w in words if len(w) > 4]
print(f'Từ dài: {long_words}')
```

---

### Bài 1.2: Dictionary Comprehension

```python
# Tạo dict từ danh sách
words = ['Python', 'Java', 'PHP', 'Go']
word_len = {w: len(w) for w in words}
print(f'Độ dài: {word_len}')

# Lọc dict
scores = {'Nam': 9, 'An': 7, 'Bình': 4, 'Chi': 8}
passed = {k: v for k, v in scores.items() if v >= 5}
print(f'Đậu: {passed}')

# Đảo ngược dict
original = {'a': 1, 'b': 2, 'c': 3}
reversed_dict = {v: k for k, v in original.items()}
print(f'Đảo ngược: {reversed_dict}')
```

---

### Bài 1.3: Set Comprehension

```python
# Loại bỏ trùng lặp
numbers = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
unique = {n for n in numbers}
print(f'Set duy nhất: {unique}')

# Bình phương số lẻ
odd_squares = {x ** 2 for x in range(10) if x % 2 != 0}
print(f'Bình phương lẻ: {odd_squares}')
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Phân Loại Dữ Liệu

Tạo file `day_12_advanced.py`:

```python
# Phân loại dữ liệu

numbers = [-5, -2, 0, 3, 7, 10]

# Phân loại âm/dương
labels = ['Dương' if n > 0 else 'Âm' if n < 0 else 'Số không' for n in numbers]
print(f'Số: {numbers}')
print(f'Nhãn: {labels}')

# Lọc và biến đổi
# Lấy số dương và nhân 10
transformed = [n * 10 for n in numbers if n > 0]
print(f'Dương x 10: {transformed}')
```

---

### Bài 2.2: Xử Lý Chuỗi Phức Tạp

```python
# Xử lý chuỗi

sentence = "Python là ngôn ngữ lập trình tuyệt vời"
words = sentence.split()

# Tạo dict thông tin từ
word_info = {w: {'length': len(w), 'upper': w.upper()} for w in words}

print("\nThông tin từ:")
for word, info in word_info.items():
    print(f"  {word}: {info}")
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Ma Trận (Matrix)

Tạo file `day_12_matrix.py`:

```python
# Làm việc với ma trận bằng comprehension

# Tạo ma trận 3x3 chứa toàn số 0
matrix = [[0 for _ in range(3)] for _ in range(3)]
print("Ma trận 3x3 (0):")
for row in matrix:
    print(row)

# Tạo bảng cửu chương 5
multiplication_table = [[i * j for j in range(1, 11)] for i in range(1, 6)]
print("\nBảng nhân (1-5):")
for row in multiplication_table:
    print(row)

# Làm phẳng ma trận (Flatten)
flat = [num for row in multiplication_table for num in row]
print(f"\nDanh sách phẳng (phần tử đầu): {flat[:10]}...")
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Hiểu List Comprehension
- [ ] Sử dụng if trong comprehension
- [ ] Sử dụng if/else trong comprehension
- [ ] Sử dụng Dictionary Comprehension
- [ ] Sử dụng Set Comprehension
- [ ] Tạo ma trận bằng comprehension
- [ ] Hoàn thành bài nâng cao

---

## 💡 Mẹo Quan Trọng

**1. Cấu trúc cơ bản:**
```python
[biểu_thức for biến in iterable if điều_kiện]
```

**2. If/Else:**
```python
[x if x > 0 else 0 for x in list]
```

**3. Dictionary:**
```python
{key: value for i in range(5)}
```
