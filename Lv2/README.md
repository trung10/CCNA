## Mục lục

##### [TCP/IP](#1)

##### [Ethernet lan](#2)

##### [Cabing](#3)

<a name = "1"></a>
## TCP/IP

##### Mô hình

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/TCP-IP-Model.png)

* Mô hình OSI chia làm 4 tầng, có thể tham chiếu đến mô hình OSI như sau:

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/OSI-TCP-IP2.jpg)

##### Transport (giao thức UDP và TCP)

* Ghép phiên truy nhập của các ứng dụng trên một đường truyền duy nhât
* Phân mảnh dữ liệu từ data thành segmen
* Điều khiểu ngược, gửi gói tin một cánh hợp lý hơn, một số giao thức mới hỗ trợ
* Connection-orientid (truyền hướng kết nối) thiết lập kết nối rồi truyền dữ liệu, một số giao thức sử dụng như TCP
* Reliability (truyền tin cậy) một số giao thức mới có

##### Giao thức UDP (User Datagram Protocol)

* Thuộc tầng transport của OSI và TCP/IP
* Truy nhập vào lớp network khô cần cớ chế kiểm tra lỗi hay báo nhập
* Connectionless protocol không tạo kênh kết nối
* Best-effort 
* Không có cơ chế phục hồi dữ liệu

* Cấu trúc

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/udppacket.gif)

##### TCP

* Thuộc tâng transport 
* Kết nối với lớp mạng
* Connection-orientid 
* Full-duplex mode (có thể truyền và nhan cùng một thời điểm)
* Cung cấp cơ chế kiểm tra lỗi
* Đánh số thứ tự
* Acknowledgement of receipt (cơ chế bóa nhận)
* Phục hồi dữ liệu

* Cấu trúc

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/TCP_UDP_headers.JPG)

* Three-Way Handshake (Bắt tay 3 bước)

> 1.SYN: các chương trình máy con (ví dụ yêu cầu từ browser, ftp client) bắt đầu connection với máy chủ bằng cách gửi một packet với cờ "SYN" đến máy chủ.
SYN packet này thường được gửi từ các cổng cao (1024 - 65535) của máy con đến những cổng trong vùng thấp (1 - 1023) của máy chủ. Chương trình trên máy con sẽ hỏi hệ điều hành cung cấp cho một cổng để mở connection với máy chủ. Những cổng trong vùng này được gọi là "cổng máy con" (client port range). Tương tự như vậy, máy chủ sẽ hỏi HĐH để nhận được quyền chờ tín hiệu trong máy chủ, vùng cổng 1 - 1023. Vùng cổng này được gọi là "vùng cổng dịch vụ" (service port).
Ví dụ (mặc định):

* Web Server sẽ luôn chờ tín hiệu ở cổng 80 và Web browser sẽ connect vào cổng 80 của máy chủ.
* FTP Server sẽ lắng ở port 21.

Ngoài ra trong gói dữ liệu còn có thêm địa chỉ IP của cả máy con và máy chủ.

> 2.SYN/ACK: khi yêu cầu mở connection được máy chủ nhận được tại cổng đang mở, server sẽ gửi lại packet chấp nhận với 2 bit cờ là SYN và ACK.
SYN/ACK packet được gửi ngược lại bằng cách đổi hai IP của server và client, client IP sẽ thành IP đích và server IP sẽ thành IP bắt đầu. Tương tự như vậy, cổng cũng sẽ thay đổi, server nhận được packet ở cổng nào thì cũng sẽ dùng cổng đó để gửi lại packet vào cổng mà client đã gửi.
Server gửi lại packet này để thông báo là server đã nhận được tín hiệu và chấp nhận connection, trong trường hợp server không chấp nhận connection, thay vì SYN/ACK bits được bật, server sẽ bật bit RST/ACK (Reset Acknowledgement) và gởi ngược lại RST/ACK packet.
Server bắt buộc phải gửi thông báo lại bởi vì TCP là chuẩn tin cậy nên nếu client không nhận được thông báo thì sẽ nghĩ rằng packet đã bị lạc và gửi lại thông báo mới.

