# 💻 Bài Tập Ngày 6

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Tuple Cơ Bản

Tạo file `day_6_tuple_basics.py`:

```python
# Ngày 6 - Tuple & Set

# Tạo Tuple
colors = ('Đỏ', 'Xanh', 'Vàng')
numbers = (1, 2, 3, 4, 5)
mixed = (1, 'hello', 3.14)

# Truy cập
print(colors[0])       # Đỏ
print(colors[-1])      # Vàng

# Độ dài
print(len(colors))     # 3

# Slicing
print(numbers[1:3])    # (2, 3)

# Phương thức
print(numbers.count(2))    # 1
print(numbers.index(3))    # 2

# Kiểm tra
print('Xanh' in colors)    # True
```

---

### Bài 1.2: Set Cơ Bản

```python
# Tạo Set
numbers = set([1, 2, 2, 3, 3, 3])
print(numbers)     # {1, 2, 3}

# Thêm & xóa
s = {'a', 'b', 'c'}
s.add('d')
print(s)           # {'a', 'b', 'c', 'd'}

s.remove('b')
print(s)           # {'a', 'c', 'd'}

# Kiểm tra
print('a' in s)    # True
print(len(s))      # 3
```

---

### Bài 1.3: Phép Toán Set

```python
a = {1, 2, 3}
b = {2, 3, 4}

# Hợp (Union)
print(a | b)       # {1, 2, 3, 4}

# Giao (Intersection)
print(a & b)       # {2, 3}

# Hiệu (Difference)
print(a - b)       # {1}

# Đối xứng hiệu
print(a ^ b)       # {1, 4}
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Loại Bỏ Trùng Lặp

Tạo file `day_6_advanced.py`:

```python
# Loại bỏ phần tử trùng lặp

print("=== LOẠI BỎ TRÙNG LẶP ===\n")

# Danh sách có trùng
numbers = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
print(f"Danh sách gốc: {numbers}")
print(f"Số phần tử: {len(numbers)}")

# Dùng Set
unique = set(numbers)
print(f"Set duy nhất: {unique}")
print(f"Số phần tử duy nhất: {len(unique)}")

# Chuyển lại thành danh sách sắp xếp
unique_sorted = sorted(unique)
print(f"Danh sách sắp xếp: {unique_sorted}")
```

---

### Bài 2.2: Tìm Phần Tử Chung

```python
# Tìm phần tử chung

print("=== TÌM PHẦN TỬ CHUNG ===\n")

# Hai nhóm người
group1 = {'Nguyễn', 'Trần', 'Phạm', 'Lê'}
group2 = {'Phạm', 'Lê', 'Hoàng', 'Tùng'}

print(f"Nhóm 1: {group1}")
print(f"Nhóm 2: {group2}")

# Phần tử chung
common = group1 & group2
print(f"\nPhần tử chung: {common}")

# Chỉ ở nhóm 1
only_group1 = group1 - group2
print(f"Chỉ ở nhóm 1: {only_group1}")

# Chỉ ở nhóm 2
only_group2 = group2 - group1
print(f"Chỉ ở nhóm 2: {only_group2}")

# Tất cả
all_people = group1 | group2
print(f"Tất cả mọi người: {all_people}")
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Đếm Tần Suất

Tạo file `day_6_challenge.py`:

```python
# Đếm tần suất các ký tự

text = input("Nhập chuỗi: ")

# Đếm từng ký tự
freq = {}
for char in text:
    if char in freq:
        freq[char] += 1
    else:
        freq[char] = 1

# In kết quả
print(f"\nTần suất ký tự trong '{text}':")
for char, count in sorted(freq.items()):
    print(f"'{char}': {count}")

# Ký tự xuất hiện nhiều nhất
max_char = max(freq, key=freq.get)
print(f"\nKý tự xuất hiện nhiều nhất: '{max_char}' ({freq[max_char]} lần)")
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Tạo Tuple
- [ ] Truy cập phần tử Tuple
- [ ] Hiểu Tuple không thay đổi được
- [ ] Tạo Set
- [ ] Thêm/xóa phần tử Set
- [ ] Hiểu phép toán Set
- [ ] Loại bỏ trùng lặp
- [ ] Tìm phần tử chung

---

## 💡 Mẹo Quan Trọng

**1. Tuple:**
```python
t = (1, 2, 3)    # không thể thay đổi
t[0] = 10        # ❌ Lỗi!
```

**2. Set - loại bỏ trùng:**
```python
list_dup = [1, 1, 2, 2, 3]
unique = set(list_dup)  # {1, 2, 3}
```

**3. Phép toán Set:**
```python
a = {1, 2, 3}
b = {2, 3, 4}
a & b  # giao: {2, 3}
a | b  # hợp: {1, 2, 3, 4}
a - b  # hiệu: {1}
```
