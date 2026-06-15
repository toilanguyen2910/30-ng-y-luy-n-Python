# 💻 Bài Tập Ngày 19

```bash
# Cài requests
pip install requests

# Python
import requests
response = requests.get('https://api.github.com')
print(response.status_code)  # 200
data = response.json()
```
