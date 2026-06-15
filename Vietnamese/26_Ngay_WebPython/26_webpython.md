# 📘 Ngày 25 - Web với Python (Flask)

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return 'Xin chào Flask!'

@app.route('/user/<name>')
def user(name):
    return f'Xin chào {name}!'

if __name__ == '__main__':
    app.run(debug=True)
```

Chạy: `python app.py` → truy cập `http://localhost:5000`
