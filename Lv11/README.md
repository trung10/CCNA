## Các lệnh năng cao

> R1(config-router)# passive-interface fa0/0    không cho quảng bá bản tin RIP vào cổng  fa0/0   

> R1(config-router)#redistribute static     Lệnh quảng bá tuyến Static trong bản tin RIP

> R1(config-router)# default-information originate    Lệnh quảng bá tuyến default route trong bản tin RIP

* Chủ động Summary bằng tay khi đã dùng lệnh (R1(config-router)# no auto-summary)

> R1(config)#int s0/0

> R1(config-if)# ip summary-address rip 200.199.48.0 255.255.252.0

> R1(config-if)# ip rip send version 1       R1 sẽ  chỉ gửi  duy  nhất  các  gói  tin Ripv1 qua interface này.

> R1(config-if)# ip rip send version 2      R1 sẽ  chỉ gửi  duy  nhất  các  gói  tin Ripv2 qua interface này.

> R1(config-if)# ip rip receive version 1        R1 sẽ  chỉ nhận duy nhất  các gói  tin Ripv1 qua interface này.

> R1(config-if)# ip rip receive version 2      R1 sẽ  chỉ nhận duy nhất  các gói  tin Ripv2 qua interface này.