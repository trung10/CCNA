## Các lệnh cấu hình cơ bản

##### [Các mode](#1)
##### [Enable passwork](#2)
##### [Kiểm tra cấu hình](#3)
##### [Console-passwork](#4)
##### [Mã hóa passwork](#5)
##### [Đổi tên](#6)
##### [Banner mode](#7)
##### [Show các cổng](#8)
##### [Đặt IP cho cổng](#9)
##### [Lưu cấu hình](#10)
##### [Xóa cấu hình trong NVRAM](#11)




-------------

<a name = "1"></a>
##### Các mode

* User EXEC mode mode (Router>)
* Previlege mode (Router#)
* Global configuration (Router(config)#)

> Ra ngoài dùng lệnh exit, end, disable

<a name = "2"></a>
##### Enable passwork

Router(config)# enable passwork xxx


<a name = "3"></a>
##### Kiểm tra cấu hình

Router#show running-config

<a name = "4"></a>
##### Console-passwork

Router(config)#line console 0

Router(config-line)#passwork xxx

Router(config-line)#login

<a name = "5"></a>
##### Mã hóa passwork

Router(config)#service passwork-encrypion

<a name = "6"></a>
##### Đổi tên

Router(config)#hostname ten

<a name = "7"></a>
##### Banner mode

Router(config)#banner motd #khẩu hiệu#

<a name = "8"></a>
##### Show các cổng

Router#show ip interface brief

<a name = "9"></a>
##### Đặt IP cho cổng

Router(config)#interface s0/0

Router(config-if)#no shutdown

Router(config-if)#ip address 192.168.1.1 255.255.255.0

Router(config-if)#description "mô tả"

<a name = "10"></a>
##### Lưu cấu hình

Router#copy running-config startup-config

<a name = "a"></a>
##### Xóa cấu hình trong NVRAM

Router#erase startup-config

Router#reload //khởi động lại router