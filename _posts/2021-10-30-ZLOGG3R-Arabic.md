---
title: ZLOGG3R (Arabic)
author: Z0ldyck, Mazen
date: 2021-08-25 18:32:00 -0500
categories: [Blogging, Tutorial]
tags: [ZLOGG3R, KeyLogger]
---

<html>
<p><span style="font-size:20pt;font-family:Arial;color:#a52a2a;background-color:transparent;font-weight:400;font-style:normal;font-variant:normal;text-decoration:none;vertical-align:baseline;white-space:pre;white-space:pre-wrap;">Agenda:</span></p>
</html>

- المقدمة
- تثبيت التطبيق
- دليل المستخدم
- ماهي التحديثات القادمة؟

<html>
<div dir="rtl">
<p dir="rtl" align="right"><span style="font-size:20pt;font-family:Arial;color:#a52a2a;background-color:transparent;font-weight:400;font-style:normal;">المقدمة:</span></p>
</div>
</html>


<html>
<div dir="rtl" align="right">
<h3>بسم الله الرحمن الرحيم</h3>
</div>
</html>
  

<html>
<div dir="rtl" align="right">
مرحبًا بالجميع ، قبل ان ادخل في تفاصيل تطبيقنا الجديد ، سوف أقدم خلفية عن هذا المشروع . تطبيق ZL0gg3r هو مشروع بحث للكلية ، كان المشروع عبارة عن إنشاء Keylogger بسيط يتم إنشاؤه باستخدام لغة Python ، لكن اتخذت القرار بأن اتحدى نفسي أكثر وانشأه باستخدام لغة C# لأني بدأت باستخدامها مؤخراً .
</div>
</html>

<html>
<div dir="rtl" align="right">
<br>
  
بعد اتخاذ القرار طرحت فكرة التطبيق الى أحد اصدقائي وبعدها اقترح علي انه بأمكاننا انشاء Keylogger بمميزات اضافية ، ومن هنا اتى سبب إنشاء هذا التطبيق .
فلذلك باذن الله سوف نقوم بأضافة المميزات مستقبلا التي ستجعل من التطبيق أكثر من مجرد Keylogger .


بدأنا بعد رسم الخطة بالاساسيات فقط، التي كانت مجرد انشاء Keylogger واضافة الميزات البسيطة 
وأثناء إنشاء التطبيق كانت الأفكار والميزات الجديدة تتبادر إلينا ، لم نرغب في تغيير اصدار التطبيق حتى ننتهي من بناء التطبيق بالكامل ، لذلك قررنا اطلاق هذا الإصدار التجريبي ، وستتم إضافة المميزات إليه بشكل شهري 
بأمكان الجميع اقتراح أفكار جديدة قد تطور وتجعل التطبيق أفضل.
</div>
<br>
</html>


<html>
<div dir="rtl">
<p dir="rtl" align="right"><span style="font-size:20pt;font-family:Arial;color:#a52a2a;background-color:transparent;font-weight:400;font-style:normal;">تثبيت التطبيق:</span></p>
</div>
</html>

<html>
<div dir="rtl" align="right">
،قبل أن تسأل عن طريقة التثبيت او مشاكل التثبيت
يجب عليك اتباع الطريقة التي سوف نشرحها هنا والتأكد من أن كل شيء كما ذكرنا 

التطبيق الان يستخدم FTP Server لنقل الملفات من جهاز الضحية، ولمعرفة المميزات القادمة عليك التحقق من "ما هي التحديثات القادمة؟"
</div>
</html>

<html>
<br>
<div dir="rtl" align="right">
<p><span style="font-size:20pt;font-family:Arial;color:#a52a2a;background-color:transparent;font-weight:400;font-style:normal;">ZL0GG3R:</span></p>
</div>
</html>

<html>
<body>
<div dir="rtl" align="right">
بأمكانك نسخ الكود وإنشاء التطبيق باستخدام Visual Studio أو أستخدام البرنامج المرفق عن طريق تنزيله مباشرة 
<br> #ملاحظة : يُنصح بتنزيل و استخدام البرنامج المرفق مباشرة لأننا نضمن انه سوف يعمل بدون مشاكل ، ايضا قد تحتاج الى تعديل بعض التعليمات ليعمل على نظام ويندوز الخاص بك . <br>

</div>
<br>
<div dir="rtl" align="right">
الان قم بفتح التطبيق في Visual Studio ثم قم بفتح Form2.cs وانتقل الى سطر 53 وقم بتعديل CSC version number ، لانه قد تحتاج الى تعديل هذا المسار الى المسار الموجود على جهازك.
</div> 
</body>
</html>

![](../../images/ZLOGG3R/5.png)

<html>
<br>
<div dir="rtl" align="right">
بعد أن عدلت اصدار CSC الى الاصدار الذي يملكه جهازك، اضغط بزر الماوس الأيمن على اسم التطبيق واضغط على "Build" وسوف يتم إنشاء التطبيق. في نفس الملف انتقل الى "keylogger.cs" افتحه واذهب الى السطر 64 ، وقوم بتعديل عنوان الشبكة الى العنوان الخاص بك. احفظ وسوف تتمكن من استخدام ZL0GG3R الان. 
</div>
</html>

<html>
<br>
<div dir="rtl" align="right">
<p><span style="font-size:20pt;font-family:Arial;color:#a52a2a;background-color:transparent;font-weight:400;font-style:normal;">FTP Server:</span></p>
</div>
</html>


