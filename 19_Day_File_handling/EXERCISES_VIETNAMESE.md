# 💻 Bài Tập Ngày 15

## Bài 1: Đọc File

```python
# Tạo file test
with open('students.txt', 'w') as f:
    f.write('Nguyễn,8.5\n')
    f.write('Trần,7.0\n')
    f.write('Phạm,9.2\n')

# Đọc file
with open('students.txt', 'r') as f:
    for line in f:
        name, score = line.strip().split(',')
        print(f'{name}: {score}')
```

## Bài 2: Ghi File

```python
# Tạo file với danh sách
numbers = list(range(1, 11))
with open('numbers.txt', 'w') as f:
    for num in numbers:
        f.write(f'{num}\n')
```

## Bài 3: JSON

```python
import json

students = [
    {'name': 'Nam', 'score': 8.5},
    {'name': 'An', 'score': 7.0}
]

# Ghi
with open('students.json', 'w') as f:
    json.dump(students, f, ensure_ascii=False, indent=2)

# Đọc
with open('students.json', 'r') as f:
    data = json.load(f)
    for s in data:
        print(f"{s['name']}: {s['score']}")
```
