# 강의 6.1

- prettier 적용 후 !
- class name 할 때 안 흔한거 ex) line,box 쓰지 마
- status-bar\_\_column : 겹치지 않게

# 강의 6.2

- bem : block element modifier
- id 안 쓰고 class만 쓰자 : class였는지 id였는지 헷갈릴 때 있어서 통일함

# 강의 6.3

- fontawsome
  1. script는 항상 body의 맨 끝
  2. js파일의 형식

# 강의 6.4

- header는 여러 개가 나올 수 밖에 없음
  - header에 class로 이름을 붙이자 ex)welcome-header
- href="#" : 자기자신으로 복귀

# 강의 6.5

- link:css 단축키
- 상단바
  - display:flex
  - justify-content : space-between
- 와이파이 아이콘 살짝 여백 - margin-right : 5px
  -body에 font-family

# 강의 6.6

- reset css
  - 브라우저가 임의로 정해놓은 margin 등을 없앤다. ex)body의 margin을 0으로 만들기
  ``` css
  html, body, div, span, applet, object, iframe,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  a, abbr, acronym, address, big, cite, code,
  del, dfn, em, img, ins, kbd, q, s, samp,
  small, strike, strong, sub, sup, tt, var,
  b, u, i, center,
  dl, dt, dd, ol, ul, li,
  fieldset, form, label, legend,
  table, caption, tbody, tfoot, thead, tr, th, td,
  article, aside, canvas, details, embed, 
  figure, figcaption, footer, header, hgroup, 
  menu, nav, output, ruby, section, summary,
  time, mark, audio, video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
  }
  /* HTML5 display-role reset for older browsers */
  article, aside, details, figcaption, figure, 
  footer, header, hgroup, menu, nav, section {
    display: block;
  }
  body {
    line-height: 1;
  }
  ol, ul {
    list-style: none;
  }
  blockquote, q {
    quotes: none;
  }
  blockquote:before, blockquote:after,
  q:before, q:after {
    content: '';
    content: none;
  }
  table {
    border-collapse: collapse;
    border-spacing: 0;
  }
  ```

- reset.css 만들고
    ``` css
    @import "reset.css";
    ```
- statusbar 내용도 따로 css만들어서 import 하자

- h1,p를 포함한 header 가운데 정렬
  ```css
  text-align:center;
  ```

- welcome-header 가운데 정렬
  1. welcome-header__title, welcome-header__text의 box를 가운데정렬
    ``` css
    display:flex;
    flex-direction:column;
    align-items:center;
    ```
  2. welcome-header__text box 안의 내용을 가운데정렬
    ```css
    text-align: center;
    ```

- opacity

# 강의 6.7
varibles.css 만들고
```CSS
  :root{
    --yellow:#fae100;
  }

  //변수 쓸 때
  var(--yellow)
```

border<-->outline

pseudo-element : selector::element - 포함된거
pseudo-class : selector:class - ~상태

# 강의 6.9

```html
<form action="friends.html" method="get" login-form">
```

# 강의 6.10

nav>ul>li*4>a

a는 기본 색깔이 blue -> reset.css에서 바꿔주자.

nav아래 고정
```css
positon:fixed;
bottom:0;
```

# 강의 6.11

```css
box-sizing : border-box;
```
nav에 width : 100%를 적용했을 때 오른쪽이 짤리는 경우
- padding 때문임
- padding 20px + width 100% 해서 박스의 크기가 화면보다 커짐
- 따라서 border-box를 통해 해결

# 강의 6.13

display : absolute 쓰려면 parent가 relative여야 한다.

# 강의 6.16

- 자주 반복되는 것은 component화 해서 따로 저장하자

- component의 종류는 같지만 size가 다르거나 하면
```css
<img class="user-component__avatar user-component__avatar--xl" src="images/01.png"/>
```
 처럼 class를 하나 추가하자

- 설계할 때
  - header
  - main
  - footer

 # 강의 6.20
 
 span은 inline요소이므로 padding-top이 안돼

 position : fixed 하면 부모로부터 독립됨(diffent layer)
 -> 넓이도 달라짐
 -> width:100% 하자