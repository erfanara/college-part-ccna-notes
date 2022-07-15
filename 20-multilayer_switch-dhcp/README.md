# Multilayer switch

- چرا به جای روتر از مولتی لایر سوییچ استفاده می کنیم؟
	+ دلایل اقتصادی (قیمت حساب شده برای هر پورت)

![](../_resources/swappy-20220715-093803.png)

![](../_resources/inter-vlan-routing-example-1-89937701.png)


# router on stick scenario:

![](../_resources/swappy-20220715-100808.png)

- در مواقعی که ۲ تا vlan داریم و می خواهیم به هر نحوی که شده آنها را به هم متصل کنیم می توانیم از این سناریو کمک بگیریم
	
## router on stick with one port using sub-interfaces

![](../_resources/swappy-20220715-102055.png)
	
- در این حالت با استفاده از دو sub-interface در روتر و با استفاده از مشخص کردن encapsulation dot1q برای sub-interface ها، می توانیم فقط با استفاده از یک اینترفیس همان سناریو قبلی را پیاده سازی کنیم
- فقط باید توجه کرد که اینترفیس واسط بر روی مد trunk قرار بگیرد
- `(config-subif)# encap dot1q 10`
- در این سناریو پهنای باند ما بین دو ویلن نصف می شود



---
- جای که ۲ توسط ، لایه ۳ شکسته شود دیگر vlan ها متصل نخواهند بود ، زیرا روتر در حالت عادی هیچ درکی از vlan ها ندارد
	![](../_resources/swappy-20220715-102917.png)
---


# application of multilayer switch


# DHCP
- چرا باید آی پی داشته باشیم؟ اگر آی پی نداشته باشیم نمی توانیم حتی arp کنیم

- udp port 67,68
	+ 67 -> server
	+ 68 -> clients
	
- DORA:
	+ Discover
	+ Offer
	+ Request (به من این آی پی را بده)
	+ Ack (DHCP options)

	![](../_resources/10674iE1E5DE27B1F07D63-3244093833.jpg)

	![](../_resources/maxresdefault-380756527.jpg)
	
	
- 