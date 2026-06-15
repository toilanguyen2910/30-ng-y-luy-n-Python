# 📘 Ngày 26 - MongoDB

```python
from pymongo import MongoClient

client = MongoClient('mongodb://localhost:27017/')
db = client['mydb']
collection = db['students']

# Thêm
collection.insert_one({'name': 'Nam', 'age': 20})

# Đọc
students = collection.find()
for s in students:
    print(s)

# Cập nhật
collection.update_one({'name': 'Nam'}, {'$set': {'age': 21}})
```
