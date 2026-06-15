# 💻 Bài Tập Ngày 13

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Lambda Functions

Tạo file `day_13_lambda.py`:

```python
# Ngày 13 - Hàm Lambda

# Hàm nhân 2 số
multiply = lambda a, b: a * b
print(f'5 * 3 = {multiply(5, 3)}')

# Hàm kiểm tra số chẵn
is_even = lambda x: x % 2 == 0
print(f'4 là số chẵn: {is_even(4)}')
print(f'5 là số chẵn: {is_even(5)}')

# Hàm nối chuỗi
concat = lambda a, b: f'{a} {b}'
print(concat('Hello', 'Python'))
```

---

### Bài 1.2: Sử Dụng map()

```python
# map() cơ bản
numbers = [1, 2, 3, 4, 5]

# Bình phương (dùng lambda)
squares = list(map(lambda x: x ** 2, numbers))
print(f'Bình phương: {squares}')

# Gấp đôi (dùng hàm)
def double(x):
    return x * 2

doubles = list(map(double, numbers))
print(f'Gấp đôi: {doubles}')

# Xử lý chuỗi
names = ['nam', 'an', 'bình']
caps = list(map(str.capitalize, names))
print(f'Tên viết hoa: {caps}')
```

---

### Bài 1.3: Sử Dụng filter()

```python
# filter() cơ bản
numbers = [1, -2, 3, -4, 5, 0]

# Lọc số dương
positives = list(filter(lambda x: x > 0, numbers))
print(f'Số dương: {positives}')

# Lọc chuỗi dài
words = ['python', 'c', 'java', 'go', 'js']
long_words = list(filter(lambda w: len(w) > 3, words))
print(f'Từ dài (>3): {long_words}')
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Sử Dụng reduce()

Tạo file `day_13_reduce.py`:

```python
from functools import reduce

numbers = [1, 2, 3, 4, 5]

# Tính tổng
total = reduce(lambda a, b: a + b, numbers)
print(f'Tổng: {total}')

# Tính tích
product = reduce(lambda a, b: a * b, numbers)
print(f'Tích: {product}')

# Tìm min/max
maximum = reduce(lambda a, b: a if a > b else b, numbers)
print(f'Lớn nhất: {maximum}')

# Nối chuỗi
words = ['Python', 'is', 'awesome']
sentence = reduce(lambda a, b: f'{a} {b}', words)
print(f'Câu: {sentence}')
```

---

### Bài 2.2: Kết Hợp map, filter, reduce

```python
from functools import reduce

# Kết hợp nhiều hàm HOF
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Đề bài: Tính tổng bình phương của các số chẵn
# B1: Lọc số chẵn
evens = filter(lambda x: x % 2 == 0, numbers)

# B2: Bình phương
squares = map(lambda x: x ** 2, evens)

# B3: Tính tổng
result = reduce(lambda a, b: a + b, squares)

print(f"Danh sách: {numbers}")
print(f"Tổng bình phương các số chẵn: {result}")

# Viết gọn trong 1 dòng:
result_short = reduce(lambda a, b: a + b, map(lambda x: x ** 2, filter(lambda x: x % 2 == 0, numbers)))
print(f"Viết gọn: {result_short}")
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Phân Tích Dữ Liệu

Tạo file `day_13_analysis.py`:

```python
# Phân tích dữ liệu bằng HOF
from functools import reduce

# Dữ liệu
orders = [
    {'id': 1, 'item': 'Laptop', 'price': 1500, 'qty': 2},
    {'id': 2, 'item': 'Mouse', 'price': 50, 'qty': 5},
    {'id': 3, 'item': 'Keyboard', 'price': 80, 'qty': 1},
    {'id': 4, 'item': 'Monitor', 'price': 300, 'qty': 2}
]

print("=== PHÂN TÍCH ĐƠN HÀNG ===\n")

# 1. Tính tổng giá trị mỗi đơn hàng (map)
order_totals = list(map(lambda order: {'id': order['id'], 'total': order['price'] * order['qty']}, orders))
print("Tổng từng đơn hàng:")
for order in order_totals:
    print(f"  Đơn {order['id']}: ${order['total']}")

# 2. Lọc đơn hàng lớn (> $500) (filter)
big_orders = list(filter(lambda order: order['total'] > 500, order_totals))
print("\nĐơn hàng lớn (>$500):")
print(f"  {[o['id'] for o in big_orders]}")

# 3. Tính tổng doanh thu (reduce)
total_revenue = reduce(lambda a, b: a + b['total'], order_totals, 0)
print(f"\nTổng doanh thu: ${total_revenue}")
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Hiểu hàm Lambda
- [ ] Sử dụng map()
- [ ] Sử dụng filter()
- [ ] Sử dụng reduce()
- [ ] Kết hợp map, filter, reduce
- [ ] Hoàn thành bài nâng cao
- [ ] Hoàn thành phân tích dữ liệu

---

## 💡 Mẹo Quan Trọng

**1. Cú pháp HOF:**
```python
map(func, iterable)
filter(func_return_bool, iterable)
reduce(func_two_args, iterable)
```

**2. List Comprehension vs map/filter:**
Pythonic way thường dùng list comprehension hơn map/filter:
```python
# map: 
list(map(lambda x: x**2, nums))
# tương đương list comp:
[x**2 for x in nums]

# filter:
list(filter(lambda x: x>0, nums))
# tương đương list comp:
[x for x in nums if x>0]
```
