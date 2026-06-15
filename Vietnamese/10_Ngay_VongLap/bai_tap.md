# 💻 Bài Tập Ngày 9

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: For Loop Cơ Bản

Tạo file `day_9_for_basics.py`:

```python
# Ngày 9 - Vòng Lặp

# Lặp danh sách
fruits = ['Chuối', 'Cam', 'Xoài']
for fruit in fruits:
    print(fruit)

# Lặp chuỗi
for char in 'Python':
    print(char)

# Lặp với range
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4

# Lặp với range(start, stop, step)
for i in range(0, 10, 2):
    print(i)  # 0, 2, 4, 6, 8
```

---

### Bài 1.2: enumerate() & While

```python
# enumerate - lấy index
fruits = ['Chuối', 'Cam', 'Xoài']
for idx, fruit in enumerate(fruits):
    print(f'{idx}: {fruit}')

# While cơ bản
count = 0
while count < 3:
    print(f'Count: {count}')
    count += 1

# While vô tận + break
while True:
    user = input('Nhập "thoát" để dừng: ')
    if user == 'thoát':
        break
    print(f'Bạn nhập: {user}')
```

---

### Bài 1.3: Break & Continue

```python
# Break - dừng
for i in range(10):
    if i == 5:
        break
    print(i)  # 0, 1, 2, 3, 4

# Continue - bỏ qua
for i in range(5):
    if i == 2:
        continue
    print(i)  # 0, 1, 3, 4
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Bảng Cửu Chương

Tạo file `day_9_multiplication.py`:

```python
# Bảng cửu chương

n = int(input('Nhập số (1-9): '))

print(f'\nBảng cửu chương {n}:')
for i in range(1, 10):
    result = n * i
    print(f'{n} × {i} = {result}')
```

---

### Bài 2.2: Tính Tổng Số

```python
# Tính tổng 1 + 2 + ... + n

n = int(input('Nhập n: '))
total = 0

for i in range(1, n + 1):
    total += i

print(f'Tổng từ 1 đến {n}: {total}')

# Kiểm chứng công thức
formula_result = n * (n + 1) // 2
print(f'Công thức: {formula_result}')
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Hình Tam Giác

Tạo file `day_9_triangle.py`:

```python
# Vẽ hình tam giác

n = int(input('Nhập chiều cao: '))

print('\nHình tam giác:')
for i in range(1, n + 1):
    print('*' * i)

print('\nHình tam giác ngược:')
for i in range(n, 0, -1):
    print('*' * i)
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Sử dụng for với danh sách
- [ ] Sử dụng range()
- [ ] Sử dụng enumerate()
- [ ] Sử dụng while
- [ ] Sử dụng break
- [ ] Sử dụng continue
- [ ] Hoàn thành bài cơ bản
- [ ] Hoàn thành bài nâng cao
- [ ] Hoàn thành thách thức

---

## 💡 Mẹo Quan Trọng

**1. For cơ bản:**
```python
for item in list:
    print(item)
```

**2. range() hữu ích:**
```python
range(5)         # 0,1,2,3,4
range(2, 5)      # 2,3,4
range(0, 10, 2)  # 0,2,4,6,8
```

**3. enumerate():**
```python
for i, item in enumerate(list):
    print(f'{i}: {item}')
```
