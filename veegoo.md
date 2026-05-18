---
type: Project
Status: Active
_organized: true
---
# Veegoo

**Veegoo** là nền tảng SaaS quản lý vận tải (TMS — Transport Management System) dành cho các nhà xe cá nhân, đội xe doanh nghiệp và dịch vụ vận chuyển nhân viên. Veegoo giúp đơn giản hóa việc quản lý tuyến, xe, khách hàng và tài xế — tất cả trong một nơi.

## Overview

Veegoo giải quyết bài toán vận hành hàng ngày của các nhà xe vừa và nhỏ: theo dõi xe theo thời gian thực, quản lý lịch chạy và tuyến đường, nhận đặt chỗ từ khách hàng, và phối hợp với các nhà xe khác khi có xe trống. Nền tảng hỗ trợ mô hình **đơn lẻ** (một cá nhân tự quản lý xe của mình) lẫn mô hình **hợp tác** (nhiều nhà xe chia sẻ tuyến và hoa hồng).

Ở giai đoạn **MVP**, trọng tâm là cá nhân hoặc nhóm nhỏ: một chủ xe có thể tự vận hành, đăng ký tuyến, nhận khách đặt chỗ, và mở rộng sang hợp tác liên xe khi cần.

## Goals

- **Đơn giản hóa vận hành** — cho phép một người quản lý toàn bộ hoạt động xe của mình mà không cần đội ngũ hành chính.
- **Tăng hiệu suất xe trống** — kết nối các nhà xe cá nhân để chia sẻ tuyến, giảm chuyến xe chạy rỗng.
- **Minh bạch hoa hồng** — tự động tính toán và phân chia doanh thu khi hợp tác liên xe.
- **Mở rộng dần** — từ mô hình MVP cá nhân đến quản lý đội xe doanh nghiệp và vận chuyển nhân viên khu công nghiệp.

## Target Users

| Người dùng | Vai trò |
|---|---|
| **Chủ nhà xe / Chủ doanh nghiệp** | Quản lý toàn bộ hoạt động, xe, tuyến, doanh thu và đối tác hợp tác |
| **Điều phối viên (Dispatcher)** | Phân công tài xế, theo dõi lịch chạy và xử lý sự cố vận hành hàng ngày |
| **Tài xế** | Nhận lịch chạy, xem tuyến đường, cập nhật trạng thái chuyến |
| **Khách hàng / Nhân viên** | Đặt chỗ, xem thông tin chuyến xe, theo dõi xe đến |

> **MVP focus:** Chủ nhà xe cá nhân — người vừa là chủ vừa là điều phối, có thể chỉ có 1–2 xe đang vận hành.

## Key Concepts

### Tuyến (Route)
Hành trình cố định hoặc linh hoạt giữa điểm đón và điểm trả. Một tuyến có thể do một nhà xe vận hành hoặc được chia sẻ với nhà xe đối tác.

### Chuyến (Trip)
Một lần chạy cụ thể trên một tuyến, gắn với tài xế, xe, thời gian xuất phát và danh sách khách.

### Đặt chỗ (Booking)
Yêu cầu của khách hàng để tham gia một chuyến cụ thể. Hệ thống xác nhận, phân chỗ và thông báo tự động.

### Hợp tác liên xe (Partner Sharing)
Khi xe của một nhà xe còn trống, họ có thể mời nhà xe đối tác ghép khách hoặc nhượng tuyến. Hoa hồng được tính và phân chia tự động theo tỷ lệ thỏa thuận.

### Nhà xe (Operator)
Đơn vị vận hành — có thể là cá nhân sở hữu 1 xe hoặc doanh nghiệp có đội xe lớn. Mỗi Operator có không gian riêng (multi-tenant).

## Key Features

- **Quản lý tuyến & chuyến** — tạo, chỉnh sửa lịch chạy và tuyến đường linh hoạt
- **Đặt chỗ từ khách hàng** — form đặt chỗ, xác nhận tự động, danh sách hành khách
- **Hợp tác liên xe** — chia sẻ tuyến, phân chia hoa hồng giữa các nhà xe đối tác
- **Theo dõi xe thời gian thực** — GPS tracking, trạng thái chuyến trực tiếp
- **Dashboard vận hành** — tổng quan doanh thu, chuyến chạy, xe và tài xế
- **Ứng dụng Tài xế** *(Next phase)* — nhận lịch, cập nhật trạng thái từ điện thoại
- **Multi-tenant** — mỗi nhà xe có dữ liệu và quyền truy cập riêng biệt