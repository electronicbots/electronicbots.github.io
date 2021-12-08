---
title: Persistence For Red Teamers
author: Z0ldyck
date: 2021-12-09 18:32:00 -0500
categories: [Blogging, Tutorial]
tags: [Persistence]
---

## What is Persistence?

<html>
<div dir="rtl" align="right">
خلونا في البداية نتفق ان مترجم قوقل هو الافضل هذه ترجمة معنى الكلمة:
</div>
</html>

![](../../images/persistence/5.png)


<html>
<div dir="rtl" align="right">
طيب نرجع لموضوعنا بختصار هي عبارة عن طرق نستخدمها عشان نحافظ على وصلونا لجهاز معين وما نضطر نستهدف مستخدم مرة ثانية عشان نوصل لجهازه. الطرق الي رح اذكرها هي طرق انا استخدمتها في اخر كم انقيجمنت.
</div>
</html>

## Windows Accessibility Features

<html>
<div dir="rtl" align="right">
هذه خدمة يقدمها نظام وندوز تساعد ذوي الأحتياجات الخاصة على التعامل مع الجهاز وللأسف نقدر نستغلها لصالحنا.
</div>
</html>

### Sticky Keys

<html>
<div dir="rtl" align="right">
عمركم ضغطتم على ال shift اكثر من مرة وطلعت لكم هذه الرسالة:
</div>
</html>

![](../../images/persistence/6.png)

<html>
<div dir="rtl" align="right">
أول حاجة تسويها تروح هنا 
</div>
</html>

```
C:\Windows\System32
```

<html>
<div dir="rtl" align="right">
رح تغير اسم sethc.exe الى اي حاجة ثانية وبعدين انسخ cmd.exe وعدل على الاسم وخليه sethc.exe رح تنتهي بشي قريب من هذا: 
</div>
</html>

![](../../images/persistence/3.png)

<html>
<div dir="rtl" align="right">
غالبا رح تضطر تغير ال Owner الخاص ب sethc.exe وتخليه اليوزر الي انت واصل له
</div>
</html>


![](../../images/persistence/1.png)


![](../../images/persistence/2.png)

<html>
<div dir="rtl" align="right">
الأن اذا جيت تسجل دخول اضغط ال shift أكثر من مرة ورح تطلع لك cmd.exe
</div>
</html>

![](../../images/persistence/4.png)


<html>
<body>
<iframe src="https://giphy.com/embed/1236TCtX5dsGEo" width="480" height="480" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/ryan-gosling-clap-university-1236TCtX5dsGEo"></a></p>
</body>
</html>


![Alt Text](https://giphy.com/embed/1236TCtX5dsGEo)
