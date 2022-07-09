---
title: 14-OSPF
updated: 2022-06-21 18:17:07Z
created: 2022-06-21 17:31:44Z
latitude: 36.26046230
longitude: 59.61675490
altitude: 0.0000
---

# OSPF => Open shortest path first
- A.D = 110
- از قوانین همسایگی پیروی می کند
- برای همسایه شدن Hello می فرستد مثل EIGRP
- پکت های Hello را multicast می کند مثل EIGRP
	- 224.0.0.5
	- 224.0.0.6
- از ساختار های area بندی استفاده می کند که با Autonomous System در EIGRP فرق دارد 
- VLSM را کامل ساپورت میکند ؟
- محاسبه metric => فقط bandwitdh
- inceremental update, trigger update
- مدل area در OSPF با AS در EIGRP هیچ شباهتی به هم ندارند
- در شبکه های با چند area حتما باید area 0 را داشته باشیم ولی در شبکه های تک area الزامی نیست
- OSPF در شرایط همسایگی کمی پیچیده تر عمل می کند
- برای مثال:
![4efe1640cbfedb5dd2ca7d44480fa4f6.png](../_resources/4efe1640cbfedb5dd2ca7d44480fa4f6.png)
روت های مربوط به area 10 در area 0 ریخته نمی شوند زیرا ABR ما به area 0 وصل نیست ، مگر اینکه virtual link بزنیم


# scenario 1
- TODO