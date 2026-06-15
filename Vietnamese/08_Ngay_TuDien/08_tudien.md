# 📘 Ngày 7 - Từ Điển (Dictionary)

## 🎯 Mục Tiêu Ngày 7

- Hiểu từ điển là gì
- Tạo và truy cập từ điển
- Sử dụng các phương thức từ điển
- Lặp qua từ điển
- Lồng từ điển

---

## 🔑 Từ Điển (Dictionary) Là Gì?

**Từ điển** là tập hợp các cặp **key-value** (khóa-giá trị) được bao quanh bởi dấu ngoặc nhọn `{ }`.

### Tạo Từ Điển

```python
# Từ điển rỗng
empty_dict = {}

# Từ điển cơ bản
person = {
    'name': 'Nguyễn Văn A',
    'age': 20,
    'city': 'Hà Nội'
}

# Từ điển hỗn hợp
data = {
    'id': 1,
    'name': 'Nam',
    'scores': [8.5, 9.0, 7.5],
    'is_active': True
}

# Dùng dict()
d = dict(name='Nam', age=20)
print(d)  # {'name': 'Nam', 'age': 20}
```

---

## 🔍 Truy Cập & Sửa Đổi

### Truy Cập Giá Trị

```python
person = {'name': 'Nguyễn', 'age': 20, 'city': 'Hà Nội'}

# Truy cập với []
print(person['name'])      # Nguyễn

# Truy cập với get() - an toàn
print(person.get('age'))   # 20
print(person.get('country', 'N/A'))  # N/A (nếu không có)
```

### Thêm & Sửa Phần Tử

```python
person = {'name': 'Nguyễn', 'age': 20}

# Thêm phần tử mới
person['city'] = 'Hà Nội'

# Sửa phần tử
person['age'] = 21

print(person)
# {'name': 'Nguyễn', 'age': 21, 'city': 'Hà Nội'}
```

### Xóa Phần Tử

```python
person = {'name': 'Nguyễn', 'age': 20, 'city': 'Hà Nội'}

# del
del person['city']

# pop()
age = person.pop('age')
print(age)  # 20

# clear()
person.clear()
print(person)  # {}
```

---

## 📋 Các Phương Thức Từ Điển

### keys() - Lấy Tất Cả Khóa

```python
person = {'name': 'Nguyễn', 'age': 20, 'city': 'Hà Nội'}

print(person.keys())    # dict_keys(['name', 'age', 'city'])
```

### values() - Lấy Tất Cả Giá Trị

```python
print(person.values())  # dict_values(['Nguyễn', 20, 'Hà Nội'])
```

### items() - Lấy Cặp Key-Value

```python
print(person.items())
# dict_items([('name', 'Nguyễn'), ('age', 20), ('city', 'Hà Nội')])
```

### in - Kiểm Tra Khóa

```python
print('name' in person)        # True
print('country' in person)     # False
```

### len() - Số Phần Tử

```python
print(len(person))    # 3
```

### update() - Cập Nhật

```python
person = {'name': 'Nguyễn', 'age': 20}
person.update({'age': 21, 'city': 'Hà Nội'})
print(person)
# {'name': 'Nguyễn', 'age': 21, 'city': 'Hà Nội'}
```

---

## 🔄 Lặp Qua Từ Điển

### Lặp Qua Khóa

```python
person = {'name': 'Nguyễn', 'age': 20, 'city': 'Hà Nội'}

for key in person:
    print(key)
# name
# age
# city

# Hoặc dùng .keys()
for key in person.keys():
    print(key)
```

### Lặp Qua Giá Trị

```python
for value in person.values():
    print(value)
# Nguyễn
# 20
# Hà Nội
```

### Lặp Qua Cặp Key-Value

```python
for key, value in person.items():
    print(f'{key}: {value}')
# name: Nguyễn
# age: 20
# city: Hà Nội
```

---

## 🎯 Từ Điển Lồng Nhau

```python
company = {
    'name': 'Tech Company',
    'employees': [
        {'id': 1, 'name': 'Nguyễn', 'position': 'Dev'},
        {'id': 2, 'name': 'Trần', 'position': 'Designer'}
    ],
    'address': {
        'street': 'Lê Lợi',
        'city': 'Hà Nội'
    }
}

# Truy cập
print(company['name'])                      # Tech Company
print(company['address']['city'])           # Hà Nội
print(company['employees'][0]['name'])      # Nguyễn
```

---

## 💻 Ví Dụ Thực Tế

### Ví Dụ 1: Hồ Sơ Sinh Viên

```python
# Hồ sơ sinh viên
student = {
    'id': '20200001',
    'name': 'Nguyễn Văn A',
    'birth_year': 2002,
    'major': 'CNTT',
    'gpa': 3.8,
    'courses': ['Python', 'JavaScript', 'Database']
}

# In thông tin
print('=== HỒ SƠ SINH VIÊN ===')
for key, value in student.items():
    print(f'{key}: {value}')
```

### Ví Dụ 2: Đếm Tần Suất

```python
# Đếm tần suất từ
text = "python java python javascript python java"
words = text.split()

# Tạo từ điển đếm
count = {}
for word in words:
    if word in count:
        count[word] += 1
    else:
        count[word] = 1

# In kết quả
print('Tần suất từ:')
for word, freq in count.items():
    print(f'{word}: {freq}')
```

---

## 📊 So Sánh List, Tuple, Set, Dict

| Đặc Điểm | List | Tuple | Set | Dict |
|---------|------|-------|-----|------|
| Tạo | `[]` | `()` | `{}` | `{}` |
| Thay đổi | ✓ | ✗ | ✓ | ✓ |
| Thứ tự | ✓ | ✓ | ✗ | ✓ |
| Trùng lặp | ✓ | ✓ | ✗ | ✗ |
| Key-Value | ✗ | ✗ | ✗ | ✓ |

---

## 🚀 Tiếp Theo - Ngày 8

Ngày 8 bạn sẽ học:
- Câu lệnh if/elif/else
- Điều kiện boolean
- Lồng điều kiện
