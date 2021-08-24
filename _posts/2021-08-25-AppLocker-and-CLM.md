---
title: Bypassing AppLocker and CLM
author: Z0ldyck
date: 2021-08-25 18:32:00 -0500
categories: [Blogging, Tutorial]
tags: [zoldyck]
---

## What is AppLocker?

<html>
  <div dir="auto">
    ال AppLocker هو عبارة عن برنامج موجود في ال Windows يقدر يقيد البرامج الثانية كال executable files. و ال AppLocker rules تكتب لخمس فئات:
    </div>
</html>


- Executable
- Windows Installer
- Script
- Packaged App
- DLLs

<html>
  <div dir="auto">
    وفي default configuration لل AppLocker تخلي بعض الأماكن مسموح فيها ال executable files لان هذا المكان فيه ملفات trusted by Windows مثل C:\Windows و ال C:\Program Files . الصعوبة في عملية ال bypass لل AppLocker  تعتمد على ال rules الي موجودة. خلونا ناخذ مثال صغير ونحاول نجيب revers shell على النظام. لنفترض اننا نقلنا ملف ال revers shell لل Desktop. اذا جربنا نشغل الملف رجع لنا هذا ال Error:
    </div>
</html>

\
&nbsp;
![GUI](../../images/Applocker-CLM/1.png)

![reverse shell](../../images/Applocker-CLM/2.png)


<html>
  <div dir="auto">
    من ال Error نقدر نتأكد ان ال AppLocker شغال. خلونا اول شي نستعرض ال rules الخاصة بال AppLocker عن طريق هذا الأمر:
    </div>
</html>

\
&nbsp;
```powershell
Get-ApplockerPolicy -Effective -xml > C:\users\IEUser\Desktop\AppLocker.xml
```
