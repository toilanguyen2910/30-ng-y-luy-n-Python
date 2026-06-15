# 💻 Bài Tập Ngày 17

## Bài 1: Nhập Liệu An Toàn

```python
def input_int(prompt):
    while True:
        try:
            return int(input(prompt))
        except ValueError:
            print('Nhập số nguyên!')

age = input_int('Tuổi: ')
print(f'Tuổi: {age}')
```

## Bài 2: Đọc File An Toàn

```python
def read_file_safe(filename):
    try:
        with open(filename, 'r') as f:
            return f.read()
    except FileNotFoundError:
        return f'Không tìm thấy: {filename}'
    except PermissionError:
        return f'Không có quyền đọc: {filename}'
    except Exception as e:
        return f'Lỗi: {e}'

print(read_file_safe('test.txt'))
```

## Bài 3: Exception Tùy Chỉnh

```python
class ScoreError(Exception):
    pass

def validate_score(score):
    if score < 0 or score > 10:
        raise ScoreError(f'Điểm {score} không hợp lệ (0-10)')
    return score

try:
    validate_score(11)
except ScoreError as e:
    print(e)
```
