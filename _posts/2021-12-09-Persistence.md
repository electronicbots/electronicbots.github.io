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

### Abusing Windows Narrator

<html>
<div dir="rtl" align="right">
ال Narrator في ال windows يقرأ لك الكلام الي موجود بالصفحة وحدة من الأمور الي نقدر نستغلها هي خاصية ال "Feedback-Hub" أول حاجة تسويها هي تفعيلها من الأعدادات: 
</div>
</html>

![](../../images/persistence/7.png)


<html>
<div dir="rtl" align="right">
في ال Narrator settings عدل على "Provide Narrator feedback" وحط له الأختصار الي يناسبك 
</div>
</html>

![](../../images/persistence/8.png)

<html>
<div dir="rtl" align="right">
شغل Registry Editor وروح على ال key الي تحت وسجل اسم الملف الي حاط عليه بالسهم 
</div>
</html>

`Computer\HKEY_CLASSES_ROOT\Local Settings\Software\Microsoft\Windows\CurrentVersion\AppModel\PackageRepository\Extensions\windows.protocol\feedback-hub`

![](../../images/persistence/9.png)

<html>
<div dir="rtl" align="right">
بعدين استخدم هذا الاسم وروح على هذه ال entry:
</div>
</html>

`Computer\HKEY_CURRENT_USER\Software\Classes\<file_name>\Application`

![](../../images/persistence/10.png)

<html>
<div dir="rtl" align="right">
في ملف ال command رح تلقى ملف اسمه DelegateExecute احذفه 
</div>
</html>

![](../../images/persistence/11.png)


<html>
<div dir="rtl" align="right">
بعدين بنفس المكان عدل على ال Default entry وحط فيها الكوماند الي تحتاجه 
</div>
</html>

![](../../images/persistence/12.png)

<html>
<div dir="rtl" align="right">
سوي Lock للحساب واضغط الأختصار الي سجلناه بالبداية ورح تجي لك request للسيرفر:
</div>
</html>

![](../../images/persistence/13.png)

<html>
<div dir="rtl" align="right">
أعتقد واضحة كيف تقدرون تستغلوها لمثلاً meterpreter shell
</div>
</html>

<html>
<body>
<iframe src="https://giphy.com/embed/1236TCtX5dsGEo" width="480" height="480" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
</body>
</html>


## Screensavers

<html>
<div dir="rtl" align="right">
بأختصار اذا ما استخدمت جهازك لمدة معينة رح تضهر لك شاشة سوداء. نقدر نستغلها كالأتي اول شي استخدم هذا الكوماند عشان نعدل على الملف الي رح يشتغل اذا ما تم استخدام الجهاز:
</div>
</html>

`reg add "HKEY_CURRENT_USER\Control Panel\Desktop" /v "SCRNSAVE.EXE" /t REG_SZ /d "cmd.exe" /f`

<html>
<div dir="rtl" align="right">
بعدين رح نعدل على كم ثانية اذا المستخدم ما اشتغل على الجهاز عشان يشغل لنا ال cmd.exe
</div>
</html>

`reg add "HKEY_CURRENT_USER\Control Panel\Desktop" /v "ScreenSaveTimeOut" /t REG_SZ /d "15" /f`

![](../../images/persistence/14.png)

<html>
<div dir="rtl" align="right">
انتضر شوي ورح تطلع لك ال cmd بنفس الوقت خلي ببالك انه في group policy لل screensavers في ال Active Directory
</div>
</html>

### `Demo:`

![](../../images/persistence/screen.gif)

`Leave your computer on, while I am already in ;)`
<html>
<body>
<iframe src="https://giphy.com/embed/1JyWrrkCIUQyQ" width="480" height="480" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
</body>
</html>

## .lnk Shortcuts

<html>
<div dir="rtl" align="right">
نقدر نسوي hijack لل Shortcuts وبهذه الطريقة اذا المستخدم شغل firefox رح يشتغل وبنفس الوقت رح يشغل برنامجنا. في ال properties عدل على ال target وحط فيه الكوماند الي تحت وعدل على خيار ال Run وحطه Minimized
</div>
</html>

`powershell.exe -c "invoke-item 'C:\Program Files\Mozilla Firefox\firefox.exe'; invoke-item c:\windows\system32\cmd.exe"`


![](../../images/persistence/16.png)

<html>
<div dir="rtl" align="right">
في حال تغيرت ال icon تقدر ترجع تعدلها من ال properties
</div>
</html>

### `Demo:`

![](../../images/persistence/17.gif)


## User Login

<html>
<div dir="rtl" align="right">
نقدر نعدل على ال registry ونخلي كل مرة المستخدم يسجل دخول يشتغل برنامجنا. أول شي رح تسويه هو انك تكتب الملف الأتي:
</div>
</html>

`zoldyck.bat:`

```bat
@ECHO OFF

C:\Windows\System32\calc.exe
```

<html>
<div dir="rtl" align="right">
أستخدم الكوماند الي تحت عشان تعدل على ال registry:
</div>
</html>

`reg add "HKEY_CURRENT_USER\Environment" /v UserInitMprLogonScript /d "C:\temp\zoldyck.bat" /t REG_SZ /f`

### `Demo:`

![](../../images/persistence/18.gif)


# DLL Hijacking

