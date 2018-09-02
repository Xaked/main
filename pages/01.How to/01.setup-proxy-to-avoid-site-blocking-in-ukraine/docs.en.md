---
title: 'Setup proxy to avoid site blocking in Ukraine'
taxonomy:
    category: docs
visible: true
---

### The first step is to make sure that the provider does not block dns resolve blocked sites

For example, in windows we can do this by entering this command **nslookup yandex.ru 8.8.8.8**.

We are using google public dns for tesing. If you seeing response like on first image than you can go to next step.  
![DNS resolve OK](https://i.imgur.com/CAOC2uB.png)

If your response looks like this, then you need to use another method.  
![DNS resolve ERROR](https://i.imgur.com/MrM9Osf.png)

### If all is good then we need to setup google public dns resolver as default in our system

For example in windows 10:

![1](https://i.imgur.com/INnxxFg.png)
![2](https://i.imgur.com/NhOxrFG.png)
![3](https://i.imgur.com/yqozYhd.png)

### Now setup proxy with automatic pac script

In windows 10:

Press on keyboard **Win + R** and input **inetcpl.cpl**

![1](https://i.imgur.com/ebts2hC.png)

In proxy address you can use one of this:
1. Zaborona.help proxy.pac file [https://zaborona.help/proxy.pac](https://zaborona.help/proxy.pac)
1. Our proxy file [https://sc.xaked.com/js/unblock/r/ua.pac](https://sc.xaked.com/js/unblock/r/ua.pac)

![2](https://i.imgur.com/thZF29W.png)

Last step is to clear dns resolver cache. Write in console this command **ipconfig /flushdns**

![ipconfig](https://i.imgur.com/Ovrh0eA.png)

Restart your applications or your pc, and try to use blocked websites.

>We are using proxy sites provided by Zaborona.help