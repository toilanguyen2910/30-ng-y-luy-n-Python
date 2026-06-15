# 💻 Bài Tập Ngày 7

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Tạo & Truy Cập Từ Điển

Tạo file `day_7_dict_basics.py`:

```python
# Ngày 7 - Từ Điển

# Tạo từ điển
person = {
    'name': 'Nguyễn Văn A',
    'age': 20,
    'city': 'Hà Nội',
    'job': 'Developer'
}

# Truy cập
print(person['name'])       # Nguyễn Văn A
print(person['age'])        # 20

# Truy cập an toàn
print(person.get('name'))   # Nguyễn Văn A
print(person.get('country', 'N/A'))  # N/A

# Độ dài
print(len(person))          # 4

# Kiểm tra khóa
print('name' in person)     # True
print('country' in person)  # False
```

---

### Bài 1.2: Thêm & Xóa Phần Tử

```python
# Thêm phần tử
person = {'name': 'Nguyễn', 'age': 20}
person['city'] = 'Hà Nội'
print(person)
# {'name': 'Nguyễn', 'age': 20, 'city': 'Hà Nội'}

# Sửa phần tử
person['age'] = 21
print(person)
# {'name': 'Nguyễn', 'age': 21, 'city': 'Hà Nội'}

# Xóa phần tử
del person['city']
print(person)
# {'name': 'Nguyễn', 'age': 21}

# pop()
age = person.pop('age')
print(f'Tuổi: {age}')       # Tuổi: 21
```

---

### Bài 1.3: Lặp Qua Từ Điển

```python
person = {'name': 'Nguyễn', 'age': 20, 'city': 'Hà Nội'}

# Lặp khóa
print('Khóa:')
for key in person:
    print(f'  {key}')

# Lặp giá trị
print('\nGiá trị:')
for value in person.values():
    print(f'  {value}')

# Lặp cặp
print('\nCặp:')
for key, value in person.items():
    print(f'  {key}: {value}')
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Quản Lý Hồ Sơ

Tạo file `day_7_dict_advanced.py`:

```python
# Quản lý hồ sơ sinh viên

print("=== HỒ SƠ SINH VIÊN ===\n")

# Tạo hồ sơ
student = {
    'id': '20200001',
    'name': 'Nguyễn Văn A',
    'birth_year': 2002,
    'major': 'Công Nghệ Thông Tin',
    'gpa': 3.8,
    'courses': ['Python', 'JavaScript', 'Database']
}

# In thông tin
print('Thông tin:')
for key, value in student.items():
    print(f'  {key}: {value}')

# Tính tuổi
current_year = 2026
age = current_year - student['birth_year']
print(f'\nTuổi: {age}')

# Số môn học
print(f'Số môn học: {len(student["courses"])}')
print(f'Các môn: {", ".join(student["courses"])}')
```

---

### Bài 2.2: Đếm Tần Suất

```python
# Đếm tần suất từ

text = input("Nhập chuỗi: ")
words = text.split()

# Đếm
word_count = {}
for word in words:
    if word in word_count:
        word_count[word] += 1
    else:
        word_count[word] = 1

# In kết quả
print('\nTần suất từ:')
for word, count in sorted(word_count.items()):
    print(f'  {word}: {count}')

# Từ xuất hiện nhiều nhất
most_common = max(word_count, key=word_count.get)
print(f'\nTừ xuất hiện nhiều nhất: {most_common} ({word_count[most_common]} lần)')
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Lồng Từ Điển

Tạo file `day_7_nested_dict.py`:

```python
# Từ điển lồng nhau - Công ty

company = {
    'name': 'Tech Company',
    'employees': [
        {
            'id': 1,
            'name': 'Nguyễn Văn A',
            'position': 'Developer',
            'salary': 15000000
        },
        {
            'id': 2,
            'name': 'Trần Thị B',
            'position': 'Designer',
            'salary': 12000000
        },
        {
            'id': 3,
            'name': 'Phạm Văn C',
            'position': 'Manager',
            'salary': 18000000
        }
    ],
    'address': {
        'street': 'Lê Lợi',
        'district': 'Hoàn Kiếm',
        'city': 'Hà Nội'
    }
}

# In thông tin
print(f"Công ty: {company['name']}")
print(f"Địa chỉ: {company['address']['street']}, {company['address']['district']}, {company['address']['city']}")

# In danh sách nhân viên
print("\nDanh sách nhân viên:")
total_salary = 0
for emp in company['employees']:
    print(f"  {emp['id']}. {emp['name']} - {emp['position']} - {emp['salary']:,} VND")
    total_salary += emp['salary']

# Thống kê
print(f"\nTổng nhân viên: {len(company['employees'])}")
print(f"Tổng lương: {total_salary:,} VND")
print(f"Lương trung bình: {total_salary // len(company['employees']):,} VND")
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Tạo từ điển
- [ ] Truy cập giá trị
- [ ] Thêm phần tử mới
- [ ] Sửa phần tử
- [ ] Xóa phần tử
- [ ] Sử dụng get()
- [ ] Lặp qua khóa
- [ ] Lặp qua giá trị
- [ ] Lặp qua cặp key-value
- [ ] Hoàn thành bài tập nâng cao

---

## 💡 Mẹo Quan Trọng

**1. Tạo từ điển:**
```python
d = {'key': 'value'}
d = dict(key='value')
```

**2. Truy cập an toàn:**
```python
d.get('key')           # None nếu không có
d.get('key', 'default')  # giá trị mặc định
```

**3. Lặp tốt nhất:**
```python
for key, value in d.items():
    print(key, value)
```
