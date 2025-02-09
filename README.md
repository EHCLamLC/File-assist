1, File và cấu trúc của nó trong Linux
(*) File là gì: 
    - Trong hệ điều hành Linux, tất cả mọi thứ đều được coi là tệp tin, bao gồm cả thư mục, thiết bị phần cứng, tién trình và cả socket. Cấu trúc hệ thống của tệp Linux tuần theo tiêu chuẩn phần cấp (FHS), giúp tổ chức tệp tin một cách có hệ thống và dễ quản lý
(*)  Phân loại file trong Linux
    - Gồm các loại sau: 
    + Regular file: Tệp tin bình thường ( như bình thường)
    + Diretory : Thư mục chứa các file và thư mục khác 
    + Synbolic Link : Liên kết mềm'
    + Character Device : Thiết bị ký tự
    + Socket : Fike đặc biệt dùng để giao tiếp giữa các tiến trình 
    + Named Pipe : Cơ chế giao tiếp với các tiến trình 
(*) Cấu trúc hệ thống thông tệp trong Linux 
  / : Thư mục gốc (root) của hệ thống
  /bin : chứa các lệnh cơ bản như ls, cp, mv, ...
  /boot : chứa các tập tin khởi động như vmlinuz, grub
  /dev : chứa các ổ cứng (/dev/sda) USD, máy in
  /etc : chứa file cấu hình hệ thống
  /home : chứa thư mục của người dùng thông thường
  /lib : chứa thư viện dùng chung cho các chương trình trong /bin và /sbin
  /media : Thue mục mount thiết bị bên ngoài (USD, CD-ROM)
  /mnt : điểm mount tạm thời của thiết bị 
  /opt : Chứa phần mềm cài đặt thêm từ bên ngoài
  /proc : Chứa thông tin hệ thống và tiến trình chạy
  /root : thư mục của user [root]
  /sbin : Chứa các lệnh quản trị hệ thống
  /srv : Chứa các dữ liệu cho các dịch vụ máy chủ(wed sever, ...)
  /sys : Chứa thông tin về phần cứng hệ thống
  /tmp : chứa các file tạm thời
  /usr : Chứa các file thư viện của user 
  /var : Chứa dữ liệu thay đổi liên tục như log, thư.

2, Process trong Linux:
  (*) Process là gì:
  - Process là một chương trình  đang chạy trên hệ thống. Mỗi tiến trình có một Process ID (PID) duy nhất và có thể chạy trên nhiều trạng thái khác nhau trong vòng đời của nó.
  (*) Các trạng thái của của nó
-Running : đang chạy hoặc sẵn sàng chạy
- Sleeping : Đang chờ ngắn hạn
- Stpped : Bị dừng bởi tín hiệu ctrl + z
- Zombie : kết thúc nhưng ctring chưa bị xóa
- Deep sleep : chờ dài hạn

3,User trong Linux
 (*) User gồm có 3 loại chính 
 -Root : Người dùng có quyền hệ thống cao nhất (UID = 0) có thể làm mọi thứ trên hệ thống
 -Regular : Người dùng thông thường, có quyền hạn chế trên hệ thống
 -System User : Được tạo cho các hệ thống dịch vụ 
 (*)group
   Group giúp quản lý quyền truy cập file và thư mục theo nhóm user.
 - các lạo group
 + Primary Group : Nhóm chính của User
 + Supperlementary Group : Nhóm bổ sung mà user có thể thuộc về

4, Phân quyền trong linux
Hệ thống phân quyền trong linux giúp bảo vệ dữ liệu, kiểm soát soát truy cập file và thư mục. dưới đây là cách hoạt động của hệ thống này.
 (*) cấu trúc phân quyền trong Linux
 - 1,1 các loại người dùng
   + Owner : Chủ sở hữu file/ thư mục, (ng tạo ra file)
   + Group : Nhóm người dùng có quyền trên file/ thư mục
   + Orther : Tất cả nhưng người dùng còn lại trên hệ thống
(*) Các loại quyền
r : đọc
w : write
x :thực thi
