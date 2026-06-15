# 📘 Ngày 24 - Pandas

```python
import pandas as pd

# Tạo DataFrame
data = {'Name': ['Nam', 'An'], 'Age': [20, 21]}
df = pd.DataFrame(data)
print(df)

# Đọc CSV
df = pd.read_csv('data.csv')
print(df.head())

# Lựa chọn cột
print(df['Name'])

# Filter
print(df[df['Age'] > 20])
```
