---
title:  "제 30회 커뮤니케이션디자인국제공모전 동상 수상작 [청사진]"
header:
  teaser: "/assets/images/posts_img/blueprint/teaser.png"
categories:
  - Projects
  - Code
tags:
  - front-end
  - html/css/js
  - figma
  - 공모전
  
toc: true
toc_sticky: true
toc_label: "청사진"
---
<br>
# 📝 학교 밖 청소년들의 미래를 준비하기 위한 솔루션

| **기간**    | 2024.03 ~ 2024.06 (2-1학기)                                                                                     |
| **인원**    | 기획1, 디자인1, **개발1**                                                                                         |
| **담당분야**  | 팀장 및 서비스 비디오 촬영,<br>웹 콘텐츠 소스 제작 및 HTML/CSS/JS를 이용한 웹 제작 및 GitHub 배포                                    |
| **관련 링크** | <a href="https://hwijaekim.github.io/blueprint2024" target="_blank">https://hwijaekim.github.io/blueprint2024</a> |

   <br><br>


# 🔑 핵심 기술 요약
- HTML/CSS/JS 세 가지를 이용하여 처음으로 제작한 웹 사이트 <br>
- Web Fonts를 적용하여 웹 사이트를 더욱 완성도 있게 배포
- `Vanilla JavaScript`를 적극적으로 활용한 프로젝트이며 `Ovserver`를 이용하여 `Viewport`에 감지될 시 CSS `active`클래스를 토글하여 애니메이션을 구현. <br>
- `Typeit.js` 외부 라이브러리를 사용하여 타이핑 애니메이션 구현.

<br><br>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Lnxbw6FSc_I?si=LyU-lvSpD1P7YVNH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<br><br>

# 📌 주요 코드
## Web Fonts 및 <head> 정리
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>청사진</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="./sources/site_icon.png">
<!--    CSS선언-->
    <link rel="stylesheet" href="./style/index_style.css">
    <link rel="stylesheet" href="./style/index_keyframe_media.css">

<!--    외부JS라이브러리 선언 >>TypeIt 비영리목적 무료-->
    <script src="https://unpkg.com/typeit@8.7.1/dist/index.umd.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/dixonandmoe/rellax@master/rellax.min.js"></script>


    <!--    WebFonts 선언-->
    <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.min.css" />
    <link href="https://cdn.jsdelivr.net/gh/sun-typeface/SUIT/fonts/static/woff2/SUIT.css" rel="stylesheet">

</head>
```