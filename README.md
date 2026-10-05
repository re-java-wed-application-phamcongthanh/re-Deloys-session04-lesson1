# Báo Cáo Bài 1: Khởi tạo Local Repository và Cấu hình danh tính

## 1. Mục tiêu
- Khởi tạo thành công một Git repository trống tại thư mục làm việc cục bộ (`session4/bai1`).
- Thiết lập thông tin danh tính tác giả (tên và email) ở cấp độ cục bộ (`--local`).
- Tạo tệp tin mới (`index.html`, `README.md`), đưa vào vùng chuẩn bị (Staging Area) và tiến hành commit đầu tiên.
- Phân tích trạng thái thư mục làm việc và lịch sử commit thông qua lệnh `git log`.

---

## 2. Các bước thực hiện

### Bước 1: Khởi tạo Git Local Repository
Tại thư mục làm việc của dự án, khởi tạo một repository mới:
```bash
git init
```
*Kết quả:* Tạo thư mục ẩn `.git` chứa toàn bộ dữ liệu quản lý phiên bản của repository.

### Bước 2: Cấu hình danh tính tác giả ở phạm vi Cục bộ (Local)
Sử dụng cờ `--local` để đảm bảo thông tin danh tính chỉ áp dụng cho dự án này, không ảnh hưởng đến cấu hình `--global`:
```bash
git config --local user.name "phamcongthanhvn2k6"
git config --local user.email "phamcongt56@gmail.com"
```

### Bước 3: Đưa tệp tin vào Staging Area và Tạo Commit đầu tiên
Kiểm tra trạng thái các tệp tin chưa được theo dõi:
```bash
git status
```
Đưa toàn bộ tệp tin vào vùng chuẩn bị (Staging Area):
```bash
git add .
```
Tiến hành commit với thông điệp rõ nghĩa:
```bash
git commit -m "Initial commit: Khởi tạo Local Repository và Cấu hình danh tính"
```

---

## 3. Kết quả Kiểm tra (Verification)

### Kiểm tra cấu hình Email cục bộ:
```bash
git config --local user.email
```
**Output:**
```text
phamcongt56@gmail.com
```

### Kiểm tra cấu hình Tên cục bộ:
```bash
git config --local user.name
```
**Output:**
```text
phamcongthanhvn2k6
```

### Xem toàn bộ cấu hình Local:
```bash
git config --local --list
```
**Output:**
```text
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
user.name=phamcongthanhvn2k6
user.email=phamcongt56@gmail.com
```

### Xem lịch sử Commit (`git log --oneline`):
```bash
git log --oneline
```
**Output:**
```text
7c7d48b Initial commit: Khởi tạo Local Repository và Cấu hình danh tính
```

---

## 4. Kết luận
- Dự án đã được khởi tạo thành công dưới sự quản lý của Git.
- Thông tin danh tính tác giả đã được thiết lập chuẩn xác ở cấp độ `--local`.
- Lịch sử commit đã ghi nhận commit đầu tiên của dự án.
