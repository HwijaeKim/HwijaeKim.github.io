---
title:  "서버프로그래밍 교과목 실습응용 [블로그 express 서버]"
header:
  teaser: "/assets/images/posts_img/union-server-programming/teaser.png"
categories:
  - Projects
  - Code
tags:
  - back-end
  - node.js
  - mongodb
  - npm
toc: true
toc_sticky: true
toc_label: "청사진"
---
<style>
  .ico {
    border-radius: 5px;
    height: 30px;
    margin-bottom: 5px;
  }
</style>
<br>
# 📝 MongoDB를 이용한 이미지 업로드를 지원하는 블로그 express 서버

| **기간**    | 2024.11 ~ 2024.12  (2-2학기)                                                                                       |
| **인원**    | 개인                                                                                         |
| **담당분야**  | 개발환경 구축, MongoDB 연결, `multer`를 이용한 이미지 업로드, 그 외 일부 `html, css`를 제외한 요소 구현     |
| **관련 링크** | <sub>학습 교재</sub><br>고영희 저 Do it! Node.js 프로그래밍 입문<br>쉽고 빠르게 달리는 백엔드 개발 / 자바스크립트+노드제이에스+익스프레스+몽고DB로 개발 순서에 따라 직접 서버 만들기! |

<br><br>

# 🔑 핵심 기술 요약
- `js, Node.js, express, MongoDB`를 이용한 기초 express 서버 제작
- `GET, POST, PUT, DELETE` 메서드를 요청하고 처리
- 요청/응답을 처리하는 미들웨어 구성
- 템플릿 엔진으로 `ejs` 연결
- `jsonwebtoken(JWT), cookie`를 이용한 어드민 회원가입/로그인 관리
- `multer`를 이용한 이미지 업로드

<br><br>
video
<br><br>

# 📌 주요 코드
## npm 패키지
```json
  "dependencies": {
    "bcrypt": "^5.1.1",
    "cookie-parser": "^1.4.7",
    "dotenv": "^16.4.5",
    "ejs": "^3.1.10",
    "express": "^4.21.1",
    "express-async-handler": "^1.2.0",
    "express-ejs-layouts": "^2.5.1",
    "gridfs-stream": "^1.1.1",
    "install": "^0.13.0",
    "jsonwebtoken": "^9.0.2",
    "method-override": "^3.0.0",
    "mongoose": "^8.8.1",
    "multer": "^1.4.5-lts.1",
    "nodemon": "^3.1.7",
    "npm": "^10.9.0"
  }
```

## env 설정
```
DB_CONNECT = mongodb+srv://(SECURITY).mongodb.net/myBlog
JWT_SECRET=(SECURITY)
```