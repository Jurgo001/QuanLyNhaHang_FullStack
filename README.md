# Hệ Thống Quản Lý Đặt Bàn & Gọi Món Nhà Hàng Trực Tuyến

## Giới thiệu

Đây là hệ thống Web/POS quản lý nhà hàng được xây dựng bằng ASP.NET Core MVC, hỗ trợ các nghiệp vụ chính như xem thực đơn, đặt bàn, gọi món, quản lý giỏ hàng, áp dụng voucher và xử lý hóa đơn. Hệ thống hướng đến việc số hóa quy trình vận hành nhà hàng, giúp khách hàng đặt món thuận tiện hơn và hỗ trợ nhân viên/admin quản lý dữ liệu hiệu quả.

## Công nghệ sử dụng

* C#
* ASP.NET Core MVC
* Entity Framework Core
* SQL Server
* LINQ
* Bootstrap 5
* VietQR API
* Git/GitHub

## Chức năng chính

### Khách hàng

* Xem danh sách món ăn theo danh mục
* Tìm kiếm món ăn
* Xem chi tiết món ăn
* Thêm món vào giỏ hàng
* Cập nhật số lượng món trong giỏ hàng
* Áp dụng voucher giảm giá
* Đặt món và tạo hóa đơn
* Đặt bàn trực tuyến
* Xem lịch sử đơn hàng

### Admin/Nhân viên

* Quản lý món ăn
* Quản lý loại món
* Quản lý khách hàng
* Quản lý nhân viên
* Quản lý voucher
* Quản lý đơn hàng
* Cập nhật trạng thái hóa đơn
* Thống kê doanh thu
* Hiển thị danh sách Top 10 món bán chạy

## Điểm nổi bật

* Xây dựng Cart Controller sử dụng Session để quản lý giỏ hàng.
* Tự động tính tổng tiền, cập nhật số lượng món và áp dụng voucher từ cơ sở dữ liệu.
* Sử dụng LINQ GroupBy/Aggregate để thống kê doanh thu và món ăn bán chạy.
* Tích hợp VietQR API hỗ trợ thanh toán chuyển khoản.
* Thiết kế giao diện bằng Bootstrap 5, phù hợp cho cả khách hàng và nhân viên quản lý.

## Cấu trúc dự án

```text
RestaurantManagement/
├── Controllers/
├── Models/
├── Views/
├── Data/
├── wwwroot/
├── appsettings.json
└── Program.cs
```

## Cài đặt và chạy dự án

### 1. Clone repository

```bash
git clone https://github.com/Jurgo001/QuanLyNhaHang_FullStack.git
```

### 2. Mở project

Mở project bằng Visual Studio 2022 hoặc Visual Studio Code.

### 3. Cấu hình cơ sở dữ liệu

Cập nhật chuỗi kết nối trong file `appsettings.json`:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=QuanLyNhaHang;Trusted_Connection=True;TrustServerCertificate=True;"
}
```

### 4. Tạo database

Chạy migration hoặc import file script SQL nếu dự án có sẵn.

```bash
dotnet ef database update
```

### 5. Chạy dự án

```bash
dotnet run
```

Sau đó mở trình duyệt tại:

```text
https://localhost:xxxx
```

## Tài khoản demo

```text
Admin:
Email: truongmilan@nhahang.vn
Password: 123

Khách hàng:
Email: khoa@gmail.com
Password: 123
```


## Hình ảnh giao diện

```md
![Trang chủ](screenshots/home.png)
![Giỏ hàng](screenshots/cart.png)
![Trang quản trị](screenshots/admin.png)
```

## Định hướng phát triển

* Bổ sung phân quyền chi tiết cho từng vai trò
* Cải thiện bảo mật đăng nhập
* Tối ưu giao diện responsive
* Hoàn thiện chức năng báo cáo doanh thu nâng cao
* Tích hợp thêm hình thức thanh toán trực tuyến

## Tác giả

**Trương Khả Hào**
GitHub: https://github.com/Jurgo001
