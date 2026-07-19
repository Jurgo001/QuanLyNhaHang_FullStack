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

<img width="1877" height="886" alt="image" src="https://github.com/user-attachments/assets/ffaf66b5-ddb0-4898-8709-7912a377742e" />
<img width="1901" height="896" alt="image" src="https://github.com/user-attachments/assets/3b38daa1-4a9d-4536-a326-869b68e822d3" />
<img width="1867" height="892" alt="image" src="https://github.com/user-attachments/assets/fdc8398c-9d08-47f4-9921-241a0cd4709c" />
<img width="1877" height="896" alt="image" src="https://github.com/user-attachments/assets/a1af4777-2ca3-41c0-913f-25c7251973bb" />
<img width="1876" height="906" alt="image" src="https://github.com/user-attachments/assets/96314001-9f2f-4a0c-ace9-992e0fdb7324" />
<img width="1875" height="900" alt="image" src="https://github.com/user-attachments/assets/d6e35f12-c432-40fd-b5c0-d4f7d6e1c8a8" />
<img width="1872" height="903" alt="image" src="https://github.com/user-attachments/assets/5038d7e2-e25f-4299-ba62-886fd5face6a" />


## Định hướng phát triển

* Bổ sung phân quyền chi tiết cho từng vai trò
* Cải thiện bảo mật đăng nhập
* Tối ưu giao diện responsive
* Hoàn thiện chức năng báo cáo doanh thu nâng cao
* Tích hợp thêm hình thức thanh toán trực tuyến

## Tác giả

**Trương Khả Hào**
GitHub: https://github.com/Jurgo001
