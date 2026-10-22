# Cài bộ GitHub Profile: LuKi Anime Coder

Tài khoản: https://github.com/lusieakiquata

## 1) Tạo repository profile

1. Mở https://github.com/new.
2. **Repository name**: `lusieakiquata` (chính xác giống username).
3. Chọn **Public** và bật **Add a README file**.
4. Chọn **Create repository**. Đã có repo đó thì bỏ qua bước này.

GitHub hiển thị README profile khi repo trùng username, public và có `README.md` ở thư mục gốc.

## 2) Đưa mã lên GitHub

### Cách dễ dùng với Git / terminal

Giải nén `LuKi-Anime-Coder-GitHub-Profile.zip` rồi làm như sau:

```bash
git clone https://github.com/lusieakiquata/lusieakiquata.git
cd lusieakiquata
```

**Sao chép 3 mục** từ thư mục vừa giải nén vào thư mục `lusieakiquata`:

- `README.md` (ghi đè README ban đầu),
- `assets/banner.svg`,
- `.github/workflows/snake.yml`.

Sau đó:

```bash
git add README.md assets/banner.svg .github/workflows/snake.yml
git commit -m "style: add LuKi anime coder profile"
git push origin main
```

Nếu nhánh mặc định không phải `main`, thay `main` bằng tên nhánh tương ứng. Có thể upload qua VS Code/GitHub Desktop theo cùng cấu trúc thư mục. **Đừng upload nguyên file ZIP lên repo và mong nó tự giải nén.**

## 3) Chạy hiệu ứng con rắn

1. Mở repo `lusieakiquata/lusieakiquata` > tab **Actions**.
2. Chọn **Generate Anime Coder Snake**.
3. Chọn **Run workflow**, chạy trên nhánh chứa `snake.yml`.
4. Khi workflow thành công, một nhánh `output` sẽ chứa `snake-light.svg` và `snake-dark.svg`.
5. Quay về profile để xem. Cần một lần chạy thành công trước khi ảnh snake xuất hiện.

Workflow tự chạy khoảng 09:17 sáng giờ Việt Nam mỗi ngày (GitHub có thể chạy trễ). Token của workflow được giới hạn phạm vi `contents: write` để xuất ảnh ra branch `output`.

**Nếu bị 403 / permission denied:** Kiểm tra repo **Settings > Actions > General > Workflow permissions** và cho phép Read and write permissions nếu thiết lập tài khoản cho phép. Đảm bảo repository cho phép action `Platane/snk` và `crazy-max/ghaction-github-pages` chạy. Không cần tự tạo personal access token (PAT).

## 4) Tùy biến

- Banner: sửa trực tiếp `assets/banner.svg`. Có thể mở bằng trình duyệt để xem; chỉ dùng font hệ thống, không cần tải font.
- Dòng chữ tự gõ: tìm `readme-typing-svg.demolab.com` trong `README.md`, sửa tham số `lines=`. Mỗi dòng được ngăn bằng `;`.
- Màu: đen `#0B1020`, xanh `#80C7FF`, tím `#B59BFF`, hồng `#FF96C8`.
- Dự án: thay các hàng ở bảng **Selected Quests**.
- Các đường link sử dụng tài khoản `lusieakiquata` và các repo có thật đã được kiểm tra.

## 5) Kiểm tra / xử lý lỗi

- **Banner không hiện:** kiểm tra đúng tên `assets/banner.svg` (phân biệt hoa thường).
- **Snake bị ảnh lỗi:** chạy Action lần đầu; kiểm tra nhánh `output` và hai file SVG đã được đẩy lên.
- **GitHub Stats bị lỗi:** đây là ảnh tải từ bên thứ ba, có lúc gặp giới hạn lượt truy cập. Phần này được để trong `details` và có thể xóa hoàn toàn mà không ảnh hưởng các phần còn lại.
- **Typing không chạy:** mở URL ảnh trực tiếp xem dịch vụ đang hoạt động; animation có thể bị ảnh hưởng bởi chế độ giảm chuyển động/trình duyệt.

## Lưu ý

Các hiệu ứng không cần đặt mật khẩu/API key vào README. README và workflow **chưa được tự động đăng lên GitHub của bạn** từ gói tải này.
