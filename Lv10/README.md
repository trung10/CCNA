## RIP

##### [Giao thức định tuyến định tuyến](#1)

##### [RIP và RIPv2](#2)

##### [Cấu hình](#3)

-----------

<a name = "1"></a>
## Giao thức định tuyến định tuyến

* Duy trì các thông tin định tuyến ở xa trong bảng định tuyến của mình

* Sau khi xác định đường đi router có thể chỉ đường thồng qua giao thức "routed protocol"

* 

##### Autonomous system

![](https://github.com/trung10/CCNA/blob/master/Lv10/Pictures/1.jpg)

* AS là tập hợn các mạng chung một sự quản lý về kỹ thuật hay sỡ hữu nào đó (thuộc lớp 3)

* IGPs (Interior Gateway Protocol) là các giáo thức dùng trong 1 AS nào đó

* EGPs (Exterior Gateway Protocol) là các giao thức kết nối các AS với nhau

##### Các trường phái giao thức định tuyến

![](https://github.com/trung10/CCNA/blob/master/Lv10/Pictures/2.jpg)

##### Administrative Distance (AD)

* Khi xuất hiện nhiều giao thức khác nhau chỉ nhiều đương đi khác nhau đi đến cùng một đích, router sẽ dựa vào chỉ số AD nhỏ hơn.

##### Distance Vector (RIP)

* Gửi toàn bộ bảng định tuyến của mình cho láng riềng theo định ký.

* Router tìm được đường đi tốt nhất dựa vào người láng riềng của nó.

* "Metric" định lượng tốt xấu của một đường đi, trong giao thức RIP metric là số node trên đương đi, tối đa là 15.

##### Split Poisoning

* Router nhận được cập nhật định tuyến từ mạng nào thì không được gửi được gửi thông tin định tuyến về mạng đó nữa

##### Route Poisoning

* Khi router có một mạng bị down thì gửi một bảng cập nhật đến router láng riêng.

##### Poison Reverse

* Gửi lại cập nhật y hêt để xác nhận.

##### Hold-Down Timer

* Chờ 1 khoảng thời gian tham gia tính toán

<a name = "2"></a>
##### RIP và RIPv2

![](https://github.com/trung10/CCNA/blob/master/Lv10/Pictures/3.jpg)

<a name = "3"></a>
##### Cấu hình 

* RIP

````
R(config)#router rip
R(config-router)#network network-number
````

* RIPv2

````
R(config)#router rip
R(config-router)#version 2
R(config-router)#network network-number
R(config-router)#no auto-summary
````