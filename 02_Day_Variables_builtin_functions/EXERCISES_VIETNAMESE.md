# 💻 Bài Tập Ngày 2

## Bài 1: Kiến Thức Cơ Bản

### Bài 1.1: Tạo Biến

Tạo file `day_2_basic.py`:

```python
# Ngày 2 - Biến và Hàm Built-in

# Tạo biến với các kiểu dữ liệu khác nhau
first_name = 'Nguyễn'
last_name = 'Văn A'
age = 20
height = 1.75
is_student = True
skills = ['Python', 'JavaScript', 'HTML']

# In các biến
print(first_name)
print(last_name)
print(age)
print(height)
print(is_student)
print(skills)
```

**Chạy:**
```bash
python3 day_2_basic.py
```

---

### Bài 1.2: Gán Nhiều Biến

```python
# Gán nhiều biến cùng lúc
name, age, city = 'Nguyễn', 20, 'Hà Nội'
print(f'{name}, {age} tuổi, sống ở {city}')

# Gán cùng một giá trị
x = y = z = 100
print(x, y, z)

# Hoán đổi
a = 5
b = 10
a, b = b, a
print(f'a = {a}, b = {b}')
```

---

### Bài 1.3: input() và Chuyển Đổi Kiểu

```python
# Nhập tên
name = input('Nhập tên: ')
print(f'Xin chào {name}!')

# Nhập tuổi (phải chuyển thành int)
age = int(input('Nhập tuổi: '))
print(f'Bạn {age} tuổi')

# Nhập chiều cao (phải chuyển thành float)
height = float(input('Nhập chiều cao (m): '))
print(f'Chiều cao: {height}m')
```

---

## Bài 2: Kiến Thức Nâng Cao

### Bài 2.1: Sử Dụng Hàm Built-in

Tạo file `day_2_builtin.py`:

```python
# Các hàm built-in quan trọng

# len() - độ dài
print(len('Python'))          # 6
print(len([1, 2, 3, 4, 5]))   # 5

# max() và min()
numbers = [10, 5, 20, 15, 3]
print(f'Số lớn nhất: {max(numbers)}')    # 20
print(f'Số nhỏ nhất: {min(numbers)}')    # 3

# sum() - tổng
total = sum(numbers)
print(f'Tổng: {total}')                  # 53

# abs() - giá trị tuyệt đối
print(abs(-10))    # 10

# round() - làm tròn
pi = 3.14159
print(round(pi))        # 3
print(round(pi, 2))     # 3.14

# sorted() - sắp xếp
print(sorted(numbers))  # [3, 5, 10, 15, 20]
```

---

### Bài 2.2: Chương Trình Tính Chỉ Số BMI

```python
# Tính chỉ số BMI (Body Mass Index)

# Nhập dữ liệu
name = input('Nhập tên: ')
weight = float(input('Nhập cân nặng (kg): '))
height = float(input('Nhập chiều cao (m): '))

# Tính BMI
bmi = weight / (height ** 2)

# In kết quả
print(f'\nThông tin của {name}:')
print(f'Cân nặng: {weight} kg')
print(f'Chiều cao: {height} m')
print(f'Chỉ số BMI: {bmi:.2f}')

# Đánh giá
if bmi < 18.5:
    print('Tình trạng: Gầy')
elif bmi < 25:
    print('Tình trạng: Bình thường')
elif bmi < 30:
    print('Tình trạng: Thừa cân')
else:
    print('Tình trạng: Béo phì')
```

---

## Bài 3: Thách Thức Cao Cấp

### Bài 3.1: Chương Trình Hồ Sơ Sinh Viên

Tạo file `day_2_profile.py`:

```python
# Hồ sơ sinh viên

print('=== TẠO HỒ SƠ SINH VIÊN ===\n')

# Nhập thông tin cá nhân
first_name = input('Nhập họ: ')
last_name = input('Nhập tên: ')
birth_year = int(input('Nhập năm sinh: '))
major = input('Nhập ngành học: ')

# Tính tuổi
current_year = 2026
age = current_year - birth_year

# Nhập kỹ năng (nhập cách nhau bằng dấu phẩy)
skills_input = input('Nhập kỹ năng (cách nhau bằng dấu phẩy): ')
skills = [skill.strip() for skill in skills_input.split(',')]

# Số lượng kỹ năng
num_skills = len(skills)

# In hồ sơ
print('\n=== HỒ SƠ SINH VIÊN ===')
print(f'Họ tên: {first_name} {last_name}')
print(f'Tuổi: {age}')
print(f'Ngành học: {major}')
print(f'Số kỹ năng: {num_skills}')
print(f'Kỹ năng: {", ".join(skills)}')
```

---

### Bài 3.2: Tính Lương

```python
# Tính lương tháng

print('=== TÍNH LƯƠNG THÁNG ===\n')

# Nhập dữ liệu
name = input('Nhập tên nhân viên: ')
base_salary = float(input('Nhập lương cơ bản (triệu VND): '))
tax_rate = float(input('Nhập tỷ lệ thuế (%): '))
bonus = float(input('Nhập thưởng (triệu VND): '))

# Tính toán
total_income = base_salary + bonus
tax = total_income * tax_rate / 100
net_salary = total_income - tax

# In kết quả
print('\n=== BẢNG LƯƠNG ===')
print(f'Nhân viên: {name}')
print(f'Lương cơ bản: {base_salary:.2f} triệu')
print(f'Thưởng: {bonus:.2f} triệu')
print(f'Tổng thu nhập: {total_income:.2f} triệu')
print(f'Thuế ({tax_rate}%): {tax:.2f} triệu')
print(f'Lương ròng: {net_salary:.2f} triệu')
```

---

## 📋 Danh Sách Kiểm Tra

- [ ] Hiểu biến là gì
- [ ] Đặt tên biến đúng quy tắc
- [ ] Sử dụng input() nhập dữ liệu
- [ ] Chuyển đổi kiểu dữ liệu (int, float, str)
- [ ] Sử dụng được hàm len(), max(), min(), sum()
- [ ] Sử dụng được hàm round(), abs(), sorted()
- [ ] Hoàn thành bài tập cơ bản
- [ ] Hoàn thành bài tập nâng cao
- [ ] Hoàn thành thách thức cao cấp

---

## 💡 Mẹo Quan Trọng

**1. input() luôn trả về chuỗi:**
```python
age = input('Tuổi: ')  # '20' (chuỗi)
age = int(age)         # 20 (số)
```

**2. F-string cho format chuỗi:**
```python
name = 'Nguyễn'
print(f'Xin chào {name}')  # Xin chào Nguyễn
```

**3. Chuyển đổi kiểu:**
```python
int('10')      # 10
float('3.14')  # 3.14
str(42)        # '42'
```

**4. Tách chuỗi:**
```python
text = 'Python,Java,C++'
languages = text.split(',')  # ['Python', 'Java', 'C++']
```

---

## 🚀 Chuẩn Bị Cho Ngày 3

Ngày 3 bạn sẽ học:
- Toán tử số học
- Toán tử so sánh
- Toán tử logic
- Ưu tiên toán tử
