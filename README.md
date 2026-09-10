# Hướng dẫn cài đặt & bắt đầu — Nodeflow Studio (bản beta)

Chào mừng bạn tới bản dùng thử Nodeflow Studio. Tài liệu này đưa bạn đi từ lúc tải phần mềm
đến khi chạy được workflow đầu tiên trên máy của bạn. Mất khoảng **10–15 phút**.

> **Nodeflow Studio là gì?** Một công cụ dựng "dây chuyền" tạo ảnh/video bằng AI (Grok, ChatGPT,
> Google Vids) chạy **ngay trên máy bạn**. Bạn dùng tài khoản AI của chính mình; ảnh/video và
> nhật ký nằm ở máy bạn, không tải lên đám mây.

---

## 0. Chuẩn bị

- **Hệ điều hành:** Windows 10 hoặc 11 (64-bit).
- **Mạng khi cài:** cần Internet lúc cài đặt (phần mềm tự tải thành phần hiển thị *WebView2* nếu
  máy chưa có — đa số máy Windows 11 đã có sẵn nên bước này thường tức thì).
- **Tài khoản AI của bạn:** ít nhất một tài khoản Grok / ChatGPT / Google Vids để đăng nhập vào
  trong phần mềm (bạn tự đăng nhập bằng tay, phần mềm không giữ mật khẩu của các tài khoản này).

---

## 1. Tải và cài đặt

1. Tải tệp cài đặt mới nhất tại **https://github.com/ken-online/nodeflow-studio-releases/releases/latest**
   (tệp **`Nodeflow Studio_<phiên bản>_x64-setup.exe`**).
2. Bấm đúp để chạy.

### Khi gặp màn hình xanh "Windows đã bảo vệ PC của bạn"

Bản beta **chưa mua chứng chỉ ký số** (để giữ chi phí bằng 0 trong giai đoạn thử nghiệm), nên
Windows SmartScreen sẽ cảnh báo về một ứng dụng "chưa được nhận diện". Đây là điều **bình thường**
với phần mềm mới — không phải virus. Cách qua:

1. Bấm dòng chữ **"Thông tin thêm"** (*More info*).
2. Bấm nút **"Vẫn chạy"** (*Run anyway*) hiện ra bên dưới.

> Nếu trình duyệt (Edge/Chrome) cũng cảnh báo lúc **tải** tệp, chọn **Giữ lại** (*Keep*) → *Giữ dù sao*.

3. Làm theo trình cài đặt tới khi xong. Phần mềm cài cho **người dùng hiện tại** (không cần quyền
   Administrator) và tạo lối tắt trong Start Menu tên **Nodeflow Studio**.

---

## 2. Tạo tài khoản Studio (trên web)

Tài khoản Studio là nơi quản lý workflow và các máy chạy của bạn. Tạo một lần, dùng mãi.

1. Mở trình duyệt, vào: **https://vwf-studio.hoangxnam.workers.dev**
2. Bấm **"Tạo tài khoản"** (ngay trang chủ, cạnh nút Tải cho Windows — hoặc vào thẳng `/dang-ky`).
3. Điền **Email** + **Mật khẩu** (tối thiểu 8 ký tự). Ô *Tên xưởng* không bắt buộc.
4. Bấm **Tạo tài khoản** → bạn được đưa thẳng vào trang quản lý (`/app`).

> **Nên bật xác thực hai lớp (2FA):** vào **Cài đặt** (góc trên) → **Bật xác thực hai lớp**, quét mã
> bằng Google Authenticator / 1Password, rồi **lưu các mã khôi phục** (chúng chỉ hiện đúng một lần).

---

## 3. Ghép máy tính của bạn với tài khoản

Bước này nối phần mềm trên máy bạn với tài khoản Studio vừa tạo. Cần làm **một lần** cho mỗi máy.

**Trên web** (trang `/app` vừa vào):

1. Ở mục **Máy chạy**, bấm **"Thêm máy"**.
2. Màn hình hiện dòng **"Mã ghép (10 phút): XXXXXXXX"**. Mã này sống **10 phút** — cứ để trang mở đó.

**Trên phần mềm** (mở **Nodeflow Studio** từ Start Menu):

3. Bấm nút **Chạy** (hoặc chip trạng thái máy). Phần mềm sẽ lần lượt mở:
   - **Hộp Đăng nhập** → nhập đúng Email/Mật khẩu (và mã 2FA nếu bạn đã bật) của tài khoản Studio ở bước 2.
   - **Hộp Ghép máy** → **dán mã ghép** vừa lấy trên web → bấm **Ghép máy**.
