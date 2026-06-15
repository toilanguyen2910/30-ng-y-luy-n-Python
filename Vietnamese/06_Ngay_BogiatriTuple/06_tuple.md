# 📘 Ngày 6 - Bộ Giá Trị Tuple & Tập Hợp Set

## 🎯 Mục Tiêu Ngày 6

- Hiểu Tuple là gì
- Hiểu Set là gì
- So sánh List, Tuple, Set
- Sử dụng các phương thức Tuple & Set
- Biết khi nào dùng cái nào

---

## 📦 Bộ Giá Trị (Tuple)

**Tuple** là tập hợp các phần tử được bao quanh bởi dấu ngoặc tròn `( )`.
**Đặc điểm quan trọng:** Tuple **không thể thay đổi** (immutable).

### Tạo Tuple

```python
# Tuple rỗng
empty_tuple = ()

# Tuple với một phần tử
single = (1,)  # Lưu ý: phải có dấu phẩy

# Tuple nhiều phần tử
colors = ('Đỏ', 'Xanh', 'Vàng')

# Tuple hỗn hợp
mixed = (1, 'hello', 3.14, True)

# Tuple lồng nhau
nested = ((1, 2), ('a', 'b'), (3, 4))

# Không cần ngoặc
tuple_no_paren = 1, 2, 3
print(tuple_no_paren)  # (1, 2, 3)
```

### Truy Cập Phần Tử

```python
colors = ('Đỏ', 'Xanh', 'Vàng')

print(colors[0])    # Đỏ
print(colors[-1])   # Vàng
print(colors[1:])   # ('Xanh', 'Vàng')
```

### Phương Thức Tuple

```python
numbers = (1, 2, 3, 2, 4, 2)

# count() - đếm
print(numbers.count(2))     # 3

# index() - tìm vị trí
print(numbers.index(3))     # 2

# len() - độ dài
print(len(numbers))         # 6

# in - kiểm tra
print(2 in numbers)         # True
```

### Lợi Ích của Tuple

✅ **An toàn** - không thể sửa đổi  
✅ **Nhanh** - tối ưu hơn List  
✅ **Làm khóa** - có thể dùng làm dict key  
✅ **Unpack** - dễ gán giá trị  

### Unpacking Tuple

```python
# Unpacking
x, y, z = (1, 2, 3)
print(x, y, z)      # 1 2 3

# Swap
a, b = 10, 20
a, b = b, a
print(a, b)         # 20 10

# Unpacking với *
first, *middle, last = (1, 2, 3, 4, 5)
print(first)        # 1
print(middle)       # [2, 3, 4]
print(last)         # 5
```

---

## 🔖 Tập Hợp (Set)

**Set** là tập hợp các phần tử duy nhất được bao quanh bởi dấu ngoặc nhọn `{ }`.
**Đặc điểm:** Set **không có thứ tự** và **không có phần tử trùng lặp**.

### Tạo Set

```python
# Set rỗng (cẩn thận: {} là dict)
empty_set = set()

# Set từ danh sách
numbers = set([1, 2, 2, 3, 3, 3])
print(numbers)      # {1, 2, 3}

# Set trực tiếp
colors = {'Đỏ', 'Xanh', 'Vàng'}

# Set từ chuỗi
chars = set('hello')
print(chars)        # {'h', 'e', 'l', 'o'}
```

### Phương Thức Set

```python
a = {1, 2, 3}
b = {2, 3, 4}

# add() - thêm
a.add(4)
print(a)            # {1, 2, 3, 4}

# remove() - xóa (lỗi nếu không có)
a.remove(4)
print(a)            # {1, 2, 3}

# discard() - xóa (an toàn)
a.discard(10)       # không lỗi

# pop() - xóa ngẫu nhiên
item = a.pop()
print(item)         # 1 (hoặc khác)

# clear() - xóa tất cả
a.clear()
print(a)            # set()

# len() - số phần tử
print(len(b))       # 3

# in - kiểm tra
print(2 in b)       # True
```

### Phép Toán Tập Hợp

```python
a = {1, 2, 3}
b = {2, 3, 4}

# Hợp (Union) - |
print(a | b)        # {1, 2, 3, 4}
print(a.union(b))   # {1, 2, 3, 4}

# Giao (Intersection) - &
print(a & b)        # {2, 3}
print(a.intersection(b))  # {2, 3}

# Hiệu (Difference) - -
print(a - b)        # {1}
print(a.difference(b))    # {1}

# Đối xứng hiệu (Symmetric Difference) - ^
print(a ^ b)        # {1, 4}
print(a.symmetric_difference(b))  # {1, 4}
```

---

## 📊 So Sánh List, Tuple, Set

| Đặc Điểm | List | Tuple | Set |
|---------|------|-------|-----|
| Tạo | `[]` | `()` | `{}` |
| Thay đổi được | ✓ | ✗ | ✓ |
| Có thứ tự | ✓ | ✓ | ✗ |
| Phần tử duy nhất | ✗ | ✗ | ✓ |
| Dùng làm key | ✗ | ✓ | ✗ |
| Tốc độ | Chậm | Nhanh | Cực nhanh |
| Dùng khi | Sửa đổi | Bảo vệ | Duy nhất |

---

## 💡 Khi Nào Dùng Cái Nào?

**Dùng List khi:**
- Cần thêm/xóa/sửa phần tử
- Cần giữ thứ tự
- Phần tử có thể trùng lặp

```python
students = ['Nguyễn', 'Trần', 'Phạm']
students.append('Lê')
```

**Dùng Tuple khi:**
- Không muốn sửa đổi dữ liệu
- Làm khóa trong dictionary
- Trả về nhiều giá trị từ hàm

```python
coordinates = (10, 20, 30)  # không thay đổi
colors = {('R', 'G', 'B'): 'RGB'}  # dùng làm key
```

**Dùng Set khi:**
- Cần phần tử duy nhất
- Kiểm tra tồn tại nhanh
- Phép toán tập hợp

```python
unique_numbers = set([1, 1, 2, 2, 3])  # {1, 2, 3}
if 2 in unique_numbers:  # nhanh
    pass
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Loại Bỏ Phần Tử Trùng

```python
# Loại bỏ số trùng lặp
numbers = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
unique = set(numbers)
print(unique)         # {1, 2, 3, 4}
print(sorted(unique)) # [1, 2, 3, 4]
```

### Ví Dụ 2: Tìm Phần Tử Chung

```python
# Những người tham gia cả 2 sự kiện
event1 = {'Nguyễn', 'Trần', 'Phạm', 'Lê'}
event2 = {'Phạm', 'Lê', 'Hoàng', 'Tùng'}

# Giao
both = event1 & event2
print(both)           # {'Phạm', 'Lê'}

# Chỉ sự kiện 1
only_event1 = event1 - event2
print(only_event1)    # {'Nguyễn', 'Trần'}
```

---

## 🚀 Tiếp Theo - Ngày 7

Ngày 7 bạn sẽ học:
- Từ điển (Dictionary)
- Các phương thức từ điển
- Lặp qua từ điển
