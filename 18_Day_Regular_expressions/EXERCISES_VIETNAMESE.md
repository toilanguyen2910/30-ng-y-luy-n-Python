# 💻 Bài Tập Ngày 18

```python
import re

# Bài 1: Tìm số
text = 'Tôi có 2 cái bàn, 3 cái ghế, 5 quyển sách'
numbers = re.findall(r'\d+', text)
print(numbers)  # ['2', '3', '5']

# Bài 2: Kiểm tra email
email = 'user@gmail.com'
if re.match(r'^[\w.-]+@[\w.-]+\.\w+$', email):
    print('Email hợp lệ')

# Bài 3: Thay thế
text = 'Ngày 15/06/2026 là ngày tốt'
new_text = re.sub(r'\d+', 'X', text)
print(new_text)  # Ngày X/X/X là ngày tốt
```
