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
    <meta charset="utf-8" />    
    <style type="text/css">  
        body {  
            margin: 0;  
            background: #e6e6e6;  
        }  
        .showSlide {  
            display: none  
        }  
            .showSlide img {  
                width: 100%;  
            }  
        .slidercontainer {  
            max-width: 1000px;  
            position: relative;  
            margin: auto;  
        }  
        .left, .right {  
            cursor: pointer;  
            position: absolute;  
            top: 50%;  
            width: auto;  
            padding: 16px;  
            margin-top: -22px;  
            color: white;  
            font-weight: bold;  
            font-size: 18px;  
            transition: 0.6s ease;  
            border-radius: 0 3px 3px 0;  
        }  
        .right {  
            right: 0;  
            border-radius: 3px 0 0 3px;  
        }  
            .left:hover, .right:hover {  
                background-color: rgba(115, 115, 115, 0.8);  
            }  
        .content {  
            color: #eff5d4;  
            font-size: 30px;  
            padding: 8px 12px;  
            position: absolute;  
            top: 10px;  
            width: 100%;  
            text-align: center;  
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
            from {  
                opacity: .4  
            }  
            to {  
                opacity: 1  
            }  
        }  
  
        @keyframes fade {  
            from {  
                opacity: .4  
            }  
            to {  
                opacity: 1  
            }  
        }  
    </style>  
</head>  
<body>  
    <div class="slidercontainer">  
        <div class="showSlide fade">  
            <img src="../../images/certs/CRTO.png" />  
            <div class="content">Slide1 heading</div>  
        </div>  
        <div class="showSlide fade">  
            <img src="../../images/certs/eCPPT.png" />  
            <div class="content">Slide2 heading</div>  
        </div>  
  
        <div class="showSlide fade">  
            <img src="../../images/certs/eWPT.png" />  
            <div class="content">Slide3 heading</div>  
        </div>  
        <div class="showSlide fade">  
            <img src="../../images/certs/eJPT.png" />  
            <div class="content">Slide4 heading</div>  
        </div>  
        <!-- Navigation arrows -->  
        <a class="left" onclick="nextSlide(-1)">❮</a>  
        <a class="right" onclick="nextSlide(1)">❯</a>  
    </div>  
  
    <script type="text/javascript">  
        var slide_index = 1;  
        displaySlides(slide_index);  
  
        function nextSlide(n) {  
            displaySlides(slide_index += n);  
        }  
  
        function currentSlide(n) {  
            displaySlides(slide_index = n);  
        }  
  
        function displaySlides(n) {  
            var i;  
            var slides = document.getElementsByClassName("showSlide");  
            if (n > slides.length) { slide_index = 1 }  
            if (n < 1) { slide_index = slides.length }  
            for (i = 0; i < slides.length; i++) {  
                slides[i].style.display = "none";  
            }  
            slides[slide_index - 1].style.display = "block";  
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
