# 📘 Ngày 21 - Web Scraping

Web scraping là kỹ thuật lấy dữ liệu từ trang web.

```python
import requests
from bs4 import BeautifulSoup

url = 'https://example.com'
response = requests.get(url)
soup = BeautifulSoup(response.content, 'html.parser')

# Tìm element
titles = soup.find_all('h1')
for title in titles:
    print(title.text)

# Tìm theo class
divs = soup.find_all('div', class_='content')
```
