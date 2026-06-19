# Hướng dẫn thực hành: Phát hiện dữ liệu nhạy cảm với Amazon Macie
## 1. Các bước thực hiện chính
1.  **Cấu hình Amazon SNS:** Tạo một Topic (Standard type) và đăng ký Email của bạn để nhận thông báo. Hãy nhớ xác nhận trong hộp thư đến.
2.  **Thiết lập Amazon Macie:**
    * Kích hoạt Macie.
    * Tạo Job (One-time hoặc Scheduled) để quét S3 Bucket.
3.  **Cấu hình EventBridge:**
    * Tạo Rule để lắng nghe sự kiện `Macie Finding`.
    * Thiết lập Target trỏ về SNS Topic đã tạo.
4.  **Kiểm tra kết quả:**
    * Khi Macie quét và phát hiện dữ liệu nhạy cảm (PII, Credit Card...), nó sẽ sinh ra một "Finding".
    * Cấu hình trong EventBridge sẽ tự động gửi thông báo qua SNS đến Email của bạn.

## 2. Kết quả thực tế
Dưới đây là minh chứng cho việc hệ thống đã hoạt động:

### Ảnh chụp màn hình: Amazon Macie Finding
(Đây là nơi ghi nhận kết quả phát hiện dữ liệu nhạy cảm từ Job)
![Macie Finding](image/macie.png)

### Ảnh chụp màn hình: Thông báo qua Email
(Khi Macie Finding được tạo, AWS sẽ gửi email thông báo tới địa chỉ bạn đã đăng ký)
![alt](image/emailmacie.png)

---
