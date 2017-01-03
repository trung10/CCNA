## Mục lục

##### [Static route](#1)



-----------

<a name = "1"></a>
## Static route

##### Định tuyến

* Định tuyến là tìm ra đường đi tối ưu trong mạng

* Để định tuyến cần

> Biết địa chỉ đích
> Cần phải biết router kế tiếp trong đường đi
> Biết các đường đi có thể đến đích để phòng sự cố
> Chọn đường đi tối nhât
> Duy trì và giữ thông tin định tuyến này

##### Bảng định tuyến

![](https://github.com/trung10/CCNA/tree/master/Lv5/Pictures/1.png)

* Câu lệnh

> Router#show ip route

* Tự điền tay vào bảng định tuyến thì đó là định tuyến tĩnh

##### Cấu hình

> Router(config)# ip route network [mask] {addess | interface} [distance] [permanent]


* Ví dụ

> r(config)#ip route network 255.255.255.0 192.168.1.0 s0/0



