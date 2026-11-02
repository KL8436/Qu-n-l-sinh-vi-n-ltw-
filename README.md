# Hệ thống quản lý sinh viên

Bài tập lớn môn Lập trình web, PTIT. Hệ thống quản lý thông tin học tập của sinh viên.

## Chức năng

- Quản lý sinh viên (thêm, sửa, xóa, tìm kiếm)
- Quản lý lớp học, điểm số (nhập điểm, tính điểm trung bình)
- Xem bảng điểm, xếp loại học lực
- Phân quyền: Admin, Giảng viên, Sinh viên

## Công nghệ

- Frontend: React + Vite (JavaScript)
- Backend: NestJS + TypeORM (TypeScript)
- Database: MySQL 8.0
- Xác thực: session cookie

## Yêu cầu cài đặt

- Node.js 22 trở lên
- MySQL 8.0
- Git

## Cách chạy sau khi clone

### 1. Tạo database

Đăng nhập MySQL bằng tài khoản root và chạy:

```sql
CREATE DATABASE student_management CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'sm_user'@'localhost' IDENTIFIED BY 'mat_khau_cua_ban';
GRANT ALL PRIVILEGES ON student_management.* TO 'sm_user'@'localhost';
```

### 2. Tạo file `.env`

Sao chép `.env.example` thành `.env` ở thư mục gốc, rồi điền mật khẩu vừa đặt:


copy .env.example .env


### 3. Chạy backend

```powershell
cd backend
npm install
npm run start:dev
```

Mở http://localhost:3000, thấy "Hello World!" là backend đã chạy.

### 4. Chạy frontend

Mở terminal thứ hai:

```powershell
cd frontend
npm install
npm run dev
```

Mở http://localhost:5173.

## Cấu trúc thư mục

```
backend/    NestJS: API và xử lý logic
frontend/   React + Vite: giao diện
database/   File SQL tạo bảng và dữ liệu mẫu
docs/       Ghi chú cho báo cáo
```