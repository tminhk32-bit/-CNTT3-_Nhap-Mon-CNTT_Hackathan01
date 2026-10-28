# BÀI LÀM – HACKATHON 01

- **Mã đề: 13** 
- **Họ tên: Đào Tuấn Minh** 
- **Lớp: CNTT3** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS): WinDows** 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```Powershell
1. PS D:\starter-kit\ngoai-ngu-website> pwd
2. PS D:\starter-kit\ngoai-ngu-website> ls -Force
3. PS D:\starter-kit\ngoai-ngu-website> mv .\thoi_khoa_bieu.txt .\docs
4. PS D:\starter-kit\ngoai-ngu-website> mv .\logo_trung_tam_ngoai_ngu.PNG .\media
5. PS D:\starter-kit\ngoai-ngu-website> rm .\temp_213.tmp
6. PS D:\starter-kit\ngoai-ngu-website> cp .\media\logo_trung_tam_ngoai_ngu.PNG .\backup
7. PS D:\starter-kit\ngoai-ngu-website> cd .\logs
8. PS D:\starter-kit\ngoai-ngu-website\logs> ls
9. PS D:\starter-kit\ngoai-ngu-website\logs> cd ..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
Directory: D:\starter-kit\ngoai-ngu-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026  10:50 AM                backup
d-----        10/28/2026  11:01 AM                data
d-----        10/28/2026  10:50 AM                docs
d-----        10/28/2026  10:53 AM                logs
d-----        10/28/2026  10:50 AM                media
------        10/27/2026   1:31 AM             68 .env
-a----        10/27/2026   1:31 AM           4365 logo_trung_tam_ngoai_ngu.PNG
------        10/27/2026   1:31 AM             22 temp_213.tmp
-a----        10/27/2026   1:31 AM             67 thoi_khoa_bieu.txt
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```Powershell
PS D:\starter-kit\ngoai-ngu-website> Get-Content ".\logs\course.log" | Select-String "ERROR" > ".\logs\daily_report.txt"

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-03-28 08:24:28 [ERROR] Het thoi gian cho (timeout)
2026-03-28 08:30:28 [ERROR] Het thoi gian cho (timeout)
```

## 4.4. Thao tác với tài liệu Markdown (README.md)
# Ngoai_Ngu_Website
app dùng để **học tiếng anh** và *luyện tập tiếng anh* nhằm ***nâng cao khả năng sử dụng tiếng anh cho học sinh***
| STT | thư mục | nội dung |
| --- | --- | --- |
| 1 | data | hoan thien bao cao excel |
| 2 | media | luu tru logo trung tam tieng anh |

```PowerShell
ls
```
- [x] hoàn thiện báo cáo excel 
- [ ] tạo app học tập online

> không up load file .env
## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```Powershell
1. PS D:\starter-kit\ngoai-ngu-website> Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
2. PS D:\starter-kit\ngoai-ngu-website> .\auto_report.ps1
```

### Kết quả hiển thị

```text

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```Powershell
PS D:\starter-kit\ngoai-ngu-website> (Get-Content ".\logs\course.log" | Select-String "ERROR").count
```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
6
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
1. PS D:\starter-kit\ngoai-ngu-website> ni ".\logs\tong_hop.txt" >> "===TONG HOP LOG ==="
2. PS D:\starter-kit\ngoai-ngu-website> Get-Content ".\logs\course.log" | Select-String "WARNING" > ".\logs\tong_hop.txt"
3. PS D:\starter-kit\ngoai-ngu-website> (Get-Content ".\logs\course.log" | Select-String "ERROR").count >> .\logs\tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
===TONG HOP LOG===

2026-03-28 08:51:28 [WARNING] Thoi gian tai trang cham
2026-03-28 08:54:28 [WARNING] Video bai giang dung luong lon
2026-03-28 08:57:28 [WARNING] Thoi gian tai trang cham

6
```





