## #1 INTRODUCTION

### 1.5 What Makes a Website?

    - Website is just text
    - 브라우저 understands your code

### 1.6 What is HTML

    - text -> language
    - website made of 3 lang : HTML, CSS, JS

    HTML : Hypertext Markup Language
        browser (google chrome, firefox, explorer)
        브라우저에게 웹사이트의 content가 어떻게 구성되어 있는지 설명할때 사용

### 1.7 What is CSS

    CSS : Cascading Style Sheets
    should be use both CSS & HTML
    browser에게 웹사이트가 어떻게 보여야하는지에 대해 알려줌

    HTML은 "brower야 이건 title이야" -> 뼈대
    CSS는 "brower야 그 title은 녹색이어야해" -> 근육

    HTML이 없다면, CSS는 쓸 수 없어

### 1.8 What is JavaScript

    JS : 웹사이트의 뇌 -> 웹 사이트의 동적인 부분
    클릭했을 때 애니메이션
    interactivity
    모든 app이 interactive가 필요한건 아님

### 1.9 Recap

    HTML -> Markup language (Borns)
    CSS -> language for design and style (Mustle)
    JS -> Web Programming language (Brain)

## #2 LEARNING HTML

### 2.0 Our First HTML File

    파일명/폴더명은 항상 소문자로 작성한다
    html -> 확장자명
    파일 내용이 변경될 때 마다, 저장 필수

### 2.1 Setup and Errors

    Extensions에서 테마와 아이콘 설치

### 2.2 Our First HTML Tag

    What is tag -> Html은 tag를 text로 넣음
    <food>김치</food>라는 tag로 인해 브라우저는 김치가 food라는 걸 알게 됨
    tag는 닫아주자
    <h1> ~ <h6>

### 2.3 More Tags and Prettier

    <ul> //unordered list
    <ol> //ordered list
    <list> //list element
    확장프로그램 prettier -> 코드 오류 자동 수정

### 2.4 Tag Attributes

    <a></a> //anchor_닻 -> link
        link는 추가적인 정보가 필요함 -> where we going
        -> tag에 추가하는 부가적인 정보 : attribute(속성)
        * href(attribute) : http reference or hyperlink reference
            href는 오직 a 태그에만 적용할 수 있다.
        * target : default 값 _self , _blank

    <img/> //닫아주는 태그가 존재하지 않음 -> self-closing tag(자체 닫기 태그)
        * src

### 2.5 More Tags and Head

    <!DOCTYPE html> //브라우저에게 text 파일이 아닌 html 문서임을 알려줌
    <html>
        <head> 웹사이트의 환경을 설정 </head>
        <body> 사용자가 볼 수 있는 content </body>
    </html>

### 2.6 Its All About the Head

    <meta> 구글 검색에서 보여지는 description
    구글이 사이트에서 title과 description을 가져오는거야

    <meta charset="utf-8"/> 브라우저에게 text를 어떻게 그려달라는지 말해줌
    * meta 태그는 self closing tag

    <html lang=""> 구글, 네이버, bing 같은 검색 엔진들에게 도움을 주기 위해서

### 2.7 More Tags

    html tags mdn 페이지에서 확인

### 2.8 Form Tags 2.9 More Tags and IDs

    <form>
    <label> form에 question을 추가할 수 있음

    for과 id에 들어가는 값은 동일해야함
    -> for과 같은 값을 가진 id를 들고있는 input을 작동시켜줌

    element당 하나의 id만 가질 수 있음
    전체 html 문서에서 id는 고유해야함

    id : scripting이나 css를 식별하려는 목적을 가진 attribute

### 2.10 Semantic HTML

    <div> - division 분할, 구분, 경계선
    div 는 박스
    <span> - for short text

    <head> != <header>

    <header>, <main>, <footer>  body 안에 포함 되어있는 태그
    div를 대체 할 수 있음 -> 하지만 알아보기 어렵기 때문에 지양

    main, footer, aside 등등 의미가 있는 box를 되도록이면 쓰자

### 2.11 Recap

    Always use ""(큰따옴표) !!

## #3 LEARNING CSS

### 3.0 How to Add CSS to HTML

    어떻게 하면 CSS를 HTML페이지에 추가할 수 있는지를 이해해야 함

    CSS와 HTML을 같이 둘 수도 있고 따로 둘 수도 있음

    방법 1. <head> 태그 내부에 <style> 태그를 작성하고 안에 CSS 기입

    방법 2. CSS 파일을 따로 두고 link로 파일을 연결
    rel(rel="stylesheet" 명시)

    styles.css는 스타일시트

### 3.1 Writing Our First CSS Lines

    selector 안에 속성 properties 명시
    HTML의 어떤 태그를 가리키고 CSS로 잡아와서 쓰면댐

    tag { property : vale; } // 세미콜론 꼭 찍어야함

