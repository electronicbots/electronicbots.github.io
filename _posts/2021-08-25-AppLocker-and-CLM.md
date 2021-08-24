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

## Bypassing AppLocker
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
\
&nbsp;
<html>
  <div dir="auto">
    حفظنا النتائج في ملف xml موجود على ال Desktop نقدر نقرأ المعلومات الي بداخله:
    </div>
</html>

![AppLocker](../../images/Applocker-CLM/3.png)

<html>
  <div dir="auto">
    خلونا نركز اول شي على هذه الجزئية:
    </div>
</html>

![Deny](../../images/Applocker-CLM/4.png)


<html>
  <div dir="auto">
    نقدر نشوف انه في Deny على "%OSDRIVE%\Users\*" طيب ممكن تسأل وين مكان ال "%OSDRIVE%" هذا المكان بس ال AppLocker يتعامل معاه نقدر نسوي سيرش خفيف يرجع لنا هذه ال article من Microsoft:
    </div>
</html>

![Google](../../images/Applocker-CLM/5.png)


![Microsoft](../../images/Applocker-CLM/6.png)


<html>
  <div dir="auto">
    نقدر نعرف انه "%OSDRIVE%" هو نفسه ال "%SystemDrive%" والي هو عبارة عن "\:C" فنقدر نفهم انه كل ال executable file الي موجودة في هذا ال path ما رح تشتغل "C:\Users\" بنفس الوقت شوفو هذه الجزئية:
    </div>
</html>


![Temp](../../images/Applocker-CLM/7.png)


<html>
  <div dir="auto">
    نقدر نعرف انه مسموح نشغل اي executable file فيه ال C:\temp فخلونا ننقل ملف ال reverse shell لهذا المكان ونجرب نشغله.رح نلاحظ انه ما رجع لنا اي error و جتنا shell في ال kali:
    </div>
</html>

![cp](../../images/Applocker-CLM/8.png)


![MSF](../../images/Applocker-CLM/9.png)

\
&nbsp;

<html><div dir="auto" class="tip" markdown="1">هذا المكان بس ال AppLocker يتعامل معاه نقدر نسوي سيرش خفيف يرجع لنا هذه ال article من Microsoft: `%OSDRIVE%`</div></html>


`%OSDRIVE%`
