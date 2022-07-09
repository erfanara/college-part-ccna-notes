---
title: 7-switch
updated: 2022-06-21 17:35:24Z
created: 2022-05-26 11:03:40Z
---

# switch password recovery
 - Mode key ( run switch without config )
 - harder way ...

#
- اینترفیس های روتر ها لایه ۳ ای هستند و می شود روی آنها آی پی ست کرد،
ولی سوییچ ها اینترفیس هایشان لایه۲ هستند و نمی توانند آی پی بگیرند در نتیجه قابل ssh نیستند، ولی باید از vlan برای آنها استفاده کنیم.
-  vlan1 is always exist in switch
-  

# some cmds
- sh ip int 
- sh int
- sh ip int brief
- sh int status
- bandwidth

---
- status for int is up: no shut and cable connected (layer1 is up)
- status down: cable not connected ( layer1 is down)
- status administratively down: int is shut
- protocol : ( layer2 status ) for example if peers dont use same layer2 protocol then protocol is down
- fastEthernet uses ethernet encapsulation by default in layer 2
- fastEthernet : 100, GigabitEthernet: 1000
- 10/40/100/1000/10g

- clock rate in serial and speed is physical parameter and you cant set it on a desirable amount

- if you set a device manualy 10 and another with 100 then their layer2 connection will be down (protocol down)

# switching
- cam table (map ports to macs)
- STP , DTP
- sh mac address-table (clear mac address-table)
- cam table is empty at first , becuase computers dont send anything at first into the network
- hub just broadcast anything 
- icmp: layer3
- unknown unicast flooding (like broadcast)
- in cam table we can have records with the same port and diffrent macs (in cascade scenarios)
- mac flood attack
- mac spoofing attack
- 802.1x protocol for switching security
- dhcp snooping
- we decrease mac address-table aging where we have high mobility like airports.
- # show mac-address-table count
---
- switch interfaces have their uniq mac address 
----
- port security for interface
- # switchport mode access
- # switchport port-security
- port secure down will occure if first violated packet recieced
- این جور تنطیمات پورت سکیوریتی می تواند کار سختی باشد زیرا خیلی اوقات همه چیز ثابت نیست
- # switchport port-security maximum (can be used for hubs and untrusted networks) (useful for mac flooding attack prevention)
- # switchport port-security violation (shutdown/protect/restrict)

- protect: drop traffic
- restrict: protect + violation count + snmp trap generate

---


- switch1 -- hub -- hub -- switch1 : loop deteted and port will be down by default in cisco switch

- zonebf cisco router
- utm : unified treat management
- waf : webapplication firewall
- ospf
- firewall (frontend + backend + core) 

---

- چگونه در دانشگاه ها از دسترسی کامپیوترها به یکدیگر جلوگیری کرد؟
- pppoe quest

# Quests
- **چگونه تشخیص دهیم سوییچ های ما با کابل کراس یا استریت وصل شدند؟ (با همین کامند ها)**
- **چگونه تشخیص دهیم سوییچ های ما MDI-X ساپورت میکند یا نه؟**
```
sho cont eth f0/2 phy

		Switch# configure terminal
		Switch(config)# interface gigabitethernet1/0/1
		Switch(config-if)# speed auto
		Switch(config-if)# duplex auto
		Switch(config-if)# mdix auto
		Switch(config-if)# end
```
- ***چیکار کنیم تا اگر پورت سیکوریتی پورت را داون کرد ، آتومات پورت بعد از مدتی روشن شود بار دیگر. این قضیه فقط مربوط به پوت سکیوریتی نیست***

- **switchport port-security mac-address sticky?**
	- This command is executed in interface configuration mode and configures the port to dynamically learn the MAC address and automatically configure the MAC address as a static MAC address associated with the port.

