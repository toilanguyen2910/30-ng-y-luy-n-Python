# 📘 Ngày 15 - Xử Lý File (File Handling)

## Mục Tiêu
- Đọc và ghi file text
- with statement
- Các mode: r, w, a, r+

## File Mode

| Mode | Ý Nghĩa |
|------|---------|
| `r` | Đọc (mặc định) |
| `w` | Ghi (ghi đè) |
| `a` | Thêm (append) |
| `r+` | Đọc + Ghi |

## Đọc File

```python
# Cách 1: with statement (khuyến khích)
with open('data.txt', 'r') as f:
    content = f.read()
    print(content)

# Đọc từng dòng
with open('data.txt', 'r') as f:
    for line in f:
        print(line.strip())
```

## Ghi File

```python
# Ghi mới (ghi đè)
with open('output.txt', 'w') as f:
    f.write('Xin chào\n')
    f.write('Hôm nay là thứ 2\n')

# Thêm vào cuối file
with open('output.txt', 'a') as f:
    f.write('Dòng mới\n')
```

## Đọc Ghi JSON

```python
import json

data = {'name': 'Nam', 'age': 20}

# Ghi JSON
with open('data.json', 'w') as f:
    json.dump(data, f, ensure_ascii=False, indent=2)

# Đọc JSON
with open('data.json', 'r') as f:
    loaded = json.load(f)
    print(loaded)
```
