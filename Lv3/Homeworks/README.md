##  ► Câu hỏi Ôn tập: **

##### [1. Nếu các khái niệm sau: Địa chỉ mạng, Địa chỉ Broadcast, Địa chỉ Host, Địa chỉ Loopback, Subnet Mask, Default Gateway](#1)

##### [2. Vì sao Phải chia IP? Kiểu chia Subnetting, kiểu chia VSLM là gì? CIDR là gì?](#2)

====================

<a name = "1"></a>
##### 1. Nếu các khái niệm sau: Địa chỉ mạng, Địa chỉ Broadcast, Địa chỉ Host, Địa chỉ Loopback, Subnet Mask, Default Gateway

* Địa chỉ mạng tất cả các bit host = 0 ví dụ: 192.168.1.0/24

* Địa chỉ Broadcast tất cả các bit host = 1 ví dụ: 192.168.1.255/24

* Địa chỉ Host các đị chỉ từ địa chỉ mạng và broadcast 
* Địa chỉ Loopback để kiếm tra tính đúng đắn khi triển khai mạng 172.0.0.1
* Subnet Mask để máy tính AND với địa chỉ IP biết các bit và là host các bit nào là mạng
* Default Gateway là cổng nối vào router

<a name = "2"></a>
##### 2. Vì sao Phải chia IP? Kiểu chia Subnetting, kiểu chia VSLM là gì? CIDR là gì?

* Chia để bảo tồn IPv4 là có hạn tuy nhiên khi lên IPv6 việc chia IP là không thực sự cần thiết

* SUBNETTING:
> cách chia này rất dễ và hoàn toàn không cần nhiều tính toán. Đặc điểm củ phép chia này đó là khi chúng ta chia mạng con ra từ một Major
network nào đó thì tất cả các địa chỉ IP con này đều có chung một subnet. Cụ thể như sau:
ví dụ có major network sau: 192.168.0.0/16
khi chia ra 5 mạng con, thì tất cả mạng con sẽ có cùng một subnet. Cụ thể
ta có thể chia major network này ra 5 mạng con như sau:

192.168.1.0/24

192.168.2.0/24

192.168.3.0/24

* VLSM:
> VLSM, nó là cụm từ viết tắt của: Variable Length Subnet Masking
Cách chia VLSM sinh ra nhằm mục đích tận dụng tối đa số địa chỉ IP
của một major network nào đó.
Đầu tiên, ví dụ ta có địa chỉ này: 192.168.0.0/16
Đây là địa chỉ IP của lớp B. Giả sử ta cần chia Major network này ra làm
5 mạng con như sau:

> Lan 1: 200 host

> Lan 2: 200 host

> Lan 3: 100 host

> Lan 4: 50 host

> Lan 5: 2 host
(chúng ta cần sắp xếp các Lan theo số host từ lớn tới bé, để chia dễ dàng
hơn)

Bắt đầu nhé!

Lan 1: 200 host (2^8 = 256)

Như vậy ta cần mượn 8 bit từ phần net cho phần host.

Địa chỉ IP của Lan 1 sẽ là: 192.168.0.0/24

Lan 2: 200 host cũng tương tự thì mạng này cũng cần mượn  8 bit từ phần
net.

Cho nên địa chỉ IP của Lan 2 sẽ là : 192.168.1.0/24

dư ra 56 IP không đủ cho Lan 3 nên:

Lan 3: 100 host (2^7=128)

như vậy cần mượn 7 bit từ phần net.

địa chỉ của Lan 3 sẽ là: 192.168.2.0/25

Lan 4: 50 host (2^6=64)

cho nên cần mượn 6 bit từ phần net.

Cụ thể, IP của Lan 4 sẽ là: 192.168.2.128/26

Lan 5: 2 host (2^2=4)

cho nên, Lan 5 sẽ có địa chỉ như sau: 192.168.2.192/30

Đó là cách chia IP theo cách VLSM.

* CIDR là kiểu chia lấy bit thêm bit mạng để làm bit host có kiểu chia lớn hơn.


