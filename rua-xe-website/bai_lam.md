# BÀI LÀM – HACKATHON 01

- **Mã đề:** 22
- **Họ tên:** Hoa Việt Hoàng
- **Lớp:** CNTT3
- **Link repository:** https://github.com/hoaviethoang2002-lab/HN-KS26-CNTT3_Nhap-mon-CNTT_Hackathon01.git
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force -Recurse
mv .\bang_quy_trinh.txt .\docs
mv .\logo_rua_xe.png .\media
cp .\media\logo_rua_xe.png .\backup
rm .\temp_305.tmp
cd .\logs
ls -Force
cd..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
Directory: C:\Users\ADMIN\Downloads\starter-kit\rua-xe-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026  10:59 AM                backup
d-----        10/28/2026  10:50 AM                data
d-----        10/28/2026  10:55 AM                docs
d-----        10/28/2026  10:50 AM                logs
d-----        10/28/2026  10:57 AM                media
------        10/27/2026   1:32 AM             64 .env
-a----        10/27/2026   1:32 AM           2227 bai_lam.md


    Directory: C:\Users\ADMIN\Downloads\starter-kit\rua-xe-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           6191 logo_rua_xe.png


    Directory: C:\Users\ADMIN\Downloads\starter-kit\rua-xe-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           6114 luot_rua_xe_thang_2.xlsx


    Directory: C:\Users\ADMIN\Downloads\starter-kit\rua-xe-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM             53 bang_quy_trinh.txt


    Directory: C:\Users\ADMIN\Downloads\starter-kit\rua-xe-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           1029 carwash.log


    Directory: C:\Users\ADMIN\Downloads\starter-kit\rua-xe-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           6191 logo_rua_xe.png
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
Get-Content .\logs\carwash.log | Select-String "ERROR"
Get-Content .\logs\carwash.log | Select-String "ERROR">.\logs\daily_report.log
Get-Content .\logs\daily_report.log
Get-Content .\logs\daily_report.log -TotalCount 2
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-02-28 08:39:37 [ERROR] Het thoi gian cho (timeout)
2026-02-28 09:03:37 [ERROR] Dat lich that bai
```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] Heading 1: tên dự án
- [ ] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [ ] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [ ] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [ ] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
.\auto_report.ps1
```

### Kết quả hiển thị

```text
Dang loc log ...
Hoan thanh!
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(Get-Content .\logs\carwash.log | Select-String "error").count
6
```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
6
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
"=== TONG HOP LOG ===" >.\logs\tong_hop.txt
Get-Content .\logs\carwash.log | Select-String "warning" >> .\logs\tong_hop.txt
(Get-Content .\logs\carwash.log | Select-String "error").count >>.\logs\tong_hop.txt
Get-Content .\logs\tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG ===

2026-02-28 08:35:37 [WARNING] Anh truoc sau dung luong lon
2026-02-28 08:47:37 [WARNING] Anh truoc sau dung luong lon
2026-02-28 09:23:37 [WARNING] Khoang rua so 2 dong khach
2026-02-28 09:27:37 [WARNING] Thoi gian phan hoi cham


6
```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/luot_rua_xe_thang_2.xlsx`, không cần ghi vào đây.
