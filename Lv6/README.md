## Mục lục

##### [Telnet](#1)

##### [CDP](#2)

##### [SSH](#3)

-----------

<a name = "1"></a>
## Telnet

##### Overview


* Giao thức cấu hình từ xa
* Dùng giao thức TCP, port 23
* Giao thức ở tầng Applicatin

* Điều kiên

> Ping được 2 router à mở cổng vty

##### Cấu hình

> Router(config)#line vty 0 4
> Router(config-line)#passwork xxx
> Router(config-line)#login

<a name = "2"></a>
## CDP (Sisco Discovery Protocol)

##### Overview

* Giúp router có thể tìm hiều thông tin về láng riềng của mình của mình

* Chạy trên thiết bị sisco

* L2

* Cho biết

> Hostname, Local-interface cổng đấu với láng riềng, cổng láng riềng đấu với mình, dòng của router láng riềng
> IOS của láng riềng, IP láng riềng, cho biết láng riềng là router hay switch, có chạy giao thức IGMP

##### Cấu hình

> Router#show cdp neighbor
> Router#show cdp neighbor detail (xem cho tiết)
> Router#show cdp entry *
> Router(config)#no cdp run
> Router(config-if)#no cdp enable

<a name = "3"></a>
## SSH 

* Tương tự như telnet nhưng có mã hóa

##### Cấu hình

> Router(config)#ip domain-name xxx.com //quản lý
> Router(config)#username cisco passwork xxx
> Router(config)#crypto key generate rsa
> Router(config)#line vty 0 4
> Router(config-line)#login local
> Router(config-line)#transport input ssh telnet

