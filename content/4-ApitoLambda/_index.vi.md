---
title : "Cấu hình API Gateway"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---
Cấu hình API Gateway là bước quan trọng để quản lý và bảo vệ luồng truy cập đến các dịch vụ backend như AWS Lambda, EC2, hoặc các hệ thống khác. Việc cấu hình giúp chúng ta:

- Kiểm soát truy cập: chỉ cho phép người dùng hoặc ứng dụng hợp lệ gọi API.

- Chuyển đổi định dạng dữ liệu: từ HTTP request thành input phù hợp cho Lambda hoặc dịch vụ backend.

- Bảo mật: hỗ trợ xác thực (API key, JWT, IAM), giới hạn tốc độ gọi (throttling), chống DDoS.

- Quản lý phiên bản và monitoring: dễ dàng theo dõi, phân tích log và triển khai nhiều phiên bản API.

- Tóm lại, cấu hình API Gateway giúp đảm bảo API hoạt động an toàn, hiệu quả và dễ quản lý trong môi trường sản xuất.
#### Nội Dung
4.1 [Cấu hình API Gateway REST API kết nối Lambda](4.1-updateiamrole/)