# 📘 Ngày 27 - API

REST API là cách để các ứng dụng giao tiếp với nhau qua HTTP.

```python
import requests
import json

# GET request
response = requests.get('https://api.github.com/users/github')
user_data = response.json()
print(user_data['name'])

# POST request
data = {'name': 'Nam', 'age': 20}
response = requests.post('https://example.com/api/users', json=data)
print(response.status_code)
```

## HTTP Status Codes

- 200: OK
- 201: Created
- 400: Bad Request
- 404: Not Found
- 500: Server Error
