---
title:  "React 시작 + 문제 해결"
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
toc_label: "React 설치 + 문제 해결"
---

***Node.js는 이미 설치 되었다는 가정***   
처음에는 `create-react-app` 명령어로 시도했지만 추후 vite를 이용함.

<br>

# Vite를 이용한 React 프로젝트 생성
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


<br>

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

<br>

### 실패과정
Google 검색과 chatGPT를 이용하여 오류를 검색하고 많은 해결법을 시도해 봤지만 여전히 같은 오류가 발생했음.   
<br>
**터미널 입력**
```bash
npm i react@18 react-dom@18
```
설명: 최근 출시된 리액트19 릴리즈에서 의존성 버전 문제를 일으킨 것으로 추정. 하지만 어디까지나 임시 해결책으로 장기적으로는 권장되지 않음.   
<br>

하지만 위와 같은 해결법은 임시 해결법으로 **React 19 출시와 함께 의존성에 대한 오류**가 발생한 것으로 추정되었음.   

<br>

## 해결
Node.js버전은 당시 **v20.17.0**으로 공식적으로는 문제가 없었지만 마지막 방법으로 LTS최신버전인 **v22.12.0** 버전으로 업데이트 함.   
결과적으로 문제 없이 `npm run dev` 명령어가 작동하였으며 `localhost`로 잘 작동함.   
<br>
![Vite + React](/assets/images/posts_img/install-react/vite+react.png)

<br>

하지만 여기서 드는 의문점은 **Windows 환경.**   
Windows에서의 Node.js 버전은 **v20.17.0**으로 **macOS와 동일한 버전**이지만 React 환경이 정상적으로 실행됐음   
![win-node](/assets/images/posts_img/install-react/win-node.png)
![win-react](/assets/images/posts_img/install-react/win-react.png)


<br>
---
<br>


# 프로젝트 시작