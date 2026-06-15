# 📘 Ngày 20 - Lớp và Đối Tượng (OOP)

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def info(self):
        return f'{self.name}, {self.age} tuổi'

s = Student('Nguyễn', 20)
print(s.info())  # Nguyễn, 20 tuổi

# Thừa kế
class GraduateStudent(Student):
    def __init__(self, name, age, gpa):
        super().__init__(name, age)
        self.gpa = gpa
    
    def info(self):
        return f'{super().info()}, GPA: {self.gpa}'

gs = GraduateStudent('Trần', 22, 3.8)
print(gs.info())
```
