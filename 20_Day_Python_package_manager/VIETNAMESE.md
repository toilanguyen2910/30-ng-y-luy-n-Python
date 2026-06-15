# 📘 Ngày 19 - Package Manager (pip)

pip là công cụ cài đặt thư viện Python.

```bash
# Cài đặt thư viện
pip install requests

# Cài version cụ thể
pip install numpy==1.21.0

# Cài nhiều thư viện
pip install requests pandas matplotlib

# Xóa thư viện
pip uninstall requests

# Liệt kê thư viện đã cài
pip list

# Lưu dependencies
pip freeze > requirements.txt

# Cài từ requirements
pip install -r requirements.txt
```

## Các Thư Viện Phổ Biến

- **requests** - HTTP library
- **numpy** - Tính toán số học
- **pandas** - Phân tích dữ liệu
- **matplotlib** - Vẽ biểu đồ
- **flask** - Web framework
- **django** - Web framework lớn
