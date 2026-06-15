# 💻 Bài Tập Ngày 20

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

class Employee(Person):
    def __init__(self, name, age, salary):
        super().__init__(name, age)
        self.salary = salary
    
    def info(self):
        return f'{self.name}, {self.age}, {self.salary}K'

emp = Employee('Nam', 30, 15)
print(emp.info())
```
