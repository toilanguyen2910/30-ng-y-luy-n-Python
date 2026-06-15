# 💻 Bài Tập Ngày 16

## Bài 1: Ngày Giờ Hiện Tại

```python
from datetime import datetime

now = datetime.now()
print(f'Ngày: {now.strftime("%d/%m/%Y")}')
print(f'Giờ: {now.strftime("%H:%M:%S")}')
print(f'Thứ: {now.strftime("%A")}')
```

## Bài 2: Tính Tuổi

```python
from datetime import date

def calculate_age(birth_date):
    today = date.today()
    age = today.year - birth_date.year
    if (today.month, today.day) < (birth_date.month, birth_date.day):
        age -= 1
    return age

birth = date(2007, 10, 29)
print(f'Tuổi: {calculate_age(birth)}')
```

## Bài 3: Đếm Ngày

```python
from datetime import date

start = date(2026, 1, 1)
end = date(2026, 12, 31)
days_left = (end - date.today()).days
print(f'Ngày còn lại trong năm: {days_left}')
```
