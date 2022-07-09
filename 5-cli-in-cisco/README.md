---
title: 5-cli-in-cisco
updated: 2022-07-09 20:04:42Z
created: 2022-05-28 05:34:42Z
latitude: 35.68722153
longitude: 51.41527939
altitude: 0.0000
---

# cli for cisco
1. Console
2. Telnet/ssh
3. AUX (Auxiliary,)
	- عملا فرقی با کنسول ندارد ، برای پشتیبانی است و معمولا به مودم های تلفنی متصل می شود تا در موارد اظطراری  قابل استفاده باشد.

# keywords for search
- switch 2960x
- cisco console cable
- com 
- serial connection 
- rs-232
- microusb mode 
- cisco AUX port
- WIK - NM - HWIK
- combo port (MIkrotik)
- AAA -> Auth - Athorize - Accounting
- Radius
- Active directory
- cisco ise

# 
- login:
	- local (local username/password- clear-type7-secret(md5))
	- AAA
- enable:
	- pass (clear password)
	- secret (md5)
	- اگر جفتش فعال باشد سکرت کار میکند
- 
# some cmds
- sh int status (for switch?)
- if prot line (?)
- no ip domain-lookup
- sh running-config
- do -> can be used when we are not in enable mode


# 
- usermode:
	- Hostname>
- enable mode:
	- Hostname#
- \<CR>:
	- carrier row
- ctrl+shift+6 -> break
- line -> پورت های مدیریتی

# Quests
1. **how to set more than one ip for an interface? (packet tracer does not support this)**
2. encrypt vs hash
3. **set 'Test?cisco' for password (packet tracer does not support this) (ctrl+v)**
4. **how level5 user can access the global config mod?**