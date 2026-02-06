# I. Lab THM
## 1. Lab1 
- Cách hoạt động của 1 trang web:
  + 1 website thì được tạo từ các file:
    - `html` -> tạo giao diện chưa có màu sắc khung xương
    - `css` -> tạo giao diện bố cục
    - `javascript` -> tương tác với người dùng 
  + Khi mà ta truy cập 1 trang web, trình duyệt sẽ gửi yêu cầu đến máy chủ để lấy thông tin về trang ta đang truy cập.
- 1 trang web gồm 2 thành phần chính:
  + `Front-end`: phần giao diện người dùng và tương tác.
  + `Back-end`: phần logic, CSDL và máy chủ phía sau, xử lý yêu cầu, lưu trữ dữ liệu.
- nó có giới thiệu html, css, js nhma e sẽ để 3 cái đấy riêng
## 2. Lab2 
- `HTTP` là giao thức dùng để truyền tải dữ liệu trên web theo mô hình client-sever, trong đó
  + Client gửi request
  + Sever phản hồi lại 
- `HTTPS` là phiên bản bảo mật của HTTP, sử dụng SSL/TLS để mã hóa dữ liệu giúp đảm bảo tính bảo mật và toàn vẹn của thông tin trong quá trình truyền tải.
- các HTTP method:
  + `GET`: dùng để lấy dữ liệu từ server
  + `POST`: gửi dữ liệu để tạo tài nguyên mới
  + `PUT`: cập nhật tài nguyên đã tồn tại
  + `DELETE`: xóa tài nguyên
- HTTP Status Codes phổ biến:
```
            200 - OK
            201 - Created
            301 - Moved Permanently
            302 - Found
            400 - Bad Request
            401 - Not Authorised
            403 - Forbidden
            405 - Method Not Allowed
            404 - Page Not Found
            500 - Internal Service Error
            503 - Service Unavailable
```
- HTTP Headers:
  + Headers cung cấp thông tin bổ sung cho request và response, ví dụ:
    - `Host`: xác định tên miền server
    - `User-Agent`: thông tin trình duyệt hoặc công cụ gửi request
    - `Content-Type`: kiểu dữ liệu được gửi hoặc nhận
    - `Content-Length`: độ dài nội dung
- Cookies là dữ liệu được server gửi cho client và lưu trên trình duyệt, thường được sử dụng để:
  + Quản lý phiên đăng nhập
  + Lưu trạng thái người dùng
  + Theo dõi hoạt động truy cập
## 3. Lab3
### Tổng quan về DNS:
  + Chuyển đổi tên miền -> địa chỉ IP
    - Ví dụ: `www.google.com` → `142.250.x.x`
  + Các loại DNS server chính:
    - `Recursive Resolver`: nhận truy vấn từ client và tìm câu trả lời
    - `Root Server`: định hướng truy vấn đến TLD server
    - `TLD Server`: quản lý các tên miền cấp cao (.com, .org…)
    - `Authoritative Server`: chứa bản ghi DNS chính xác của domain
  + Cách DNS hoạt động:
    - Quá trình phân giải DNS diễn ra theo các bước:
    - Trình duyệt gửi truy vấn DNS
    - Truy vấn được chuyển đến DNS Resolver
    - Resolver lần lượt hỏi:
       + Root DNS Server
       + TLD Server (.com, .net, .org…)
       + Authoritative DNS Server
    - Địa chỉ IP được trả về cho client
  + DNS record là các bản ghi lưu thông tin về domain. Các loại phổ biến gồm:
    - `A Record` → IPv4
    - `AAAA Record` → IPv6
    - `CNAME`: trỏ một domain đến domain khác
    - `MX`: xác định mail server
    - `TXT`: lưu thông tin văn bản (SPF, DKIM, xác thực)
    - `NS`: xác định name server của domain
  + TTL là thời gian một DNS record được lưu trong bộ nhớ cache, giúp cân bằng giữa hiệu suất và tính linh hoạt của hệ thống DNS.
    - TTL thấp: cập nhật nhanh nhưng truy vấn nhiều
    - TTL cao: giảm tải server nhưng cập nhật chậm
# II. HTML, CSS, JS
## HTML


  