4. Thấy thông báo *"Đã ghép máy này với Studio."* là xong.

> Sau khi ghép, máy có thể hiện trạng thái **"chưa kết nối"** trong giây lát — bình thường. Phần mềm
> tự bật kết nối khi đang mở; bạn không cần chạy lệnh gì thêm.

---

## 4. Thêm và đăng nhập tài khoản AI

Đây là các tài khoản AI **của bạn** mà phần mềm sẽ điều khiển để tạo ảnh/video.

1. Ở thanh bên trái, mở tab **Hồ sơ**.
2. Bấm nút **thêm tài khoản**, rồi:
   - **Tên tài khoản:** đặt tên gợi nhớ (vd "Grok chính").
   - **Proxy:** để trống nếu không dùng.
   - Chọn **loại**: Grok / ChatGPT / Google.
   - Bấm **Thêm**.
3. Trên hàng tài khoản vừa tạo, bấm **"Mở đăng nhập"** → một cửa sổ trình duyệt bật lên.
4. **Đăng nhập tài khoản AI của bạn bằng tay** trong cửa sổ đó (như đăng nhập bình thường).
5. Đăng nhập xong, quay lại phần mềm bấm **"Đã đăng nhập xong"** → phiên được lưu lại, lần sau
   không phải đăng nhập lại.

> Lặp lại cho từng tài khoản AI bạn muốn dùng. Mỗi tài khoản có bộ đếm lượt dùng trong ngày để
> bạn theo dõi.

---

## 5. Chạy workflow đầu tiên

1. Ở tab **Workflow**, tạo một workflow mới (hoặc dùng một **Mẫu có sẵn** nếu có).
2. Thêm các khối (node) và nối chúng thành một dây chuyền: khối **nguồn** (ảnh/video vào) →
   khối **AI** (Grok/ChatGPT/Google) → khối **đầu ra** (lưu tệp / gửi Telegram).
3. Ở khối **nguồn**, tại ô **Thư mục** hãy bấm nút chọn thư mục → cửa sổ Windows mở ra → chọn thư
   mục chứa ảnh/video của bạn. (Chọn thư mục hoặc một tệp là phần mềm **tự cấp quyền** đọc chỗ đó —
   không có bước cấp quyền riêng.)
4. Bấm **Chạy**. Theo dõi tiến độ ngay trên khung vẽ.

---

## 6. Gặp lỗi hoặc muốn góp ý

Bản beta chắc chắn còn thiếu sót — góp ý của bạn rất quý.

- **Kênh phản hồi:** nhắn qua Telegram **https://t.me/ken_online**.
- **Khi báo lỗi**, kèm giúp: bạn đang làm bước nào, khối nào lỗi, và **nội dung nhật ký**. Mở tab
  **Nhật ký** trong phần mềm, chọn nguồn **"Máy này"** (nguồn này ghi chi tiết nhất), rồi bấm nút
  **"Copy"** ở góc để sao chép nhật ký và dán vào tin nhắn.

> **Về quyền riêng tư:** nhật ký chi tiết (đường dẫn tệp, câu lệnh, phiên đăng nhập) nằm **cục bộ
> trên máy bạn** và không tự gửi đi đâu. Khi bạn chủ động sao chép để gửi, hãy xem qua nội dung
> trước — chỉ gửi phần liên quan tới lỗi.

---

## Phụ lục: sự cố thường gặp

| Hiện tượng | Cách xử lý |
|---|---|
| SmartScreen chặn, không thấy nút "Vẫn chạy" | Bấm **"Thông tin thêm"** trước, nút **"Vẫn chạy"** mới hiện ra. |
| Cài xong mở lên báo lỗi thành phần hiển thị | Máy chưa có **WebView2**. Nối mạng rồi cài lại; hoặc tải "Evergreen WebView2 Runtime" từ trang Microsoft. |
| Dán mã ghép báo "không hợp lệ hoặc đã hết hạn" | Mã chỉ sống **10 phút** và **dùng một lần**. Về web bấm **"Thêm máy"** lấy mã mới rồi dán lại. |
| Máy luôn ở trạng thái "chưa kết nối" | Đảm bảo phần mềm **đang mở**. Kết nối tự bật khi App mở; đóng App là ngắt. |
| Bấm Chạy nhưng lần chạy nằm chờ mãi | Thường do **chưa ghép máy** hoặc **chưa đăng nhập tài khoản AI** cần cho workflow. Kiểm tra lại mục 3 và 4. |

---

*Nodeflow Studio — Copyright by Ken Hoàng · Liên hệ: [t.me/ken_online](https://t.me/ken_online)*
