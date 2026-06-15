# 📘 Ngày 10 - Hàm (Function)

## 🎯 Mục Tiêu Ngày 10

- Hiểu hàm là gì
- Định nghĩa hàm với def
- Sử dụng tham số & trả về
- Hiểu scope (phạm vi)
- Sử dụng hàm built-in

---

## 🔧 Hàm (Function) Là Gì?

**Hàm** là khối code có tên, có thể được gọi lại nhiều lần.

### Cú Pháp

```python
def function_name(parameters):
    """Docstring - mô tả hàm"""
    # code
    return result
```

### Ví Dụ Đơn Giản

```python
# Hàm không tham số
def greet():
    print('Xin chào!')

greet()  # Xin chào!

# Hàm có tham số
def greet_person(name):
    print(f'Xin chào {name}!')

greet_person('Nguyễn')  # Xin chào Nguyễn!

# Hàm trả về giá trị
def add(a, b):
    return a + b

result = add(5, 3)
print(result)  # 8
```

---

## 📥 Tham Số (Parameters)

### Tham Số Vị Trí

```python
def info(name, age):
    print(f'{name}, {age} tuổi')

info('Nguyễn', 20)  # Nguyễn, 20 tuổi
```

### Tham Số Mặc Định

```python
def greet(name, greeting='Xin chào'):
    print(f'{greeting} {name}!')

greet('Nguyễn')  # Xin chào Nguyễn!
greet('Trần', 'Hi')  # Hi Trần!
```

### Tham Số Tên

```python
def info(name, age, city):
    print(f'{name}, {age}, {city}')

info(age=20, name='Nguyễn', city='Hà Nội')
```

### *args & **kwargs

```python
# *args - nhiều tham số vị trí
def sum_all(*numbers):
    return sum(numbers)

print(sum_all(1, 2, 3, 4))  # 10

# **kwargs - nhiều tham số tên
def print_info(**info):
    for key, value in info.items():
        print(f'{key}: {value}')

print_info(name='Nguyễn', age=20, city='Hà Nội')
```

---

## 📤 Return - Trả Về

```python
# Trả về một giá trị
def square(x):
    return x ** 2

print(square(5))  # 25

# Trả về nhiều giá trị
def get_info():
    return 'Nguyễn', 20, 'Hà Nội'

name, age, city = get_info()
print(name, age, city)
```

---

## 🔍 Scope - Phạm Vi

### Local Scope

```python
def greet():
    x = 'Hello'  # Local
    print(x)

greet()  # Hello
# print(x)  # Lỗi - x không tồn tại
```

### Global Scope

```python
x = 'Global'  # Global

def greet():
    print(x)

greet()  # Global
```

### global Keyword

```python
x = 10

def increment():
    global x
    x += 1

increment()
print(x)  # 11
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Tính BMI

```python
def calculate_bmi(weight, height):
    """Tính chỉ số BMI"""
    bmi = weight / (height ** 2)
    return bmi

weight = 70  # kg
height = 1.75  # m
bmi = calculate_bmi(weight, height)
print(f'BMI: {bmi:.2f}')
```

### Ví Dụ 2: Giai Thừa

```python
def factorial(n):
    """Tính giai thừa n!"""
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # 120
```

---

## 🚀 Tiếp Theo - Ngày 11

Ngày 11 bạn sẽ học:
- Module
- Import
- Thư viện math, random
