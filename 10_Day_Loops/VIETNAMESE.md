# 📘 Ngày 9 - Vòng Lặp (Loops)

## 🎯 Mục Tiêu Ngày 9

- Hiểu vòng lặp for
- Hiểu vòng lặp while
- Sử dụng break & continue
- Sử dụng range()
- Lặp qua danh sách & chuỗi

---

## 🔁 Vòng Lặp For

**For** dùng để lặp qua các phần tử trong danh sách, chuỗi, hay range.

### For Cơ Bản

```python
# Lặp qua danh sách
fruits = ['Chuối', 'Cam', 'Xoài']
for fruit in fruits:
    print(fruit)

# Lặp qua chuỗi
for char in 'Python':
    print(char)

# Lặp từ 0 đến 4
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4
```

### range() - Hàm Quan Trọng

```python
# range(stop)
for i in range(3):
    print(i)  # 0, 1, 2

# range(start, stop)
for i in range(2, 5):
    print(i)  # 2, 3, 4

# range(start, stop, step)
for i in range(0, 10, 2):
    print(i)  # 0, 2, 4, 6, 8
```

### enumerate() - Lấy Index

```python
fruits = ['Chuối', 'Cam', 'Xoài']

for index, fruit in enumerate(fruits):
    print(f'{index}: {fruit}')
# 0: Chuối
# 1: Cam
# 2: Xoài
```

---

## ⏱️ Vòng Lặp While

**While** lặp khi điều kiện còn đúng.

### While Cơ Bản

```python
count = 0
while count < 5:
    print(count)
    count += 1
# 0, 1, 2, 3, 4
```

### While Vô Tận & Break

```python
while True:
    user_input = input('Nhập "thoát" để dừng: ')
    if user_input == 'thoát':
        break
    print(f'Bạn nhập: {user_input}')
```

---

## 🚦 Break & Continue

### break - Dừng Vòng Lặp

```python
for i in range(10):
    if i == 5:
        break
    print(i)  # 0, 1, 2, 3, 4
```

### continue - Bỏ Qua

```python
for i in range(5):
    if i == 2:
        continue
    print(i)  # 0, 1, 3, 4
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Bảng Cửu Chương

```python
n = int(input('Nhập số (1-9): '))

for i in range(1, 10):
    result = n * i
    print(f'{n} × {i} = {result}')
```

### Ví Dụ 2: Tổng Số

```python
n = int(input('Nhập n: '))
total = 0

for i in range(1, n + 1):
    total += i

print(f'Tổng 1 + 2 + ... + {n} = {total}')
```

---

## 🚀 Tiếp Theo - Ngày 10

Ngày 10 bạn sẽ học:
- Hàm (Function)
- Tham số & trả về
- Scope
