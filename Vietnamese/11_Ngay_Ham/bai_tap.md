# 💻 Bài Tập Ngày 10

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Hàm Đơn Giản

Tạo file `day_10_function_basics.py`:

```python
# Ngày 10 - Hàm

# Hàm không tham số
def greet():
    print('Xin chào!')

greet()

# Hàm có tham số
def greet_person(name):
    print(f'Xin chào {name}!')

greet_person('Nguyễn')

# Hàm trả về giá trị
def add(a, b):
    return a + b

result = add(5, 3)
print(f'5 + 3 = {result}')

# Hàm tham số mặc định
def greet_formal(name, greeting='Xin chào'):
    print(f'{greeting} {name}!')

greet_formal('Nam')
greet_formal('Trần', 'Hi')
```

---

### Bài 1.2: Hàm Trả Về Nhiều Giá Trị

```python
# Trả về nhiều giá trị
def get_info():
    return 'Nguyễn', 20, 'Hà Nội'

name, age, city = get_info()
print(f'{name}, {age} tuổi, {city}')

# Hàm tính toán
def calculate(a, b):
    sum_val = a + b
    diff = a - b
    product = a * b
    return sum_val, diff, product

s, d, p = calculate(10, 3)
print(f'Tổng: {s}, Hiệu: {d}, Tích: {p}')
```

---

### Bài 1.3: *args & **kwargs

```python
# *args - danh sách tham số
def sum_all(*numbers):
    total = 0
    for num in numbers:
        total += num
    return total

print(sum_all(1, 2, 3))        # 6
print(sum_all(1, 2, 3, 4, 5))  # 15

# **kwargs - từ điển tham số
def print_info(**info):
    for key, value in info.items():
        print(f'{key}: {value}')

print_info(name='Nguyễn', age=20, city='Hà Nội')
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Hàm Toán Học

Tạo file `day_10_math_functions.py`:

```python
# Các hàm toán học

# 1. Tính BMI
def calculate_bmi(weight, height):
    """Tính chỉ số BMI
    weight: cân nặng (kg)
    height: chiều cao (m)
    """
    bmi = weight / (height ** 2)
    return bmi

weight = 70
height = 1.75
bmi = calculate_bmi(weight, height)
print(f'BMI: {bmi:.2f}')

# 2. Giai thừa
def factorial(n):
    """Tính giai thừa n!"""
    if n <= 1:
        return 1
    return n * factorial(n - 1)

print(f'5! = {factorial(5)}')

# 3. Kiểm tra số nguyên tố
def is_prime(n):
    """Kiểm tra số nguyên tố"""
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

for i in range(20):
    if is_prime(i):
        print(i, end=' ')
```

---

### Bài 2.2: Scope & Global

```python
# Scope - phạm vi

# Global variable
x = 100

def test_local():
    x = 10  # Local
    print(f'Local: {x}')

def test_global():
    global x
    x = 200  # Sửa global
    print(f'Global: {x}')

print(f'Trước: {x}')
test_local()
print(f'Sau local: {x}')
test_global()
print(f'Sau global: {x}')
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Tạo hàm đơn giản
- [ ] Sử dụng tham số
- [ ] Return giá trị
- [ ] Tham số mặc định
- [ ] *args
- [ ] **kwargs
- [ ] Hiểu scope
- [ ] Hoàn thành bài cơ bản
- [ ] Hoàn thành bài nâng cao

---

## 💡 Mẹo Quan Trọng

**1. Hàm cơ bản:**
```python
def function_name(param):
    return result
```

**2. Tham số mặc định:**
```python
def greet(name, msg='Hi'):
    print(f'{msg} {name}')
```

**3. *args:**
```python
def add(*nums):
    return sum(nums)
```
