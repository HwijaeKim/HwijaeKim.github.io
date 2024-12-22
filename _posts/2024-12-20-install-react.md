---
title:  "React 설치"
header:
  teaser: "/assets/images/posts_img/install-react/teaser.png"
categories: 
  - Research
tags:
  - node.js
  - npm
  - react
toc: true
toc_sticky: true
toc_label: "React 설치"
---

***Node.js는 이미 설치 되었다는 가정***   
!이제 `create-react-app`은 권장되지 않는 방법!

# React 프로젝트 생성
```bash
npm create vite@latest
```
```bash
gimhwijae@gimhwijaeui-MacBookPro react01 % npm create vite@latest

> react01@0.0.0 npx
> create-vite

? Project name: › vite-project [프로젝트명 입력]
```
```bash
? Select a framework: › - Use arrow-keys. Return to submit.
❯   Vanilla
    Vue
    React
    Preact
    Lit
    Svelte
    Solid
    Qwik
    Angular
    Others
```
방향키를 사용해 React에서 엔터

```bash
? Select a variant: › - Use arrow-keys. Return to submit.
❯   TypeScript
    TypeScript + SWC
    JavaScript
    JavaScript + SWC
    React Router v7 ↗
```
방향키를 이용해 JavaScript에서 엔터

```bash
Scaffolding project in /Users/gimhwijae/Git/react-practice/react01...

Done. Now run:

  cd react01
  npm install
  npm run dev

gimhwijae@gimhwijaeui-MacBookPro react-practice % 
```
다음 명령을 차례로 입력하여 실행




## 오류 빌생
macOS 환경에서 다음과 같은 오류가 발생함
><sub>`failed to load config from /Users/gimhwijae/Git/react-practice/react01/vite.config.js
error when starting dev server:
Error: Build failed with 3 errors:
(define name):1:0: ERROR: Expected identifier but found "import"
(define name):1:0: ERROR: Expected identifier but found "import"
(define name):1:0: ERROR: Expected identifier but found "import"
    at failureErrorWithLog (/Users/gimhwijae/Git/react-practice/react01/node_modules/esbuild/lib/main.js:1476:15)
    at /Users/gimhwijae/Git/react-practice/react01/node_modules/esbuild/lib/main.js:945:25
    at runOnEndCallbacks (/Users/gimhwijae/Git/react-practice/react01/node_modules/esbuild/lib/main.js:1316:45)
    at buildResponseToResult (/Users/gimhwijae/Git/react-practice/react01/node_modules/esbuild/lib/main.js:943:7)
    at /Users/gimhwijae/Git/react-practice/react01/node_modules/esbuild/lib/main.js:970:16
    at responseCallbacks.<computed> (/Users/gimhwijae/Git/react-practice/react01/node_modules/esbuild/lib/main.js:622:9)
    at handleIncomingPacket (/Users/gimhwijae/Git/react-practice/react01/node_modules/esbuild/lib/main.js:677:12)
    at Socket.readFromStdout (/Users/gimhwijae/Git/react-practice/react01/node_modules/esbuild/lib/main.js:600:7)
    at Socket.emit (node:events:519:28)
    at addChunk (node:internal/streams/readable:559:12)`</sub>

Google 검색을 통한 임시 해결법   
**터미널 입력**
```bash
npm i react@18 react-dom@18
```
설명: 최근 출시된 리액트19 릴리즈에서 의존성 버전 문제를 일으킨 것으로 추정. 이에 따라 일시적인 해별책을 사용