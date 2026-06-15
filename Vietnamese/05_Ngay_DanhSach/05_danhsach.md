# 📘 Ngày 5 - Danh Sách (List)

## 🎯 Mục Tiêu Ngày 5

- Hiểu danh sách là gì
- Tạo và truy cập phần tử trong danh sách
- Sử dụng các phương thức danh sách
- Cắt danh sách (List Slicing)
- Sắp xếp và sửa đổi danh sách

---

## 📋 Danh Sách (List) Là Gì?

**Danh sách** là tập hợp các phần tử được bao quanh bởi dấu ngoặc vuông `[ ]`.
Danh sách có thể chứa các kiểu dữ liệu khác nhau.

### Tạo Danh Sách

```python
# Danh sách rỗng
empty_list = []

# Danh sách số
numbers = [1, 2, 3, 4, 5]

# Danh sách chuỗi
fruits = ['Chuối', 'Cam', 'Xoài']

# Danh sách hỗn hợp
mixed = [1, 'hello', 3.14, True]

# Danh sách lồng nhau
nested = [[1, 2], ['a', 'b'], [3.14, 2.71]]
```

---

## 🔍 Truy Cập Phần Tử

### Indexing

```python
fruits = ['Chuối', 'Cam', 'Xoài', 'Dâu']
#          0       1      2       3

print(fruits[0])    # Chuối
print(fruits[1])    # Cam
print(fruits[-1])   # Dâu (phần tử cuối)
print(fruits[-2])   # Xoài (phần tử thứ 2 từ cuối)
```

### Độ Dài

```python
fruits = ['Chuối', 'Cam', 'Xoài']
print(len(fruits))  # 3
```

---

## ✂️ Cắt Danh Sách (Slicing)

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# Lấy 3 phần tử đầu
print(numbers[:3])      # [0, 1, 2]

# Lấy từ phần tử thứ 2 đến 5
print(numbers[2:5])     # [2, 3, 4]

# Lấy từ phần tử thứ 5 đến cuối
print(numbers[5:])      # [5, 6, 7, 8, 9]

# Lấy mỗi phần tử thứ 2
print(numbers[::2])     # [0, 2, 4, 6, 8]

# Đảo ngược danh sách
print(numbers[::-1])    # [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
```

---

## ➕ Thêm & Xóa Phần Tử

### append() - Thêm Vào Cuối

```python
fruits = ['Chuối', 'Cam']
fruits.append('Xoài')
print(fruits)  # ['Chuối', 'Cam', 'Xoài']
```

### insert() - Thêm Vào Vị Trí

```python
fruits = ['Chuối', 'Xoài']
fruits.insert(1, 'Cam')
print(fruits)  # ['Chuối', 'Cam', 'Xoài']
```

### extend() - Thêm Nhiều Phần Tử

```python
fruits = ['Chuối', 'Cam']
fruits.extend(['Xoài', 'Dâu'])
print(fruits)  # ['Chuối', 'Cam', 'Xoài', 'Dâu']
```

### remove() - Xóa Phần Tử

```python
fruits = ['Chuối', 'Cam', 'Xoài']
fruits.remove('Cam')
print(fruits)  # ['Chuối', 'Xoài']
```

### pop() - Xóa Và Lấy Phần Tử

```python
fruits = ['Chuối', 'Cam', 'Xoài']
last = fruits.pop()        # Xóa phần tử cuối
print(last)                # Xoài
print(fruits)              # ['Chuối', 'Cam']

first = fruits.pop(0)      # Xóa phần tử đầu
print(first)               # Chuối
```

### clear() - Xóa Tất Cả

```python
fruits = ['Chuối', 'Cam']
fruits.clear()
print(fruits)  # []
```

---

## 🔍 Tìm Kiếm & Đếm

### index() - Tìm Vị Trí

```python
fruits = ['Chuối', 'Cam', 'Xoài']
print(fruits.index('Cam'))  # 1
```

### count() - Đếm Phần Tử

```python
numbers = [1, 2, 2, 3, 2, 4]
print(numbers.count(2))     # 3
```

### in - Kiểm Tra Tồn Tại

```python
fruits = ['Chuối', 'Cam', 'Xoài']
print('Cam' in fruits)      # True
print('Táo' in fruits)      # False
```

---

## 🔄 Sắp Xếp & Đảo Ngược

### sort() - Sắp Xếp

```python
numbers = [3, 1, 4, 1, 5, 9]
numbers.sort()
print(numbers)  # [1, 1, 3, 4, 5, 9]

# Sắp xếp giảm dần
numbers.sort(reverse=True)
print(numbers)  # [9, 5, 4, 3, 1, 1]

# Sắp xếp chuỗi
fruits = ['Xoài', 'Chuối', 'Cam']
fruits.sort()
print(fruits)   # ['Chuối', 'Cam', 'Xoài']
```

### reverse() - Đảo Ngược

```python
numbers = [1, 2, 3, 4, 5]
numbers.reverse()
print(numbers)  # [5, 4, 3, 2, 1]
```

### sorted() - Hàm Sắp Xếp

```python
numbers = [3, 1, 4, 1, 5]
sorted_list = sorted(numbers)
print(sorted_list)  # [1, 1, 3, 4, 5]
print(numbers)      # [3, 1, 4, 1, 5] (không thay đổi)
```

---

## 📋 Tóm Tắt Phương Thức

| Phương Thức | Ý Nghĩa | Ví Dụ |
|------------|---------|-------|
| append() | Thêm vào cuối | list.append(5) |
| insert() | Thêm tại vị trí | list.insert(0, 'x') |
| extend() | Thêm nhiều phần tử | list.extend([1,2]) |
| remove() | Xóa phần tử | list.remove('x') |
| pop() | Xóa và lấy | list.pop() |
| clear() | Xóa tất cả | list.clear() |
| sort() | Sắp xếp | list.sort() |
| reverse() | Đảo ngược | list.reverse() |
| index() | Tìm vị trí | list.index('x') |
| count() | Đếm | list.count('x') |

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Quản Lý Danh Sách Sinh Viên

```python
# Danh sách sinh viên
students = []

# Thêm sinh viên
students.append('Nguyễn Văn A')
students.append('Trần Thị B')
students.append('Phạm Văn C')

print(f"Tổng sinh viên: {len(students)}")
print(f"Danh sách:")
for i, name in enumerate(students):
    print(f"  {i+1}. {name}")

# Tìm sinh viên
if 'Trần Thị B' in students:
    index = students.index('Trần Thị B')
    print(f"Vị trí của Trần Thị B: {index + 1}")
```

### Ví Dụ 2: Thống Kê Điểm

```python
# Danh sách điểm
scores = [8.5, 7.0, 9.0, 6.5, 8.0]

print(f"Tổng điểm: {sum(scores)}")
print(f"Điểm cao nhất: {max(scores)}")
print(f"Điểm thấp nhất: {min(scores)}")
print(f"Điểm trung bình: {sum(scores) / len(scores):.2f}")

# Sắp xếp
scores_sorted = sorted(scores, reverse=True)
print(f"Xếp hạng: {scores_sorted}")
```

---

## 🚀 Tiếp Theo - Ngày 6

Ngày 6 bạn sẽ học:
- Bộ giá trị (Tuple)
- Tập hợp (Set)
- So sánh List, Tuple, Set
