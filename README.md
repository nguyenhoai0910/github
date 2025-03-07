Giả sử bạn muốn tải thư mục src trong repo myproject
```
git clone --no-checkout https://github.com/user/myproject.git
cd myproject
```
    # --no-checkout: Không tải toàn bộ nội dung, chỉ tải metadata của repo.

2. Kích hoạt chế độ Sparse Checkout
```
git sparse-checkout init --cone
```
    # --cone: Kích hoạt chế độ lọc file theo thư mục (tốt hơn cách cũ).

```
git sparse-checkout set src

git sparse-checkout set src docs config                 # tải nhiều thư mục, chỉ cần cách nhau bằng dấu cách
```
```
git checkout main  # hoặc branch cần thiết, ví dụ: git checkout develop
```
