# Microsoft Word AI Assistant — Add-in Manifest

Manifest cấu hình triển khai tiện ích bổ sung (Office Add-in) cho **Microsoft Word**, tích hợp trợ lý AI thông minh hỗ trợ soạn thảo, biên tập, và nhận xét tài liệu.

## 📌 Tổng quan

Tệp `manifest.xml` khai báo các thông số tích hợp giao diện người dùng và quyền truy cập API theo chuẩn Microsoft Office Add-in Platform (WordApi ≥ 1.3).

* **Tên tiện ích**: Trợ lý AI Word
* **Loại tiện ích**: TaskPane Add-in
* **Phạm vi quyền**: `ReadWriteDocument` (Đọc và chỉnh sửa tài liệu Word)
* **Máy chủ dịch vụ (TaskPane URL)**: `https://word-bridge.2tocom.space`

---

## 🚀 Hướng dẫn cài đặt thử nghiệm (Sideloading)

### Cách 1: Cài đặt trên Word Desktop (Windows / macOS)
1. Chia sẻ thư mục chứa file `manifest.xml` trên mạng cục bộ (Network Share) hoặc đưa vào danh mục Tin cậy (Trusted Catalogs).
2. Mở Microsoft Word, vào **File** > **Options** > **Trust Center** > **Trust Center Settings** > **Trusted Add-in Catalogs**.
3. Thêm đường dẫn mạng của thư mục chứa `manifest.xml` và tích chọn **Show in Menu**.
4. Khởi động lại Word, vào tab **Insert** > **My Add-ins** > **Shared Folder** và chọn **Trợ lý AI Word**.

### Cách 2: Cài đặt trên Word Online (Web)
1. Mở tài liệu bất kỳ trên [Office 365 / Word Online](https://office.live.com).
2. Vào tab **Insert** > **Add-ins** > **Upload My Add-in**.
3. Duyệt và chọn file `manifest.xml` từ máy tính của bạn.
4. Nút bấm **Trợ lý AI** sẽ xuất hiện trên thanh công cụ Home ribbon.

---

## 🛠 Yêu cầu kỹ thuật
* **Microsoft Word**: Word 2016 trở lên, Microsoft 365, hoặc Word on the Web.
* **WordApi Requirement Set**: `1.3` trở lên.
* **Môi trường kết nối**: Cần truy cập được máy chủ cung cấp giao diện Taskpane HTTPS hợp lệ.
