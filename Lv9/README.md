## Mục lục

##### [ICMP](#1)

##### [ARP](#2)

##### [DHCP](#3)

-----------

<a name = "1"></a>
## ICMP (Internet Control Message Protocol)

* Kiểm tra các kết nối lớp 3

##### ping

* Reply from 192.168.3.1 t<1 ms TTL=253


* Request timed out


* Reply from 192.168.13.3 Destimation host unreachible

> Time to Live chống loop, khi qua một router thì TTL sẽ giảm đi một đơn vị, nếu một gói tin có TTL = 0 thì router sẽ bỏ gói tin đó


<a name = "2"></a>
## ARP

* map địa chỉ mạng IP với địa chỉ MAC

````
arp -a

show arp //xem cấu hình trên router
````


<a name = "3"></a>
## DHCP

* Cấp phát địa chỉ cho client

##### Cấu hình

````
R(config)#sercive dhcp
R(config)#ip dhcp pool ABC
R(dhcp-config)#network 192.168.1.0 255.255.255.0
R(dhcp-config)#default-router 192.168.1.1
R(dhcp-config)#dns-sever 8.8.8.8
R(dhcp-config)#lease 0 1 0 // ngay gio phut

R(config)#ip dhcp excluded-addess 192.168.1.1//tranh cap dia chi nay
````


