## Mục lục

##### [IP Header](#1)

##### [Cấu trúc IP Address](#2)



<a name = "1"></a>
## IP Header

![](https://github.com/trung10/CCNA/blob/master/Lv3/Pictures/ip-header-2.png)

* Version cho biết giao thức đang chạy ở phiên bản nào
* Header Length là chiều dài của header
* Service Type là sử dụng trong QoS bào đảm chất lượng dịch vụ
* Packet Length chiều dài tổng cộng của gói tin
* Identification , Flag và Flag Offset dùng để phân mảnh gói tin khí nó quá lớn
* Time to Live chống loop 
* Protocol cho biết giao thức nào của lớp trên
* Checksum kiểm tra lỗi
* Source Address nguồn
* Destination Address đích đến
* Option đẻ cho nhà sản xuất chèn thêm các tính năng
* Padding chèn vào option cho đủ 4 Byte

<a name = "2"></a>
## Cấu trúc IP Address

![](https://github.com/trung10/CCNA/blob/master/Lv3/Pictures/IPv4.png)

##### Lưu ý

* Các bit phần mạng không được phép đồng thời bằng 0
* Nếu các bit host bằng khồng thì đây là địa chỉ mạng
* Nếu tất cả các bit host bằng 1 thì đây là địa chỉ quảng bá (broadcast)

##### Các lớp mạng

![](https://github.com/trung10/CCNA/blob/master/Lv3/Pictures/DiaChiIP2.jpg)

> 127.0.0.0 để làm mạng loopback

<a name = "3"></a>
## Địa chỉ Broadcast

##### Local Broadcast (255.255.255.255)

* Gửi đến tất cả các mạng của mình

##### X.X.X.255

* Gửi đến tất cả các host thuộc mạng X.X.X.0

## Địa chỉ private và Public

*  Private Sử dụng trong mạng LAN được dùng đi dùng lại
* Public được sủ dụng cho môi trường internet

* Dải địa chỉ dùng lam private

> Lớp A: 10.x.x.xuất
> Lớp B: 172.16.x.x đến 172.31.x.x
> Lớp C: 192.168.x.x

* Công nghệ NAT để chuyển private sang public
> ý nghĩa là để bỏ tồn địa chỉ IP

## Subnet-mask

* Để máy tính xác định được địa chỉ mạng của một địa chỉ ip

* ví dụ:

> 192.168.1.2 Subnet-mask 255.255.255.0 thì mày tính sẽ biết được địa chỉ này thuộc mạng 192.168.1.0 bằng cánh and 2 giá trị đó




