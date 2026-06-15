# 📘 Ngày 28 - Xây Dựng API (Building API)

Xây dựng REST API bằng Flask:

```python
from flask import Flask, request, jsonify

app = Flask(__name__)
students = []

@app.route('/api/students', methods=['GET'])
def get_students():
    return jsonify(students)

@app.route('/api/students', methods=['POST'])
def add_student():
    data = request.json
    students.append(data)
    return jsonify({'status': 'OK'}), 201

@app.route('/api/students/<int:id>', methods=['DELETE'])
def delete_student(id):
    if 0 <= id < len(students):
        students.pop(id)
        return jsonify({'status': 'Deleted'}), 200
    return jsonify({'error': 'Not found'}), 404

if __name__ == '__main__':
    app.run(debug=True, port=5000)
```

## Kiểm Tra API

```bash
# Lấy danh sách
curl http://localhost:5000/api/students

# Thêm sinh viên
curl -X POST http://localhost:5000/api/students \\
  -H "Content-Type: application/json" \\
  -d '{"name":"Nam", "score":8.5}'

# Xóa sinh viên
curl -X DELETE http://localhost:5000/api/students/0
```
