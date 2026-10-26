# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên:** Đỗ Thành CHung 
- **Lớp:** CNTT03
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```shell
pwd
ls -Recurse
 mv .\cap_nhat.txt .\docs\
 mv .\logo_gamezone.png .\media\
 cp .\media\logo_gamezone.png .\backup\
 rm .\temp_207.tmp
  cd .\logs\
  ls
 cd..


```

### Kết quả liệt kê toàn bộ dự án

```text
Directory: C:\Users\Admin\Downloads\de-on-tap-game\starter-kit\game
    zone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:23 PM                backup
d-----        10/26/2026   2:23 PM                data
d-----        10/26/2026   1:22 PM                docs
d-----        10/26/2026   2:07 PM                logs
d-----        10/26/2026   1:23 PM                media
-a----        10/26/2026   1:10 PM             70 .env
-a----        10/26/2026   1:58 PM            223 auto_report_khung.ps1
-a----        10/26/2026   1:10 PM           1437 bai_lam.md

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
Get-Content .\logs\game.log | Select-String "ERROR" >> .\logs\daily_report.txt
 Get-Content .\logs\daily_report.txt
Get-Content .\logs\daily_report.txt -TotalCount 3

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game

```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [ ] Heading 1
- [ ] Mô tả in đậm + in nghiêng
- [ ] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [ ] Code block lệnh liệt kê
- [ ] Task list (≥2 việc, ≥1 đã xong)
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```shell
 Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
 .\auto_report_khung.ps1

```

### Nội dung file logs/auto_report.txt

```text
Da tao bao cao: HOAN_THIEN

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(Get-Content .\logs\game.log | Select-String "ERROR").Count

```

### Kết quả đếm

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
"===TONG HOP LOG===" >> .\logs\tong_hop.txt
Get-Content .\logs\game.log | Select-String "WARNING" >> .\logs\tong_hop.txt
(Get-Content .\logs\daily_report.txt | Select-String "ERROR" >> .\logs\tong_hop.txt).Count

```

### Nội dung file logs/tong_hop.txt

```text
 = = = T O N G   H O P   L O G = = = 
 
 
 
 2 0 2 5 - 1 1 - 0 5   0 8 : 5 4 : 1 5   [ W A R N I N G ]   M a y   c h u   q u a   t a i   C P U   9 0 % 
 
 
 
 
 
  6

```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
