Dưới đây là bản dịch tiếng Việt đầy đủ cho tài liệu bạn cung cấp:

---

# 🚀 Tự Động Hóa Testnet Monad

![Monad-BOT](https://img.shields.io/badge/Monad-BOT-blue.svg) ![License](https://img.shields.io/badge/License-ISC-green.svg) ![Platform](https://img.shields.io/badge/Platform-MacOS%2FLinux%2FWindows-lightgrey.svg)

**Monad-Testnet-Automation** là một công cụ tự động hóa blockchain được thiết kế để tương tác với các dịch vụ tiền mã hóa như hoán đổi và staking token. Công cụ này cung cấp **bảng điều khiển thời gian thực** để theo dõi hoạt động, ghi log giao dịch và tự động hóa các thao tác như **wrap/unwap** và **staking/unstaking**.

---

## ✨ Tính Năng

✔️ **Bảng Điều Khiển Tương Tác** – Cập nhật thời gian thực về số dư, trạng thái mạng và lịch sử giao dịch.  
✔️ **Chu Kỳ Tự Động** – Cấu hình chu kỳ tác vụ để thực hiện các thao tác hoán đổi và staking.  
✔️ **Tương Tác Blockchain** – Sử dụng `ethers.js` để thực thi smart contract mượt mà.  
✔️ **Hỗ Trợ Nhiều Dịch Vụ** – Hỗ trợ Rubic Swap, Izumi Swap, Bean Swap và nhiều hơn nữa.  
✔️ **Bảo Mật Khóa Riêng** – Tải khóa riêng từ tệp `private.key` một cách an toàn.  
✔️ **Cấu Hình Linh Hoạt** – Dễ dàng điều chỉnh các thông số chu kỳ, RPC, địa chỉ hợp đồng.  
✔️ **Hỗ Trợ Nhiều Ví** – Chạy bot cho nhiều ví cùng lúc bằng cách thêm nhiều khóa riêng.

---

## 📦 Hướng Dẫn Cài Đặt

### ✅ Yêu Cầu Trước Khi Cài

Hãy đảm bảo bạn đã cài đặt:
- **Node.js** (phiên bản 16 trở lên) – [Tải tại đây](https://nodejs.org/)
- **Git** (tùy chọn, để clone kho mã)

### 🔧 Các Bước Cài Đặt

#### 🖥️ MacOS & Linux
1️⃣ Mở terminal và chạy:
```bash
# Clone kho mã
git clone https://github.com/bronkdrop/Monad-Testnet-Bot.git
cd Monad-Testnet-Bot
# Cài đặt thư viện phụ thuộc
npm install
```

2️⃣ Thêm **khóa riêng** của bạn vào tệp `private.key` (mỗi dòng một khóa nếu nhiều ví):
```bash
nano private.key
```

3️⃣ Khởi chạy bot:
```bash
npm start
```

#### 🖥️ Windows
1️⃣ Mở **PowerShell** và chạy:
```powershell
# Clone kho mã
git clone https://github.com/bronkdrop/Monad-Testnet-Bot.git
cd Monad-Testnet-Bot

# Cài đặt thư viện phụ thuộc
npm install
```

2️⃣ Thêm **khóa riêng** của bạn vào `private.key` (dùng Notepad hoặc PowerShell, mỗi dòng một khóa):
```powershell
notepad private.key  # Mở Notepad để chỉnh sửa file
```
Dán khóa riêng, lưu lại và đóng Notepad.

3️⃣ Khởi chạy bot:
```powershell
npm start
```

---

## 🛠️ Cấu Hình

Chỉnh sửa file `config/config.json` để tùy chỉnh:
- **Cài Đặt Mạng**: Cập nhật URL RPC và trình khám phá block.
- **API Bên Ngoài**: Xác định endpoint cho các dịch vụ staking và thanh khoản.
- **Địa Chỉ Hợp Đồng**: Điều chỉnh địa chỉ các smart contract đang dùng.
- **Thông Số Chu Kỳ**: Sửa đổi chu kỳ mặc định, thời gian chờ và độ trễ.

---

## 🚀 Hướng Dẫn Sử Dụng

### 📊 Chạy Bot
- Khởi chạy bot:
  ```bash
  npm start
  ```
- Bảng điều khiển trong terminal sẽ hiển thị:
  - ✅ Cập nhật số dư
  - 🔄 Log giao dịch
  - ⏳ Trạng thái Swap/Staking
  - 📊 Tiến trình qua các chu kỳ
  - 🔄 **Xử lý nhiều ví**

### 🔄 Dịch Vụ Hỗ Trợ
Bot tương tác với các dịch vụ sau:
- **Giao Dịch**: Gửi MON ngẫu nhiên đến các ví trong `wallets.txt`, triển khai smart contract ngẫu nhiên
- **Hoán Đổi (Swap)**: Uniswap, Rubic Swap, Izumi Swap, Bean Swap, Monorail
- **Staking**: Magma Staking, aPriori Staking, Kitsu Staking
- **Tác Vụ Token**: Kiểm tra số dư, tự động wrap/unstake
- **Nhiều Ví**: Hỗ trợ chạy giao dịch lặp cho nhiều ví liên tục

