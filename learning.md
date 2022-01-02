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