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
## 1. HTML, CSS
### Cấu trúc tối thiểu của một trang HTML gồm các thẻ
``` HTML
<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
</head>
<body>
  <h1>This is a Heading</h1>
  <p>This is a paragraph.</p>
</body>
</html>

```
- `Element` thường có dạng: `<tagname>` nội dung `</tagname>`.
- `Attribute` là thông tin bổ sung nằm trong thẻ mở: `name="value"` (vd: href, src, alt, style, …).
VD:
```HTML
<a href="https://thachotoi.com">Toilagay</a>
<img src="khoc.jpg" alt="Khóc">
```
-
  + 
- Để trình bày nội dung trên HTML ta có thể sử dụng các thẻ sau:
  + Tiêu đề: `<h1>…<h6>`
  + Đoạn văn: `<p>`
  + Định dạng: `<b> <strong> <i> <em> <mark> <small> <del> <ins> <sub> <sup>`
  + Trích dẫn: `<blockquote> <q> <cite> <abbr>`
  + Comment: `<!-- ... -->`
  + Tables: `<table> <tr> <th> <td>`
  + Lists:
    - Không thứ tự: `<ul><li>…`
    - Có thứ tự: `<ol><li>…`
- Ngoài ra còn có các thẻ bố cục:
  + `<div>` dùng gom khối nội dung.
  + `class, id`.
  + `<iframe>` nhúng trang khác.
### Form HTML
- Cấu trúc của 1 form: `<form>...</form>`
- `<form>` có thể chứa một hoặc nhiều phần tử biểu mẫu sau:
  + `<Label>`: `<label for="username">Tên đăng nhập:</label>`, for phải trùng với id của input.
  + `<select>`: tạo danh sách chọn.
    
  + `<option>`: định nghĩa một tùy chọn có thể được chọn trong <select>, sử dụng multiple để chọn được nhiều hơn 1 giá trị.
    
  + `<button>`: Tạo nút bấm. Có thể dùng thay cho `input type="submit"`.
    
  + `<input>`: `<input type="text" id="username" name="username">`

| Type       | Công dụng                     |
| ---------- | ----------------------------- |
| `text`     | Nhập chữ                      |
| `password` | Nhập mật khẩu                 |
| `email`    | Email                         |
| `number`   | Số                            |
| `date`     | Ngày                          |
| `radio`    | Chọn 1                        |
| `checkbox` | Chọn nhiều                    |
| `file`     | Upload file                   |
| `submit`   | Gửi form                      |

- Form Attributes:
  + Method `POST` và `GET`
  + `target` là 1 thuộc tính nhưng mà được dùng trong 1 số thẻ HTML nhất định VD: `<form>, <a>, <base>...)`

| Value     | Ý nghĩa                               |
| ----------- | ------------------------------------- |
| `_blank`    | Mở kết quả ở **tab / cửa sổ mới**     |
| `_self`     | Mở ngay **trang hiện tại** (mặc định) |
| `_parent`   | Mở ở **frame cha**                    |
| `_top`      | Mở **toàn bộ cửa sổ**, thoát frame    |
| `framename` | Mở trong **iframe có tên**            |





  


  
