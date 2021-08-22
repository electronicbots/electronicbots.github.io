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
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {box-sizing: border-box;}
body {font-family: Verdana, sans-serif;}
.mySlides {display: none;}
img {vertical-align: middle;}

/* Slideshow container */
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

/* Caption text */
.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

/* The dots/bullets/indicators */
.dot {
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active {
  background-color: #717171;
}

/* Fading animation */
.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 1.5s;
  animation-name: fade;
  animation-duration: 1.5s;
}

@-webkit-keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}

@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}

/* On smaller screens, decrease text size */
@media only screen and (max-width: 300px) {
  .text {font-size: 11px}
}
</style>
</head>
<body>

<div class="slideshow-container">

<div class="mySlides fade">
  <div class="numbertext">1 / 3</div>
  <img src="../../images/certs/CRTO.png" style="width:100%">
  <div class="text">CRTO</div>
</div>

<div class="mySlides fade">
  <div class="numbertext">2 / 3</div>
  <img src="../../images/certs/eCPPT.png" style="width:100%">
  <div class="text">eCPPT</div>
</div>

<div class="mySlides fade">
  <div class="numbertext">3 / 3</div>
  <img src="../../images/certs/eWPT.png" style="width:100%">
  <div class="text">eWPT</div>
</div>

</div>
<br>

<div style="text-align:center">
  <span class="dot"></span> 
  <span class="dot"></span> 
  <span class="dot"></span> 
</div>

<script>
var slideIndex = 0;
showSlides();

function showSlides() {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("dot");
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  slideIndex++;
  if (slideIndex > slides.length) {slideIndex = 1}    
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
  setTimeout(showSlides, 2000); // Change image every 2 seconds
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
