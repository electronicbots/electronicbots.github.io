---
title: Who Am I

# The About page
# v2.0
# https://github.com/cotes2020/jekyll-theme-chirpy
# © 2017-2019 Cotes Chung
# MIT License
---

> **Note**: Add Markdown syntax content to file `tabs/about.md` and it will show up on this page.

Hello reader, My name is Mohammed or as known as Z0ldyck. I am a first-year student at Champlain College majoring in Cyber Security. I started learning about Network and Web Penetration Testing while I am in High School. Before High School, I had some experience with programming and Arduino.

# Certifications

### Certified Red Team Operator `(CRTO)`

### Offensive Security Certified Professional `(OSCP)`

### eLearnSecurity Certified Penetration Tester `(eCPPTv2)`

### eLearnSecurity Web Application Penetration Testing `(eWPT)`

### eLearnSecurity Junior Penetration Tester `(eJPT)`

### PentesterLab Badges
- Blue
- Intercept
- Serialize
- White
- Yellow
- Essential
- PCAP
- Unix

<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<style>
.mySlides {display:none;}
</style>
<body>

<div class="w3-content w3-display-container">

<div class="w3-display-container mySlides">
  <img src="../../images/certs/CRTO.png" style="width:100%">
  <div class="w3-display-topleft w3-large w3-container w3-padding-10 w3-black">
    CRTO
  </div>
</div>

<div class="w3-display-container mySlides">
  <img src="../../images/certs/eCPPT.png" style="width:100%">
  <div class="w3-display-topleft w3-large w3-container w3-padding-10 w3-black">
    eCPPT
  </div>
</div>

<div class="w3-display-container mySlides">
  <img src="../../images/certs/eWPT.png" style="width:100%">
  <div class="w3-display-topleft w3-large w3-container w3-padding-10 w3-black">
    eWPT
  </div>
</div>

<div class="w3-display-container mySlides">
  <img src="../../images/certs/eJPT.png" style="width:100%">
  <div class="w3-display-topleft w3-large w3-container w3-padding-10 w3-black">
    eWPT
  </div>
</div>

<button class="w3-button w3-display-left w3-black" onclick="plusDivs(-1)">&#10094;</button>
<button class="w3-button w3-display-right w3-black" onclick="plusDivs(1)">&#10095;</button>

</div>

<script>
var slideIndex = 1;
showDivs(slideIndex);

function plusDivs(n) {
  showDivs(slideIndex += n);
}

function showDivs(n) {
  var i;
  var x = document.getElementsByClassName("mySlides");
  if (n > x.length) {slideIndex = 1}
  if (n < 1) {slideIndex = x.length}
  for (i = 0; i < x.length; i++) {
     x[i].style.display = "none";  
  }
  x[slideIndex-1].style.display = "block";  
}
</script>

</body>
</html>

# Achievements

### Registered three CVEs:
- CVE-2021-31760
- CVE-2021-31761
- CVE-2021-31762

### Acknowledged By (Webmin)

### CyberPatriot
First place ( 1st ) in Vermont’s CyberPatriot for three years in a row (2019 - 2021)


# Personal Projects

### Zmuggler
- A tool that automates the process of testing web applications against HTTP Request Smuggling vulnerabilities.

### ZRedirect
- A tool that automates the process of testing web applications against Open Redirection vulnerabilities.
