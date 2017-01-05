## Mục lục

##### [Switch Introdution](#1)

##### [Port Security](#2)

-------


![](https://github.com/trung10/CCNA/blob/master/Lv7/Pictures/switch.png)

<a name = "1"></a>
## Switch Introdution

##### Overview

* Hoạt động ở layer 2
* Có khả năng lọc bỏ và đẩy frame ra tất cả các cổng trừ cổng nhận vào
* Có nhiều cổng (so với bright)
* Bộ nhớ đệm khung lớn
* Các port hỗ trợ nhiều tốc độ khác nhau
* Chuyển mạnh nội bộ nhanh chóng 

* Switching modes:

> Cut-throught
> Store-and-frorward
> Fragment-free

##### Hoạt động

* Học MAC của frame đi tới
* Forward frame đảy frame ra cổng dự vào MAC đích
* Chống loops bằng STP



##### Cấu hình

* 

````
SW(config)#interface vlan 1
SW(config)#no shut
SW(config)#ip add 192.168.1.1 255.255.255.0

SW#show mac-address-table
````

<a name = "2"></a>
## Port Security

````
S(config)#interface fa0/1
S(config-if)#switchport mode access
S(config-if)#switchport port-security
S(config-if)#switchport port-security maximum 1 //gioi han host truy nhap vao cong
S(config-if)#switchport port-security mac-address xxxx.xxxx.xxxx
S(config-if)#switchport port-security violation shutdown
````


> S(config-if)#switchport port-security mac-address sticky //switch tự động học n MAC đầu tiên bằng cánh cắm lần lượt n PC

> restrict //là dropframe, phát syslog

> protect //là dropframe, không syslog