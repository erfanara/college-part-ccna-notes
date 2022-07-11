---
title: 12-Routing-RIP
updated: 2022-06-21 17:33:10Z
created: 2022-06-16 09:33:35Z
---

# cmds
- `show ip route`


# 
![e7296d501d0af72fb87ab6e5a35a51f7.png](../_resources/e7296d501d0af72fb87ab6e5a35a51f7.png)
- دو کامپیوتر پایین همدیگر را می توانند پینگ بگیرند اگر gateway برای آنها ست شده باشد، زیرا در جدول روتنیگ R2 ، روت های مورد نیاز وجود دارد
![fa7652a24ee80b242933b6a116040ffa.png](../_resources/fa7652a24ee80b242933b6a116040ffa.png)

<div dir="auto" align="right" style="text-align: right"> در هنگام پینگ گرفتن ،وقتی پکت icmp به gateway می رسد، روتر از آنجایی که قرار است به یکی از شبکه های local خود پکت را ارسال کند در نتیجه مک گیرنده را arp می کند.</div>

-برای شبکه های directly connected هیچ کاری نیاز نیست بکنیم و روت بنویسیم

- 
![ef0ff243803fbef78212fbe2ca23a054.png](../_resources/ef0ff243803fbef78212fbe2ca23a054.png)
- وقتی آیپی 172.17.12.1 را روتر R2 پینگ می گیرد ،آیا نیاز دارد که بوسیله arp مک آدرس R1 را بدست بیاورد؟
	- نه زیرا ارتباط بین دو روتر از نوع serial است و پروتکل لایه ۲ آنها از نوع p2p می باشد (hdlc)
- route summerization
- این متریک است:

![3930f17beb9617b78e046326e0245b31.png](../_resources/3930f17beb9617b78e046326e0245b31.png)

و کنار آن عدد 2 درواقع A.D است ، وقتی static route می نویسیم می توانیم A.D را فقط مشخص کنیم.

- روش پینگ کردن از روتر با عوض کردن source ip پکت ها:

![f92cd6a79e20da88f6510a6fe232d4be.png](../_resources/f92cd6a79e20da88f6510a6fe232d4be.png)

![3ca48023f5861d24a403f5d74d7aa869.png](../_resources/3ca48023f5861d24a403f5d74d7aa869.png)

- اگر در هنگام پینگ کردن در روتر ، source ip مشخص نکنیم آنگاه خودش source ip را آی پی اینترفیسی که قرار است از آن پکت ها خارج شوند می گذارد

# dynamic routing protocols
-

# TODO: RIP


# quests
- فرق next hop route و interface route چیست؟
- سناریو را در پکت تریسر ویندوز ارسال کنید