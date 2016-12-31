## Mục lục

##### [Switch Introdution](#1)

##### [Port Security](#2)

-------


![]()

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




