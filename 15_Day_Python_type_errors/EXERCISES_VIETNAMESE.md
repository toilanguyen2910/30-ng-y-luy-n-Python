# 💻 Bài Tập Ngày 14

## Bài 1: Try/Except Cơ Bản

### Bài 1.1: Bắt Lỗi Nhập Liệu

```python
# Nhập số an toàn
while True:
    try:
        age = int(input('Nhập tuổi: '))
        break
    except ValueError:
        print('Không phải số! Nhập lại.')

print(f'Tuổi: {age}')
```

### Bài 1.2: Chia An Toàn

```python
def safe_divide(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        return 'Lỗi: Chia cho 0!'
    except TypeError:
        return 'Lỗi: Sai kiểu dữ liệu!'
    else:
        return result

print(safe_divide(10, 2))   # 5.0
print(safe_divide(10, 0))   # Lỗi: Chia cho 0!
```

---

## Bài 2: Try/Except/Finally

### Bài 2.1: Xử Lý File An Toàn

```python
def read_file(filename):
    try:
        f = open(filename, 'r')
        content = f.read()
    except FileNotFoundError:
        return 'Không tìm thấy file!'
    except PermissionError:
        return 'Không có quyền đọc!'
    else:
        return content
    finally:
        print('Hoàn tất kiểm tra file')

print(read_file('test.txt'))
```

---

## Bài 3: Thách Thức

### Bài 3.1: Máy Tính An Toàn

```python
def safe_calc():
    try:
        num1 = float(input('Số 1: '))
        op = input('Phép toán (+,-,*,/): ')
        num2 = float(input('Số 2: '))

        if op == '+': result = num1 + num2
        elif op == '-': result = num1 - num2
        elif op == '*': result = num1 * num2
        elif op == '/':
            if num2 == 0:
                raise ZeroDivisionError('Chia cho 0')
            result = num1 / num2
        else:
            raise ValueError('Phép toán không hợp lệ')

    except ValueError as e:
        print(f'Lỗi nhập liệu: {e}')
    except ZeroDivisionError as e:
        print(f'Lỗi tính toán: {e}')
    except Exception as e:
        print(f'Lỗi không xác định: {e}')
    else:
        print(f'Kết quả: {result}')
    finally:
        print('--- Kết thúc ---')

safe_calc()
```

---

## 💡 Mẹo

- Luôn dùng `try/except` khi nhập dữ liệu
- Dùng `else` cho code chỉ chạy khi KHÔNG có lỗi
- Dùng `finally` cho cleanup (đóng file, giải phóng resource)
- Tránh dùng bare `except:` → bắt quá nhiều lỗi
