# Mẫu Pyrogram Telegram Python Bot

Đây là một mẫu để tạo bot Telegram bằng cách sử dụng Pyrogram, MongoDB và Python.

## Bắt đầu

### Điều kiện tiên quyết
- Python 3.7 or higher
- Pyrogram library
- MongoDB

### Cài đặt

1. Nhân bản kho lưu trữ:

   ```bash
   git clone https://github.com/iamritiensinh/PyrogramBot
   cd PyrogramBot
   ```

3. Cài đặt các phụ thuộc:

   ```bash
   #Không bắt buộc
   python3 -m venv env
   source env/bin/activate # mac OS
   env/Scripts/activate.bat # CMD
   env/Scripts/Activate.ps1 # Powershel
   ```

   ```bash
   pip install -r requirements.txt
   ```

4. Thiết lập cơ sở dữ liệu MongoDB của bạn và lấy URI kết nối.

5. Tạo tệp `.env` trong thư mục gốc của dự án và thêm URI kết nối MongoDB và mã thông báo bot Telegram của bạn:

   ```
   DATABASE_URI=your-mongodb-connection-uri
   DATABASE_NAME=your-database-name
   API_ID=your-api-id
   API_HASH=your-api-hash
   BOT_TOKEN=your-bot-token
   ```

6. Chạy bot:

   ```bash
   python bot.py
   ```

## Các tính năng

- Khung Pyrogram để tương tác với Telegram API.
- MongoDB để lưu trữ dữ liệu.
- Dễ dàng mở rộng để thêm nhiều tính năng hơn.

## Đóng góp

Đóng góp được hoan nghênh! Vui lòng làm theo các hướng dẫn tiêu chuẩn khi đóng góp.

## Giấy phép

Dự án này được cấp phép theo MIT [License](LICENSE).
