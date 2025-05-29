```
git clone --filter=blob:none --no-checkout https://github.com/nguyenhoai0910/k8s.git && cd k8s && git sparse-checkout init --cone
git sparse-checkout set
git checkout main
```
# Giả sử bạn muốn tải thư mục src trong repo myproject
### 1. Clone repo mà không lấy toàn bộ dữ liệu
    --no-checkout: Không tải toàn bộ nội dung, chỉ tải metadata của repo.
```
git clone --filter=blob:none --no-checkout https://github.com/user/myproject.git
cd myproject
```

### 2. Kích hoạt chế độ Sparse Checkout & đánh dấu thư mục
    --cone: Kích hoạt chế độ lọc file theo thư mục (tốt hơn cách cũ).
```
git sparse-checkout init --cone
```
```
git sparse-checkout set src
git sparse-checkout set src docs config                 # tải nhiều thư mục, chỉ cần cách nhau bằng dấu cách
```
### 3. Checkout branch chính để lấy dữ liệu
```
git checkout main  # hoặc branch cần thiết, ví dụ: git checkout develop
```
