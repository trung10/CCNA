## ** ► Câu hỏi ôn tập : **

##### [1. So sánh 2 kiểu kết nối: Reliable vs Best-Effort](#1)
##### [2. Tìm các số hiệu port dịch vụ của các protocol: FTP, Telnet, HTTP, DNS (TCP & UDP), TFTP, SNMP.](#2)
##### [3. Mạng Ethernet là gì? Kể tên các đặc trưng kỹ thuật của công nghệ mạng này.](#3)
##### [4. Địa chỉ sau là địa chỉ gì, qua đó bạn biết những thông tin gì (cụ thể): e8-94-f6-4a-55-3c](#4)
##### [5. Có mấy chuẩn bấm cáp cho đầu cáp RJ-45. Kể tên thứ tự màu sắc ứng với mỗi chuẩn.](#5)

------------

<a name = "1"></a>
##### 1. So sánh 2 kiểu kết nối: Reliable vs Best-Effort

![](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/reliable-vs-best-effort.jpg)

<a name = "2"></a>
##### 2. Tìm các số hiệu port dịch vụ của các protocol: FTP, Telnet, HTTP, DNS (TCP & UDP), TFTP, SNMP.

* FTP 20,21
* Telnet 23
* HTTP 80
* DNS 53
* SNMP 161, 162

<a name = "3"></a>
##### 3. Mạng Ethernet là gì? Kể tên các đặc trưng kỹ thuật của công nghệ mạng này.

* Ethernet là 1 công nghệ mạng cục bộ (LAN) nhằm chuyển thông tin giữa các máy tính với tốc độ từ 10 đến 100 triệu bít một giây (Mbps)

* Ethernet làm việc tại lớp thứ hai trong mô hình OSI (OSI Layers 2) tức tầng data link. Trong tầng data link được chia làm hai tầng khác đó là MAC Layer và Logical Link Control (LLC) Layer. Lớp LLC – 802.2 là một chuẩn giữa lớp địa chỉ MAC và các giao thức thuộc tầng 3 trong mô hình OSI.

* Các thành phần cơ bản:

> Máy tính

> Các kết nối mạng như card mạng, dây dẩn

> Thiết bị mạng như routers, switchs

> Giao thức mạng

* Ethernet CSMA/CD

> Carrier sense - điều này được hiểu như “nghe trước khi nói”. Một máy chuẩn bị truyền một frame đi trước tiên nó nghe xem đối tượng nhận hiện thời đang dỗi và có thể đáp ứng quá trình truyền tin.

> Talk if quiet - Được hiểu như chỉ nói khi đang im lặng, nếu hệ thống lỗi nó sẽ lặp lại lần sau cho đến bao giờ nó kiểm tra thấy hệ thống dỗi nó bắt đầu truyền tin

> Collision - Một sung đột xảy ra có nghĩa là sự vượt quá điện áp trên cable truyền. Một xung đột xảy ra bởi hai đối tượng cùng truyền tin trong một thời điểm nếu xảy ra vấn đề này cả hai frames sẽ phải truyền lại.

> Collision detection - nếu một đối tượng phát hiện ra xung đột trong quá trình truyền nó sẽ dừng lại đợi đến khi hệ thống không còn xung đột nó mới truyền gói tin.

> Backoff – sau một xung đột, một đối tượng sẽ đợi sau một khoảng thời gian nhất định được gọi là backoff, sau thời gian backoff này hệ thống sẽ kiển tra lại và với thời gian backoff được lấy ngẫu nhiên dựa trên thuật toàns backoff. Nó trống lại toàn bộ các đối tượng yêu cầu truyền tin trong lúc đang xảy ra xung đột.

<a name = "4"></a>
##### 4. Địa chỉ sau là địa chỉ gì, qua đó bạn biết những thông tin gì (cụ thể): e8-94-f6-4a-55-3c

* e8-94-f6-4a-55-3c là địa chỉ MAC

* Ta có thể biêt được nó thuộc nhà sản xuất TP-LINK TECHNOLOGIES CO.,LTD nhờ phần OUI e8-94-f6

<a name = "5"></a>
##### 5. Có mấy chuẩn bấm cáp cho đầu cáp RJ-45. Kể tên thứ tự màu sắc ứng với mỗi chuẩn

![aaa](https://github.com/trung10/CCNA/blob/master/Lv2/Pictures/cab2.jpg)



