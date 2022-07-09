---
title: 6-password-recovery
updated: 2022-06-21 17:37:51Z
created: 2022-05-24 11:13:48Z
latitude: 35.68722153
longitude: 51.41527939
altitude: 0.0000
---

# انواع حافظه 
- rom (mini os for rescue purposes)
- ram (running config)
- nvram (non volatile ram) (startup config)
- flash 


# some cmds
`write`
`copy`
`erase`
`delete`
- remove from nvram
	`write erase`
	
# about mtu and packet fragmentation
- (datagram/segment) -> (packet) -> (frame)
- mtu (for layer 3 : packet)
- ttl


# image flash
`boot system flash`
- cisco campact flash
- rom monitor mode 
- k9 ==> full support
- image versions  


# switch
- spanning-tree portfast  -> tell that interface that connect faster


# password recovery for cisco router
- rommon(break while decompressing in boot)
- confreg (0x2102 default) (0x2142 no nvram load)
- copy startup-config running-config
- you should be in enable mode ...
-  do your job
-  change config-register in global config to default


# Quests
- **کانفیگ ssh**
- **password revocey for switch (has some diff with router password recovery)**
- 