# Lỗ hổng tải tệp là gì

- Là khi máy chủ web cho phép người dùng tải tệp lên hệ thống của mình mà không xác thực các thông tin như tên, loại, nội dung, kích thước

# Ản hưởng của lỗ hổng tải tệp

- Ảnh hưởng của lỗ hổng này phụ thuộc vào 2 yếu tố
  - Trang web không xác thực đúng loại, kích thước, nội dung ,... của tệp
  - Những biện pháp giới  nào được áp dụng lên file khi upload thành công
 
  Ví dụ:
- Thư mục lưu trữ: tệp có được giới hạn lưu ở 1 thư mục an toàn thay vi thư mục gốc của website
- Thực thi tệp: nếu là 1 tệp mã nguồn như `.php`, trang web có cho phép tệp đó thực thi kkhông hay chỉ hiển thị nội dung tệp mà không thực thi

 # Khai thác lỗ hổng tải tệp để triển khai web shell 

 - Nếu 1 trang web cho phép tải các tệp ( PHP, Java, Python) lên phía máy chủ, bạn có thể tạo 1 web shell của riêng mình trên máy chủ
 - Sau khi tải lên thành công 1 webshell, về cơ bản bạn có toàn quyền kiểm soát máy chủ ( đọc và ghi tệp tùy ý, trích xuất dữ liệu nhạy cảm,...)
 - Ví dụ, sử dụng dòng lệnh PHP sau để đọc các tệp tùy ý từ hệ thống máy chủ

`<?php echo file_get_contents('/path/to/target/file'); ?>`
`<?php echo system($_GET['command']); ?>`
