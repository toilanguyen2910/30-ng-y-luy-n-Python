# 📘 Ngày 17 - Xử Lý Ngoại Lệ (Exception Handling)

## Mục Tiêu
- Try/Except/Else/Finally
- Bắt nhiều loại lỗi
- Tạo exception tùy chỉnh
- Logging lỗi

## try/except

```python
try:
    num = int(input('Nhập số: '))
    result = 10 / num
except ValueError:
    print('Không phải số!')
except ZeroDivisionError:
    print('Chia cho 0!')
except Exception as e:
    print(f'Lỗi khác: {e}')
else:
    print(f'Kết quả: {result}')
finally:
    print('Hoàn tất')
```

## Tạo Exception Tùy Chỉnh

```python
class AgeError(Exception):
    def __init__(self, age, message='Tuổi không hợp lệ'):
        self.age = age
        self.message = message
        super().__init__(self.message)

def check_age(age):
    if age < 0:
        raise AgeError(age)
    if age > 150:
        raise AgeError(age, 'Tuổi quá lớn')
    return True

try:
    check_age(200)
except AgeError as e:
    print(f'{e.message}: {e.age}')
```
