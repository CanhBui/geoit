# GeoIT - Dashboard NCTT được mã hóa

Trang tĩnh GitHub Pages tại https://canhbui.github.io/geoit/. `index.html` chỉ là giao diện nhập mật khẩu; `payload.json` lưu bản báo cáo mã hóa AES-256-GCM bằng khóa dẫn xuất PBKDF2-SHA-256 (600.000 vòng). Mật khẩu **không nằm trong repository** và không được gửi về máy chủ.

**Cảnh báo:** GitHub Pages không có xác thực người dùng ở phía máy chủ. Dữ liệu ciphertext vẫn công khai và có thể bị thử mật khẩu ngoại tuyến; nên dùng mật khẩu mạnh dài. Người biết mật khẩu có thể lưu nội dung giải mã. Lịch sử commit cũ của repository vẫn có thể chứa bản HTML và JSON chưa mã hóa. Muốn loại bỏ lịch sử này cần quy trình làm sạch lịch sử riêng và vẫn không thể thu hồi các bản đã bị tải trước đó.

Chỉ sửa mã nguồn dashboard trong bản mã hóa bằng cách giải mã nguồn một cách an toàn ở máy tính có kiểm soát, thay đổi, mã hóa lại với muối/IV mới, rồi cập nhật `payload.json`.
