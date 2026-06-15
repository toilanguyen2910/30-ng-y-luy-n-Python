# 💻 Bài Tập Ngày 5

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Tạo & Truy Cập Danh Sách

Tạo file `day_5_list_basics.py`:

```python
# Ngày 5 - Danh Sách

# Tạo danh sách
numbers = [1, 2, 3, 4, 5]
fruits = ['Chuối', 'Cam', 'Xoài']
mixed = [1, 'hello', 3.14, True]

# Truy cập
print(numbers[0])       # 1
print(fruits[-1])       # Xoài
print(mixed[1])         # hello

# Độ dài
print(len(numbers))     # 5

# Slicing
print(numbers[1:3])     # [2, 3]
print(numbers[::-1])    # [5, 4, 3, 2, 1]
```

---

### Bài 1.2: Thêm & Xóa Phần Tử

```python
# Thêm phần tử
fruits = ['Chuối', 'Cam']
fruits.append('Xoài')
print(fruits)  # ['Chuối', 'Cam', 'Xoài']

# Thêm tại vị trí
fruits.insert(1, 'Dâu')
print(fruits)  # ['Chuối', 'Dâu', 'Cam', 'Xoài']

# Xóa phần tử
fruits.remove('Dâu')
print(fruits)  # ['Chuối', 'Cam', 'Xoài']

# Xóa theo vị trí
last = fruits.pop()
print(last)     # Xoài
print(fruits)   # ['Chuối', 'Cam']
```

---

### Bài 1.3: Tìm Kiếm & Sắp Xếp

```python
# Tìm kiếm
numbers = [3, 1, 4, 1, 5, 9]

if 4 in numbers:
    print('Có số 4 trong danh sách')

print(numbers.index(4))     # 2
print(numbers.count(1))     # 2

# Sắp xếp
numbers.sort()
print(numbers)              # [1, 1, 3, 4, 5, 9]

# Đảo ngược
numbers.reverse()
print(numbers)              # [9, 5, 4, 3, 1, 1]
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Quản Lý Danh Sách

Tạo file `day_5_list_advanced.py`:

```python
# Quản lý danh sách

print("=== QUẢN LÝ SINH VIÊN ===\n")

# Nhập danh sách sinh viên
students = []
n = int(input("Nhập số lượng sinh viên: "))

for i in range(n):
    name = input(f"Sinh viên {i+1}: ")
    students.append(name)

# In danh sách
print("\nDanh sách sinh viên:")
for i, name in enumerate(students):
    print(f"{i+1}. {name}")

# Tìm kiếm
search_name = input("\nTìm kiếm: ")
if search_name in students:
    print(f"Vị trí: {students.index(search_name) + 1}")
else:
    print("Không tìm thấy")

# Sắp xếp
students.sort()
print(f"\nDanh sách sắp xếp:")
for name in students:
    print(f"  - {name}")
```

---

### Bài 2.2: Thống Kê Điểm

```python
# Thống kê điểm

print("=== THỐNG KÊ ĐIỂM ===\n")

# Nhập danh sách điểm
scores = []
n = int(input("Nhập số lượng học sinh: "))

for i in range(n):
    score = float(input(f"Điểm học sinh {i+1}: "))
    scores.append(score)

# Thống kê
print(f"\nTổng cộng: {sum(scores):.2f}")
print(f"Trung bình: {sum(scores) / len(scores):.2f}")
print(f"Cao nhất: {max(scores):.2f}")
print(f"Thấp nhất: {min(scores):.2f}")

# Sắp xếp
scores_sorted = sorted(scores, reverse=True)
print(f"\nXếp hạng (từ cao đến thấp):")
for i, score in enumerate(scores_sorted):
    print(f"{i+1}. {score:.2f}")
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Quản Lý Giỏ Hàng

Tạo file `day_5_shopping_cart.py`:

```python
# Quản lý giỏ hàng

print("=== GIỎ HÀNG ===\n")

cart = []

while True:
    print("\nMenu:")
    print("1. Thêm sản phẩm")
    print("2. Xem giỏ hàng")
    print("3. Xóa sản phẩm")
    print("4. Tính tổng")
    print("5. Thoát")
    
    choice = input("Chọn: ")
    
    if choice == '1':
        product = input("Tên sản phẩm: ")
        price = float(input("Giá: "))
        cart.append({'name': product, 'price': price})
        print("✓ Đã thêm")
    
    elif choice == '2':
        if not cart:
            print("Giỏ trống")
        else:
            for i, item in enumerate(cart):
                print(f"{i+1}. {item['name']}: {item['price']:,} VND")
    
    elif choice == '3':
        if cart:
            index = int(input("Xóa sản phẩm thứ: ")) - 1
            if 0 <= index < len(cart):
                cart.pop(index)
                print("✓ Đã xóa")
    
    elif choice == '4':
        total = sum(item['price'] for item in cart)
        print(f"Tổng tiền: {total:,} VND")
    
    elif choice == '5':
        break
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Tạo danh sách
- [ ] Truy cập phần tử
- [ ] Dùng slicing
- [ ] Sử dụng append()
- [ ] Sử dụng remove()
- [ ] Sử dụng sort()
- [ ] Tìm kiếm với in
- [ ] Hoàn thành bài tập cơ bản
- [ ] Hoàn thành bài tập nâng cao
- [ ] Hoàn thành thách thức

---

## 💡 Mẹo Quan Trọng

**1. Truy cập phần tử:**
```python
list[0]      # phần tử đầu
list[-1]     # phần tử cuối
list[1:3]    # từ index 1 đến 2
```

**2. Thêm & xóa:**
```python
list.append(x)     # thêm cuối
list.insert(0, x)  # thêm đầu
list.remove(x)     # xóa phần tử x
list.pop()         # xóa cuối
```

**3. Sắp xếp:**
```python
list.sort()              # sắp xếp tăng
list.sort(reverse=True)  # sắp xếp giảm
sorted(list)             # không thay đổi gốc
```
