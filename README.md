## Mục lục

##### [Mạng căn bản](#1)

##### [Mô hình OSI](#2)

* [Physical Layer](#3)
* [Data-Link Layer](#4)
* [Network Layer](#5)
* [Transport Layer](#6)
* [Session layer](#7)
* [Presentation layer](#8)
* [Application layer](#9)

<a name = "1"></a>
## Mạng cơ bản

##### Chia sẽ tài nguyên

* Data và applications
* Resources (Tài nguyên mạng như máy in)
* Network storage (Lữu trữ)
* Backup devices (Thiết bụ dự phòng)

##### Network User applications(Ứng dụng người dùng)

* E-mail
* Web brower
* Instant messaging (Chát tức thời)
* Collaboration (Ứng dụng làm việc tập thể)
* Databases

##### Các đặc tính

* Speed
* Cost
* Security
* Availability (khả dụng)
* Scalability (Tính mở rộng)
* Reliability (độ tin cậy)
* Topology

##### Đấu nối

* Full-mesh tất cả các điểm đều đều được nối với nhau, tính dự phòng cao nhưng đắt
* partial-mesh Chỉ nối những điểm quan trọng được nối đến tất cả còn lại

<a name = "2"></a>
## Mô hình OSI (Open System Interconnection)

<a name = "3"></a>
##### Physical

* Là vật lý, như dây điện
* Truyền bits trong môi trường vật lý

<a name = "4"></a>
##### Data-Link

* Thiết lập và kết thúc liên kết: thiết lập và kết thúc liên kết hợp lý giữa hai nút
* Kiểm soát lưu lượng truy cập khung: yêu cầu nút truyền "trở lại" khi không có bộ đệm khung nào
* Trình tự khung: truyền/nhận khung tuần tự
* Báo nhận khung: cung cấp/nhận báo nhận khung. Phát hiện và khôi phục từ lỗi xảy ra trong lớp vật lý bằng cách truyền lại khung không được báo nhận và xử lý nhận khung trùng lặp
* Đặt giới hạn khung: tạo và nhận diện ranh giới khung
* Kiểm tra lỗi khung: kiểm tra khung đã nhận xem có toàn vẹn không
* Quản lý truy cập phương tiện: xác định khi nút "có quyền" sử dụng các phương tiện vật lý


<a name = "5"></a>
##### Network

* Định tuyến. Tìm đường đi tối ưu
* Ánh xạ địa chỉ vật lý logic: dịch địa chỉ hoặc tên logic thành địa chỉ vật lý
* Điều khiển lưu lượng mạng con: bộ định tuyến (hệ thống trung gian lớp mạng) có thể khiến trạm gửi "giảm tiết lưu" truyền khung khi bộ đệm của bộ định tuyến đầy lên
* Phân mảnh khung: nếu phân mảnh này xác định rằng kích thước đơn vị truyền tối đa (MTU) của bộ định tuyến hạ lưu nhỏ hơn kích thước khung, bộ định tuyến có thể phân mảnh khung để truyền và kết hợp lại tại trạm đích

<a name = "6"></a>
##### Session

* Thiết lập, duy trì giải phóng các kết nối End-to-End
* Lớp truyền tải đảm bảo rằng thư được gửi thành công, theo thứ tự và không có mất mát hay trùng lặp. Nó giúp giảm mọi mối lo ngại cho các giao thức ở lớp cao hơn liên quan đến truyền dữ liệu giữa chúng và các giao thức ngang hàng
* Cung cấp các cơ chế sữ lỗi tin cậy, dò lỗi tin cậy, phục hồi thông tin

<a name = "7"></a>
##### Transport

* Thiết lập, bảo trì và kết thúc phiên: cho phép hai quy trình ứng dụng trên các máy khác nhau thiết lập, sử dụng và kết thúc kết nối, được gọi là phiên
* Hỗ trợ phiên: thực hiện các chức năng cho phép các quy trình này giao tiếp qua mạng, thực hiện bảo mật, nhận dạng tên, đăng nhập, v.v

<a name = "8"></a>
##### Presentation

* Dịch mã ký tự: ví dụ: ASCII thành EBCDIC
* Chuyển đổi dữ liệu: thứ tự bit, CR-CR/LF, điểm nổi nguyên, v.v..
* Nén dữ liệu: giảm số lượng bit cần được truyền trên mạng
* Mã hóa dữ liệu: mã hóa dữ liệu cho mục đích bảo mật. Ví dụ: mã hóa mật khẩu

<a name = "9"></a>
##### applications

* Giao tiếp trực tiếp với người dùng, cung cấp các ứng dụng mạng các dịch vụ mạng cho người dùng
* Cung cấp xác thực người dùng