### 3.2 What Does Cascading Mean

    Cascading 브라우저가 css코드를 읽을때 위에서 부터 차례대로 읽음

    inline CSS / external CSS

    만약 위 두 CSS코드가 같은 대상을 가리키게 되면 어떻게 될까?

    마지막 코드로 적용됨

### 3.3 Blocks and Inlines

    box(div)옆에는 아무것도 오지 않음
    span은 옆에 다른 요소들이 올 수 있음

    box - div , p, address, header
    inline - a(link), span, img

### 3.4 Margin Part One

    block을 inline으로 바꾸는 게 가능할까? ㅇㅇ
    inline을 block 속성으로 변경 : display

    span의 default display 속성 : inline
    inline은 높이와 너비를 가질 수 없음

    box의 엄청난 특징 3가지
    margin padding border

    * margin : box의 border(경계)로부터 바깥에 있는 공간

### 3.5 Margin Part Two

    margin: 0; //사방
    margin:20px 15px; // 위아래_양 옆
    margin: 5px; 10px; 15px; 20px;  //위 오 아래 좌 ( 시계 방향 )

    collapsing margins : 두 박스의 경계가 같다면 두 margin은 하나로 취급됨

### 3.6 Paddings and IDs

    padding : box의 경계로부터 안쪽에 있는 공간

    #first : id가 first인 것을 가리킴

### 3.7 Border

    border : 2px solid black
    *{
        모든 요소에 적용
        inline에도 적용됨
    }

### 3.8 Classes

    inline은 높이와 너비 없음 -> 위, 아래 margin 을 가질수 없음
    class="blue"
    css -> .blue{}
    class는 재사용이 가능, id는 고유해야함

    class="btn blue" -> 여러개 적용 가능

### 3.9 Inline Block

    display : inline-block inline속성을 가지면서 너비 높이를 가질 수 있음
    but inline-block 은 별로임. 정해진 형식이 없기 때문

### 3.10 Flexbox Part One

    flexbox : 자식 엘리먼트에 말하지 않고 부모 엘리먼트에만 말한다

    body {
        display: flex;
        justify-content: center, flex-end, flex-start, space-evenly...
    }

    main axis : 주축 -> justify-content
    cross axis : 교차축 -> align-items

    vh : viewport height

### 3.11 Flexbox Part Two

    주축과 교차축은 디폴트로 수평, 수직
    디폴트 값을 바꾸기 위해선 flex-direction 수정
    flex-direction : column -> 주축과 교차축을 변경

### 3.12 Fixed

    position : 위치를 옮기고 싶을 때 사용
    position : fixed -> 그대로 존재
    top, left, bottom 중 하나만 수정해도 다른 레이어가 됨

### 3.13 Relative Absolute

    position : static; // 레이아웃이 박스를 처음 위치하는 곳에 두는 것
    position : relative; //element가 처음 위치한 곳을 기준으로 수정하는 것
    position : absolute; //가장 가까운 relative 부모를 기준으로 이동시켜줌

    부모 relative - 자식 absolute

### 3.14 Pseudo Selectors part One

    div:first-child{}
    span:nth-child(n){} ; span:nth-child(even, 3n+1){}

### 3.15 Combinators

    p안에있는 span을 변경하고 싶어
    p span {}
    div > span {div 바로 밑 자식만 변경}
    p + span {p바로 다음 형제 span에 적용}

### 3.16 Pseudo Selectors part Two

    p~span span이 p의 형제인데 바로 뒤에 오지 않을 때 쓸 수 있는 것

    input:required{}
    input[type="password"]{}
    input[placeholder~="name"]{} //placeholder에 name값을 가진 모든 값을 변경

### 3.17 States

    button:active{} : 클릭시 액션
    button:hover{} : 마우스 오버시
    button:focus{} : 선택되었을때

    a:visited{} : 사이트를 이미 방문했을때

    focus-within : focused인 자식을 가진 부모 엘리먼트에 적용 되는 거
    form:focus-within{}

    form:hover input{
        form이 hover가 되어있고 그안에 input이있을때 적용 됨
    }

### 3.18 Recap

    p::selection {
        지정한 곳 효과
    }
    p::first-letter{
        첫 글자만 효과
    }

### 3.19 Colors and Variables

    3 color systems
    1. hexadecimal color(16진수 컬러)
    2. rgb
    3. rgba(a-투명도)

    :root{ //변수 설정하고
        --main-color: red;
    }

    p{
        background-color: val(--main-color);
    }

    a{
        color: var(--main-color);
    }

## #5 GIT AND GITHUB

## #6 ClONING

### 6.12 Border Box

    box-sizing: border-box //padding을 줘도 크기를 변경하지 마 box 늘리지마
