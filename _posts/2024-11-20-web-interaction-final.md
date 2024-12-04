---
title:  "웹인터랙션프로그래밍 교과목 프로젝트 [My Origin Wizard]"
header:
  teaser: "/assets/images/posts_img/web-interaction-final/teaser.png"
categories:
  - Projects
  - Code
tags:
  - front-end
  - html/css/js
toc: true
toc_sticky: true
toc_label: "My Origin Wizard"
---
<style>
  .ico {
    border-radius: 5px;
    height: 30px;
    margin-bottom: 5px;
  }
</style>
<br>
# 📝 나의 일대기 9가지 페이지를 JavaScript 기반의 상호작용 사이트로 제작

| **기간**    | 2024.09 ~ 2024.12 (2-2학기)                                                                                     |
| **인원**    | 개인                                                                                         |
| **담당분야**  | 사이트 콘셉트 수립, 9개 콘텐츠 기획 및 기능구현                                    |
| **관련 링크** | <a href="https://hwijaekim.github.io/my-origin-wizard" target="_blank">https://hwijaekim.github.io/my-origin-wizard</a> |

<br><br>


# 🔑 핵심 기술 요약
- `display: flex;`, `flex-flow: row wrap;` 스타일 적용으로 윈도우 크기변화에 따른 적절한 아이콘 배치
- `JQuery UI` 사용으로 `index.html`에서 윈도우 창 드래그 기능 구현
- `forEach`를 이용해 `index.html`에서 각 아이콘 클릭에 대한 페이지 전환을 자연스럽고 적은 양의 코드로 구현

<br><br>
video
<br><br>

# 📌 주요 코드
## `flex` 아이콘 배치 + JQueery UI를 이용한 드래그 구현
```css
#win_contents {
    /*border: solid 1px red;*/
    width: 95%;
    height: 90%;
    margin: 0 auto;
    display: flex;
    flex-flow: row wrap;
    align-items: baseline;
}
```
```javascript
$(() => {
    $('#win_container').draggable();
})
```
![2-1](/assets/images/posts_img/web-interaction-final/2-1.webp)

## `forEach`로 페이지 전환을 자연스럽고 적은 양의 코드로 구현
```javascript
//index.html에서 각 아이콘 클릭시 화면전환 기능 구현
const icons = document.querySelectorAll('.iconFlex');  //총 9개의 iconFlex 클래스를 querySelectorAll 배열로 변수 지정
const popupBox = document.getElementById('popup');  //아이콘 클릭시 자연스럽게 전환될 수 있도록 popup id 변수 지정

icons.forEach((icon,index) => {  //iconFlex div를 forEach, 클릭된 icon의 순서를 알기 위해 index를 추가로 선언
    icon.addEventListener('click', () => {  //icon을 클릭하면
        popupBox.classList.add('active');  //미리 선언해둔 팝업 변수에 active클래스를 추가하여 keyframe애니메이션 재생

        //핵심 코드. popupBox에 active 클래스가 추가되고 1초 후 내부 코드 실행
        setTimeout(() => {
            /*
            * index페이지 전환 코드
            * 각 서브 페이지 이름은 1~9.html로 지정해 두었음
            * forEach에서 선언한 index값은 클릭한 icon의 순서
            * querySelectorAll로 불러온 배열은 0부터 시작하므로 클릭한 index에 1을 더함
            * 최종적으로 백틱을 사용하여 클릭한 icon에 대한 순서(index)값+1.html 파일을 1초 후 열도록 프로그래밍
            * ex. 6번째 아이콘을 클릭 -> index값은 5 -> 5+1 => 6.html 1초 후 전환
            * */
            window.location.href = `./${index + 1}.html`;
        }, 1000);
    })
})
```
![2-2](/assets/images/posts_img/web-interaction-final/2-2.webp)