> 3.ACK: khi client nhận được SYN/ACK packet thì sẽ trả lời bằng ACK packet. Packet này được gởi với mục đích duy báo cho máy chủ biết rằng client đã nhận được SYN/ACK packet và lúc này connection đã được thiết lập và dữ liệu sẽ bắt đầu lưu thông tự do.
Đây là tiến trình bắt buộc phải thực hiện khi client muốn trao đổi dữ liệu với server thông qua giao thức TCP. Một số thủ thuật dựa vào đặc điểm này của TCP để tấn công máy chủ (ví dụ DOS).

<a name = "2"></a>
## Ethernet lan

##### Local Area Network

* Chạy ở lớp 2 trở xuống

##### Các thành phần cơ bản

* Máy tính

* Các kết nối mạng như card mạng, dây dẩn

* Thiết bị mạng như routers, switchs

* Giao thức mạng

##### Chức năng

* Chia sẽ dữ liệu, ứng dụng

* Chia sẽ tài nguyên

* Cung cấp đường kết nối đến một mạng khác

##### CSMA/CD (Đa truy nhập cảm bến sóng mạng dò được xung đột)

![11](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/19583.png)

> Carrier sense - điều này được hiểu như “nghe trước khi nói”. Một máy chuẩn bị truyền một frame đi trước tiên nó nghe xem đối tượng nhận hiện thời đang dỗi và có thể đáp ứng quá trình truyền tin.

> Talk if quiet - Được hiểu như chỉ nói khi đang im lặng, nếu hệ thống lỗi nó sẽ lặp lại lần sau cho đến bao giờ nó kiểm tra thấy hệ thống dỗi nó bắt đầu truyền tin

> Collision - Một sung đột xảy ra có nghĩa là sự vượt quá điện áp trên cable truyền. Một xung đột xảy ra bởi hai đối tượng cùng truyền tin trong một thời điểm nếu xảy ra vấn đề này cả hai frames sẽ phải truyền lại.

> Collision detection - nếu một đối tượng phát hiện ra xung đột trong quá trình truyền nó sẽ dừng lại đợi đến khi hệ thống không còn xung đột nó mới truyền gói tin.

> Backoff – sau một xung đột, một đối tượng sẽ đợi sau một khoảng thời gian nhất định được gọi là backoff, sau thời gian backoff này hệ thống sẽ kiển tra lại và với thời gian backoff được lấy ngẫu nhiên dựa trên thuật toàns backoff. Nó trống lại toàn bộ các đối tượng yêu cầu truyền tin trong lúc đang xảy ra xung đột.


##### Cấu trúc Ethernet frame

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/ethernet-frame.png)

##### Địa chỉ MAC

* Là dãy 48 bits

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/mac-address.png)

* OUI định danh cho nhà sản xuất

##### Cánh truyền thông

* Unicast (1 - 1)
* Broadcast (tất cả)
* Multicast (một nhóm)

<a name = "3"></a>
## Cabing

##### Các loại chuẩn

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/cab1.jpg)

* 10 Base-T trong đó: 10 là tốc độ MB/s, T viết tắt của Twisted-Pair xoắn đôi
* UTP (Unshield Twisted Pair) Cáp xoắn đôi không có vỏ bảo vệ
* STP (Shield Twisted Pair) cáp có vỏ bảo vệ

##### Bấm cáp

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/cab2.jpg)

* Cáp thẳng là 2 đầu bấm chuẩn A hết hoặc B hết
* Cáp chéo 1 đầu A một đầu B

* Để dễ nhớ ta chai làm 2 nhóm

> Nhóm 1: switchs và Hub

> Nhóm 2: còn lại

* Cùng nhóm chéo khác nhóm thẳng

##### Cáp đấu nối trong mạng WAN

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/cab3.jpg)

* Dùng cab serial 
* Phía trên là cổng WIC-1T của router và đầu cáp DB-60

##### Cáp console

* Dùng để cấu hình





