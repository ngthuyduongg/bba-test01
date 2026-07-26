# Getting Started - Playwright Typescript

## Playwright là gì?

**Ưu điểm Playwright:**
- Cross browser
- Cross platform
- Tính năng "xịn sò"
- Report đầy đủ thông tin
- **Code gen**: thao tác trên trình duyệt để tự sinh ra code

---

## Tại sao chọn học Playwright TypeScript?

**Học Playwright vì:**
- Dễ cài đặt
- Cú pháp đơn giản, dễ học
- Framework đang trending, nhiều cơ hội việc làm

**Công ty dùng tool khác thì có nên học khóa này không? → Có! Vì:**
- Khóa học dạy về tư duy, hiểu bản chất
- Hiểu bản chất thì các tools tương tự nhau
- Mentor có kiến thức đa dạng các tools, có thể hỏi về tools của công ty, mentor sẽ hỗ trợ

---

## Cấu hình Git

Khai báo thông tin cá nhân và các thiết lập mặc định để sử dụng Git thuận tiện hơn. Trước khi làm việc với Git, cần một số cấu hình mặc định (chạy trong Git Bash):

- Config username (tên người dùng): `git config --global user.name "<Ho_Ten>"`
- Config email (địa chỉ email): `git config --global user.email "<email>"`
- Config branch mặc định: `git config --global init.defaultBranch main`

> Chỉ chạy một lần duy nhất trên máy, gần như không cần thay đổi cho từng project.

---

## Cài đặt VS Code

Cài đặt Playwright Extension giúp phát triển và chạy test Playwright thuận tiện hơn ngay trong VS Code, bao gồm:
- Chạy test trực tiếp từ editor
- Debug test
- Xem kết quả test
- Record Code (ghi lại thao tác trên trình duyệt để sinh code Playwright)
- Hỗ trợ gợi ý (IntelliSense) và điều hướng mã nguồn

Với Windows: đổi terminal mặc định thành Git Bash trong VS Code.

---

## Kết nối với GitHub

**Lệnh tạo SSH Keys** 
- `ssh-keygen -t rsa -b 4096 -C "<email>"` → nếu đã có key rồi thì dừng lại luôn
- `cat ~/.ssh/id_rsa.pub` → lấy nội dung SSH key
- Truy cập trang cài đặt SSH and GPG keys trên GitHub để thêm SSH key

---

## Cài đặt Playwright

## Cài đặt Playwright

1. Tạo thư mục chứa code
2. Mở thư mục 
3. Chạy `npm init playwright@latest`, Enter liên tục đến khi hiện "Happy hacking"
4. Vào VS Code 
5. Khởi tạo repo local: `git init`
6. Mở file test trong thư mục tests → chạy thử test

---

## Đưa code lên GitHub

**Khởi tạo (chỉ làm 1 lần cho mỗi project):**
1. Khởi tạo repo local: `git init`
2. Tạo repo trên GitHub, copy SSH link
3. Liên kết repo local với repo GitHub: `git remote add origin <ssh_link>`

**Làm mỗi khi có thay đổi:**
1. Thêm code: `git add .`
2. Thêm commit: `git commit -m "<message>"` (message = tên phiên bản)
3. Push code: `git push origin main` (chọn yes nếu được hỏi)

**Invite collaborator:**
1. Truy cập phần Settings → Collaborators của repo trên GitHub
2. Add collaborator