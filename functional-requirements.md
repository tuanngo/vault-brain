---
type: Note
belongsTo:
  - "[[Veegoo]]"
relationships:
  Type:
    - "[[note]]"
  belongs_to:
    - "[[Veegoo]]"
---

# Functional Requirements & Planning

Tài liệu này chi tiết hóa các yêu cầu chức năng (Functional Requirements) cho dự án [[Veegoo]] theo cấu trúc Epic và Use Case, cùng với lộ trình triển khai (Planning).

## 1. Project Planning (Lộ trình phát triển)

Lộ trình được chia thành 3 giai đoạn chính để đảm bảo tính khả thi và tập trung vào giá trị cốt lõi của MVP.

### Giai đoạn 1: Solo Operator MVP (Trọng tâm hiện tại)
- Thiết lập nền tảng hệ thống (Multi-tenant).
- Quản lý đội xe và tài xế cơ bản.
- Quản lý Tuyến và Chuyến đơn lẻ.
- Hệ thống đặt chỗ đơn giản cho khách hàng.
- Dashboard vận hành cho chủ xe.

### Giai đoạn 2: Collaboration & Partner Sharing
- Tính năng chia sẻ tuyến đường với đối tác.
- Hệ thống tính toán và phân chia hoa hồng tự động.
- Mở rộng quản lý đặt chỗ nâng cao.

### Giai đoạn 3: Advanced Operations & Scaling
- Ứng dụng di động dành cho Tài xế (Driver App).
- Theo dõi GPS thời gian thực nâng cao.
- Hệ thống thông báo tự động (SMS/Email/Push).
- Báo cáo và phân tích chuyên sâu.

---

## 2. Functional Requirements (Yêu cầu chức năng)

### Epic 1: Account & Operator Management
*Mục tiêu: Quản lý danh tính và không gian làm việc của các nhà xe.*

| ID | Use Case | Mô tả |
|---|---|---|
| UC1.1 | Đăng ký/Đăng nhập | Nhà xe có thể tạo tài khoản và đăng nhập vào hệ thống. |
| UC1.2 | Onboarding & Tạo Workspace | Luồng hướng dẫn thiết lập không gian làm việc (Workspace) ngay sau khi đăng ký thành công. |
| UC1.3 | Quản lý Profile Nhà xe | Cập nhật thông tin chi tiết công ty, logo, địa chỉ và thông tin liên hệ. |
| UC1.4 | Quản lý Thành viên | Chủ xe có thể mời nhân viên (điều phối viên) vào workspace và phân quyền. |

### Epic 2: Fleet & Resource Management
*Mục tiêu: Quản lý các nguồn lực vận tải (xe và tài xế).*

| ID | Use Case | Mô tả |
|---|---|---|
| UC2.1 | Quản lý xe | Thêm, sửa, xóa thông tin xe (biển số, loại xe, số ghế). |
| UC2.2 | Quản lý tài xế | Thêm thông tin tài xế, bằng lái và thông tin liên lạc. |
| UC2.3 | Phân công nguồn lực | Gán tài xế cố định cho xe hoặc gán linh hoạt theo chuyến. |

### Epic 3: Route & Trip Scheduling
*Mục tiêu: Thiết lập mạng lưới vận chuyển và lịch trình chạy.*

| ID | Use Case | Mô tả |
|---|---|---|
| UC3.1 | Thiết lập Tuyến (Route) | Định nghĩa điểm đón, điểm trả và các trạm dừng giữa hành trình. |
| UC3.2 | Tạo lịch trình (Schedule) | Thiết lập lịch chạy định kỳ hoặc linh hoạt cho các tuyến. |
| UC3.3 | Quản lý Chuyến (Trip) | Tạo các chuyến chạy cụ thể dựa trên lịch trình, gán xe và tài xế. |

### Epic 4: Booking & Customer Management
*Mục tiêu: Tự động hóa quy trình nhận khách và quản lý hành khách.*

| ID | Use Case | Mô tả |
|---|---|---|
| UC4.1 | Form đặt chỗ | Khách hàng có thể điền thông tin đặt chỗ trên giao diện web. |
| UC4.2 | Xác nhận đặt chỗ | Hệ thống tự động xác nhận và giữ chỗ dựa trên số ghế trống. |
| UC4.3 | Danh sách hành khách | Tự động tổng hợp manifest cho từng chuyến chạy để tài xế/điều phối theo dõi. |

### Epic 5: Partner Collaboration (Phase 2)
*Mục tiêu: Kết nối các nhà xe để tối ưu hóa công suất.*

| ID | Use Case | Mô tả |
|---|---|---|
| UC5.1 | Chia sẻ chuyến | Nhà xe có thể đẩy chuyến trống cho đối tác trong hệ thống. |
| UC5.2 | Quản lý hoa hồng | Thiết lập tỷ lệ chia sẻ doanh thu khi hợp tác liên xe. |
| UC5.3 | Đối soát tự động | Hệ thống tính toán số tiền cần thanh toán giữa các bên vào cuối kỳ. |

### Epic 6: Operational Dashboard & Tracking
*Mục tiêu: Cung cấp cái nhìn tổng thể về tình hình vận hành.*

| ID | Use Case | Mô tả |
|---|---|---|
| UC6.1 | Dashboard tổng quan | Xem nhanh số lượng chuyến trong ngày, doanh thu dự kiến và tỷ lệ lấp đầy ghế. |
| UC6.2 | Theo dõi trạng thái chuyến | Cập nhật trạng thái (Chưa khởi hành, Đang chạy, Hoàn thành, Hủy). |
| UC6.3 | Theo dõi vị trí (MVP) | Xem vị trí gần nhất của xe dựa trên cập nhật thủ công hoặc GPS cơ bản. |