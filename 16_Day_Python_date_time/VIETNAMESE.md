# 📘 Ngày 16 - Ngày Giờ Python (datetime)

## Mục Tiêu
- Sử dụng module datetime
- Định dạng ngày giờ (strftime/strptime)
- Tính khoảng cách ngày

## Module datetime

```python
from datetime import datetime, timedelta, date

# Ngày giờ hiện tại
now = datetime.now()
print(now)  # 2026-06-15 10:30:00.123456

# Tạo đối tượng ngày
d = date(2026, 6, 15)
print(d)  # 2026-06-15

# Các thuộc tính
print(now.year)   # 2026
print(now.month)  # 6
print(now.day)    # 15
print(now.hour)   # 10
```

## strftime - Định Dạng Ngày Giờ

```python
now = datetime.now()
print(now.strftime('%d/%m/%Y'))       # 15/06/2026
print(now.strftime('%Y-%m-%d'))       # 2026-06-15
print(now.strftime('%H:%M:%S'))       # 10:30:00
print(now.strftime('%d/%m/%Y %H:%M')) # 15/06/2026 10:30
```

## strptime - Chuyển Chuỗi Thành DateTime

```python
date_str = '15/06/2026'
d = datetime.strptime(date_str, '%d/%m/%Y')
print(d)  # 2026-06-15 00:00:00
```

## timedelta - Tính Khoảng Cách

```python
from datetime import timedelta

today = date.today()
future = today + timedelta(days=30)
past = today - timedelta(days=7)

print(f'Hôm nay: {today}')
print(f'30 ngày nữa: {future}')
print(f'7 ngày trước: {past}')
print(f'Sai số: {(future - today).days} ngày')
```
