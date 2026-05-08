# LE QUY DIGITAL Website

Website công ty chuẩn để xác minh Meta Business Manager.

## Cấu trúc file

```
lequydigital-website/
├── index.html      # Trang chủ
├── privacy.html    # Chính sách bảo mật (BẮT BUỘC cho Meta)
├── terms.html      # Điều khoản sử dụng (BẮT BUỘC cho Meta)
└── styles.css      # CSS chung
```

## Cách deploy

### Cách 1: GitHub Pages (miễn phí, dễ nhất)

1. Tạo repo mới trên GitHub: `lequydigital-website` (public)
2. Upload toàn bộ file vào repo
3. Vào Settings → Pages → Source: chọn `main` branch → Save
4. GitHub cấp link: `https://<username>.github.io/lequydigital-website/`
5. Vào DNS của domain `lequydigital.com`, thêm CNAME trỏ về `<username>.github.io`
6. Trong repo, tạo file `CNAME` chứa nội dung: `lequydigital.com`

### Cách 2: Cloudflare Pages (miễn phí, nhanh hơn)

1. Đăng nhập Cloudflare → Pages → Create project
2. Connect GitHub repo `lequydigital-website`
3. Build setting: để trống (static HTML)
4. Deploy → có link `*.pages.dev`
5. Custom domain → trỏ `lequydigital.com` về

### Cách 3: Server riêng

1. SSH vào server, copy folder lên `/var/www/lequydigital/`
2. Cấu hình Nginx/Apache trỏ domain về folder này
3. Cài SSL bằng `certbot`

## Sau khi deploy xong

Truy cập các URL này phải hoạt động:
- https://lequydigital.com/
- https://lequydigital.com/privacy.html
- https://lequydigital.com/terms.html

Nếu cả 3 link mở được → sẵn sàng submit BM.