<html>
<body>
<div dir="rtl" align="right">
يجب توضيح أنه بإمكان مستخدم ZL0gg3r ان يستخدم اي FTP Client  ومن الممكن ان يتم انشاء FTP Client خاص بالتطبيق مستقبلاً 
</div>
<br>
<div dir="rtl" align="right">
هنا سوف نساعدك في تثبيت FTP Server لنظام ويندوز وتشغيله 
في شريط البحث ، ابحث عن " تشغيل مميزات Windows او ايقاف تشغيلها" وقم بفتحه 
</div>
</body>
</html>

![](../../images/ZLOGG3R/1.png)

<html>
<div dir="rtl" align="right">
ابحث على " Internet Information Services " وقم بتحديد FTP Server
</div>
</html>

![](../../images/ZLOGG3R/2.png)

<html>
<div dir="rtl" align="right">
ابحث على "Web Management Tools" وقم بتحديدها ليتم التثبيت
الان في شريط البحث ، ابحث عن " Internet Information Services (IIS) Manager " وقم بتشغيله 
</div>
</html>


<html>
<br>
<div dir="rtl" align="right">
حدد من القائمة "site" من ثم "Add FTP Site"
</div>
</html>

![](../../images/ZLOGG3R/3.png)

<html>
<div dir="rtl" align="right">
الان ضع الاسم او المسار ، يُنصح بانشاء مجلد باسم FTP دخل مسار Zl0gg3r واستخدامه
</div>
<br>
<div dir="rtl" align="right">
وبعد ذلك يمكنك ترك كل شيء كما هو ولكن يجب عليك وضع خيار "NO SSL " ومن ثم التالي وحدد في نافذة المصادقة "Basic" ثم تحديد المستخدمين من "Allow access to" ووضع اسم المستخدم الذي تريده وبعدها تأكد من وضع أذونات القراءة والكتابة ، يجب أن يكون كل شيء جاهز للاستخدام الآن.
</div>
<br>
<div dir="rtl" align="right">
الآن للتأكد بأن FTP Server يعمل عليك بنسخ اي ملف ووضعه في مسار FTP والتحقق من ذلك عن طريق File Explorer
</div>
</html>

![](../../images/ZLOGG3R/4.png)

<html>
<div dir="rtl">
<p dir="rtl" align="right"><span style="font-size:20pt;font-family:Arial;color:#a52a2a;background-color:transparent;font-weight:400;font-style:normal;">Web Server:</span></p>
</div>
</html>

<html>
<div dir="rtl" align="right">
علينا استخدام خادم ويب IIS وبأمكانك استخدام اي شيء اخر 
سوف نضع مرجع لكيفية اعداد خادم ويب وتشغيله :  
</div>
</html>

[nstall and Setup a Website in IIS on Windows 10](https://helpdeskgeek.com/windows-10/install-and-setup-a-website-in-iis-on-windows-10/)

<html>
<br>
<div dir="rtl" align="right">
يجب عليك تعيين اسم الملف لخادم الويب على الدليل المسمى "WebSrv" الموجود على مجلد التطبيق. 
</div>
</html>

<html>
<br>
<div dir="rtl">
<p dir="rtl" align="right"><span style="font-size:20pt;font-family:Arial;color:#a52a2a;background-color:transparent;font-weight:400;font-style:normal;">دليل المستخدم: </span></p>
</div>
</html>
<html>

<html>
<br>
<div dir="rtl" algin="right">
تأكد بأن كل ماذكرناه سابقا يعمل بالكامل ، لنضمن عمل التطبيق بالطريقه الصحيحه وبكل سهوله 
وضعنا لكم صورة للصفحة الرئيسية للتطبيق :
</div>
</html>

![](../../images/ZLOGG3R/z1.png)

<html>
<div dir="rtl" algin="right">
دعونا نبدأ بأول تعامل مع التطبيق وهي طريقة انشاء الـ keylogger exe file
قم بإدخال معلوماتك والضغط على زر إنشاء
</div>
</html>

![](../../images/ZLOGG3R/z2.png)

<html>
<div dir="rtl" algin="right">
سيتم انشاء ملف exe في مجلد التطبيق عليك التحقق من ذلك . 
الخطوه الاخرى هي "Log Files" في هذا الخيار يمكنك اختيار المسار الذي توجد عليه جميع log files واستعراضها داخل التطبيق 
</div>
</html>
  
![](../../images/ZLOGG3R/z3.png)
  
<html>
<div dir="rtl">
<p dir="rtl" align="right"><span style="font-size:20pt;font-family:Arial;color:#a52a2a;background-color:transparent;font-weight:400;font-style:normal;">هل هو قابل للكشف؟</span></p>
</div>
</html>
  
<html>
<div dir="rtl" algin="right">
نحن نعلم ان معظم الاشخاص سوف يستخدمون Virustotal لفحص التطبيق ، وهذا ما قد يؤدي إلى اكتشاف البرنامج من الـ AVs ، لذلك هدفنا الرئيسي هو تطوير التطبيق وليس أن نجعله غير قابل للكشف من برامج ومواقع الفحص ، ولكن سوف نبذل كل جهدنا أن يكون غير قابل للكشف. عند كتابة هذا الدليل لم يُكشف التطبيق إلا من AV واحدة فقط : 
</div>
</html>
  
![](../../images/ZLOGG3R/z4.png)
