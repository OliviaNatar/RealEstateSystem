# 🏠 Real Estate System (Estora)

Hệ thống đăng tin và tiếp nhận yêu cầu bất động sản, xây dựng bằng **ASP.NET MVC 5** và **SQL Server**. Môi giới đăng tin, khách hàng tìm kiếm, lưu tin, gửi yêu cầu và nhắn tin trực tiếp với môi giới.

## ✨ Chức năng chính

**Khách hàng**
- Đăng ký, đăng nhập, quản lý hồ sơ, đổi mật khẩu
- Tìm kiếm và lọc bất động sản (tỉnh/thành, quận/huyện, loại BĐS, loại giao dịch, pháp lý, nội thất, tiện ích)
- Xem chi tiết, tải brochure, lưu tin yêu thích
- Gửi yêu cầu liên hệ và nhắn tin với môi giới

**Môi giới**
- Đăng, sửa, quản lý tin đăng và hình ảnh
- Trả lời yêu cầu và hội thoại của khách hàng
- Quản lý liên hệ Zalo

**Quản trị viên**
- Quản lý người dùng, danh mục, tin đăng, yêu cầu
- Thống kê tổng quan

## 🛠️ Công nghệ

| Thành phần | Công nghệ |
|---|---|
| Backend | ASP.NET MVC 5 (.NET Framework), C# |
| ORM | Entity Framework 6 |
| Cơ sở dữ liệu | Microsoft SQL Server |
| Giao diện | Razor, Bootstrap 5.2, jQuery |
| Bảo mật | BCrypt.Net-Next (băm mật khẩu) |

## 🚀 Cách chạy dự án

**Yêu cầu:** Visual Studio 2022, SQL Server (hoặc SQL Server Express), .NET Framework 4.8.

1. Clone repo:
   ```bash
   git clone https://github.com/OliviaNatar/RealEstateSystem.git
   ```
2. Mở SQL Server Management Studio, chạy file `RealEstateDB.sql` để tạo database `RealEstateDB` kèm dữ liệu mẫu.
3. Mở `RealEstateSystem.sln` bằng Visual Studio. Các thư viện sẽ được tự khôi phục (hoặc chuột phải Solution → *Restore NuGet Packages*).
4. Kiểm tra chuỗi kết nối trong `RealEstateSystem/Web.config`, sửa `Data Source` cho khớp máy của bạn:
   ```xml
   <add name="RealEstateDbContext"
        connectionString="Data Source=localhost;Initial Catalog=RealEstateDB;Integrated Security=True;MultipleActiveResultSets=True"
        providerName="System.Data.SqlClient" />
   ```
5. Nhấn **F5** để chạy.

## 🔑 Tài khoản dùng thử

Dữ liệu mẫu gồm 1 quản trị viên, 5 môi giới, 5 khách hàng, 30 tin đăng. Xem danh sách tài khoản và mật khẩu demo ở phần đầu file `RealEstateDB.sql`.

## 📁 Cấu trúc thư mục

```
RealEstateSystem/
├── RealEstateDB.sql          # Script tạo database + dữ liệu mẫu
├── RealEstateSystem.sln
└── RealEstateSystem/
    ├── Controllers/          # Xử lý logic (Account, Admin, Property, Listing, Conversation, ...)
    ├── Models/               # Entity và ViewModel
    ├── Views/                # Giao diện Razor
    ├── Content/ Scripts/     # CSS, JS, hình ảnh
    └── Web.config
```

## 👤 Tác giả

- Họ tên: Nguyễn Ngọc Phương Nghi
- Liên hệ:[OliviaNatar](https://github.com/OliviaNatar)
