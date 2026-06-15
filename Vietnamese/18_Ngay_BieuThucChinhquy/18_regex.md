# 📘 Ngày 18 - Biểu Thức Chính Quy (Regular Expression)

Biểu thức chính quy dùng để tìm kiếm, so sánh chuỗi theo pattern.

```python
import re

# Tìm pattern
pattern = r'\d+'  # Tìm số
text = 'Năm 2026 là một năm tốt'
matches = re.findall(pattern, text)
print(matches)  # ['2026']

# So sánh email đơn giản
email_pattern = r'^[\w.-]+@[\w.-]+\.\w+$'
print(re.match(email_pattern, 'user@gmail.com'))  # Match

# Thay thế
text = 'Tôi yêu Python'
new_text = re.sub(r'Python', 'JavaScript', text)
print(new_text)  # Tôi yêu JavaScript
```

## Pattern Phổ Biến

| Pattern | Ý Nghĩa |
|---------|---------|
| `\d` | Chữ số |
| `\w` | Chữ/số/gạch dưới |
| `\s` | Khoảng trắng |
| `+` | 1 hay nhiều |
| `*` | 0 hay nhiều |
| `?` | 0 hay 1 |
| `.` | Bất kỳ ký tự |
| `^` | Đầu chuỗi |
| `$` | Cuối chuỗi |
