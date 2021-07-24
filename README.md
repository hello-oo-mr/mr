#HTML, CSS, JS기초

## HTML

>HTML : Hyper Text Markup Language 

>웹페이지의 구조를 표시

>웹페이지의 콘텐츠를 표시 

### HTML Element

>Tag: 태그- 기술적

>문법(syntax)
>
><>로 감싸줌

> 소문자 사용

> 시작태그와 종료태그 세트로 구성됨. 
```
예시 : <tagname>conents</tagname>
```
> 예외) 시작태그만 존재하는 경우: 빈 요소(empty element)

> 포함관계(nested)
```
<body>
  <div>
    text
   </div>
 </body>
```

### HTML Attribute

>HTML 속성
>HTML 요소의 부가 정보

>속성이름= "속성값"

```
<a href=""></a>

```
### HTML 페이지에서 표시하는 콘텐츠
- 텍스트 콘텐츠

- 멀티미디어 콘텐츠(embed 콘텐츠)
 - 이미지
 - 비디오
 - 오디오

### 제목태그

>heading ->h

>h1~h6

>h1이 가장 큰 제목


### HTML 기본구조

```
<!DOCTYPE html> -1
<html> -2
  <head> -3
    <meta charset="utf-8"> -4
    <title>My test page</title> -5
  </head>
  <body> -6
    <p>This is my page</p>
  </body>
</html>

```
1. 웹 문서의 버전 : HTML 5
2. html 문서의 가장 바깥쪽 요소
3. 웹 문서를 설명하는 정보가 담기는 영역 요소
4. 웹 문서의 정보 표현
5. 웹 문서의 제목을 표시하는 요소
6. 웹 문서의 콘텐츠 요소들이 담기는 영역 요소 

### 단락(paragraph) 태그

>단락을 표시
>단락과 단락사이를 구분하는 수평선 
```
<hr> -Horizontal Rule
```
> 단락을 구분하지 않고 줄 바꿈
```
<br> - Break
```
### 목록 태그

> 순서없는 목록 ul (unordered list)
> 순서있는 목록 ol( ordered list)
> 목록 항목 li (List Item)

```
<ul>
 <li>HTML</li>
 <li>CSS</li>
</ul>
```
> 포함관계(nested)로 구성된 목록
> - HTML
>  - HTML4
>  - HTML5
> - CSS
>  -CSS2
>  -CSS3
```
<ul>
<li>
 HTML
 <ul>
  <li>HTML4</li>
  <li>HTML5</li>
 </ul>
</li>
<li>
CSS
<ul>
 <li>CSS2<li>
 <li>CSS3<li>
</ul>
</li>
</ul>
```
> 설명목록(Description List) - dl
> 
```
<dl>
<dt>HTML</dt> (dt : Description Title)
<dd>표준 마크업 언어</dd> (dd : Description Data)
</dl>
```

### HTML Hyper link

>하이퍼링크 a (anchor)
> attribute(속성) : href(hypertext reference)
```
<a href="http:www.naver.com">naver</a>
```
>북마크 기능

>외부 페이지 연결이 아닌 같은 페이지에서 특정위치로 이동할 수 있게 해주는 기능

>도착지점에 id attribute를 사용하여 이름을 지정 
```
<a href="#t1"></a>
...

<h2 id="t1">도착지점</h2>
```

### Table Element

> 기본 사용 태그 : table, thead, tbody, tr, th, td

> 열 제목 : thead (table head), th(table heading)

> 표 내용 : tbody(table body), td(table data)

> 행 : tr(table row) 

>https://www.tablesgenerator.com/html_tables : table generator 
 
### Image element

> Tag: img

> attribute: src (이미지 위치, 파일명), alt(대체 텍스트)

> 종료태그 없음
```
<img src="image.jpg" alt="대체">

```

### video element

>비디오 및 오디오 컨텐츠는 용량이 크기 때문에 서버에 저장을 해서 콘텐츠를 제공하면 많은 트래픽이 발생할 수 있다. 

> 트래픽 과부하를 해결하기 위해서 유뷰브 서비스를 사용하기도 함

>attribute 
>controls: 컨트롤 버튼 표시
>autoplay: 자동재생(* muted와 같이 사용해야함)
>muted: 음소거
>loop:반복재생

```
<video controls autoplay muted loop>
  <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
</video>
```

### Youtube 

>비디오 콘텐츠 제공시 서버의 트래픽 과부하를 해결할 수 있는 방법 중 하나
>매개변수
>controls=1(컨트롤, 기본값), 0(컨트롤x)

>autoplay=1, 0 (mute와 같이 사용)

>mute=1,0
>loop=1,0(playlist와 같이 사용)

```
<iframe width="560" height="315" src="https://www.youtube.com/embed/rwFZPEPbcpQ?controls=0&autoplay=1&mute=1&loop=1&playlist=rwFZPEPbcpQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

>텍스트는 HTML 문서에 직접 입력되는 콘텐츠
>이미지와 동영상, 오디오 콘텐츠는 외부에서 만들어지는 콘텐츠
>이미지, 동영상, 오디오는 직접 입력하는 것이 아니고 외부 파일을 삽입 =>embed 콘텐츠라고 한다. 


### Container Element (단순 영역 구분 요소)

>div(division)

>span 

### Block, Inline 

> 모든 element는 각각의 고유 영역을 가지고 있음

>Block element, Inline Element 구분은 이들 영역의 화면 표시 방식에 따른 구분 

>block element는 줄바꿈되어 표시 - block element 영역의 가로 너비가 부모요소에 100% 채워짐
>(**포함하는 요소 : 부모 요소, 포함되는 요소: 자식요소)

>block element에는 위, 아래 여백을 적용할 수 있음

>inline element는 같은 줄에 나란히 표시 - inline element 영역의 가로너비가 컨텐츠 크기만큼만 정해짐.

>inline element는 위, 아래 여백을 적용할 수 없음


### parent Element(부모요소), child Element(자식요소)

>포함관계에서 포함하는 요소가 부모요소, 포함되는 요소가 자식요소. 
>직계 포함관계에서만 부모요소, 자식요소
>직계가 아닌 포함관계에서는 조상요소(ancestor), 자손요소(decendant)


## CSS

### CSS 기본 개념

> 선택자는 스타일을 지정할 HTML 요소를 가리킵니다. 

> 선언 블록에는 세미콜론으로 구분된 하나 이상의 선언이 포함됩니다.

> 각 선언에는 콜론으로 구분된 CSS 속성(Property) 이름과 값(value)이 포합됩니다. 

> 여러 css 선언은 세미콜론으로 구분되고 선언브록은 중괄호로 묶습니다. 

### id, class
> HTML element에 특정 이름을 사용할 때 id,class attribute를 사용해서 이름을 붙여줄 수 있음. 

> id는 HTML 문서내에서 한번만 쓸 수 있음. 

> class는 동일한 이름이 여러개의 element에 사용할 수 있음. -> 따라서, 공통 디자인 요소나 공통 기능을 적용할 수 있음.

> class는 하나의 HTML Element에 대해서 띄어쓰기로 여러개 이름을 줄 수 있음, html 문서내에서 고유해야 함. 

>id는 하나의 HTML Element 에 대해서 하나의 이름만 존재, HTML 문서내에서 고유해야 함. 

```
<p class="hello nice"</p>
```
> id는 주로 서버에서 불러오는 데이터를 표시하는 위치에 고유하게 사용하는 경우 => 백앤드 개발에서 주로 사용

> class는 주로 css 스타일 적용, javascript 인터렉션 적용할 때 사용   =>프론트 앤드 개발에서 주로 사용


### css 작성방법

>External CSS: 파일 분리

>Internel CSS: 같은 HTML 문서내에 head태그 영역에 style태그를 사용하여 입력

>Inline CSS: 시작태그에 style attribute를 사용해서 입력 => javascript에서 css를 제어할때 사용. 

### naming할 때 표기방식

>id, class naming, 변수, 함수, naming, 파일/폴더 naming의 경우 가독성을 높이기 위해 사용 
>표기방식을 사용하는 이유
> - naming 할 때 두 단어이상으로 구성되는 경우 단어와 단어 사이를 구분하기 위해 사용 
> - 단어의 시작부분에 첫글자를 대문자로 변경, 특수 기호를 사용

> 표기방식종류
> snake case :gnb_depth1 =>파일/폴더
> kebab case : gnb-depth1 =>id/class
> camel case: gnbDepth1 =>javascript의 변수/함수
> pascal case : GnbDepth1 =>javascript의 클래스
> 


  ### OOCSS(Object Oriented CSS)
  
  >Html Element를 대상화시키는 과정에서 element 하나하나를 객체화 시키는 이론
  
  >html element 모두 id, class, attribute 사용해서 이름을 지정해줌
  
  ### web color
  >color mode 
  
  > -가산 혼합(빛의 혼합) : RGB 컬러모드
  
  > 표현할 수 있는 색의 개수 
  
  > 1byte=8bit=256개(0~255)
  
  >RGB =>3byte =>24bit 트루컬러 :16777216가지 색

  >색 표현 코드값
  
  >16진수(hex code): #AABA01
  
  >10진수: RGB(255,255,255)
  >

  >CSS 사용법
  ```
  color:#2abd51
  color:rgb(42,189,81)
  color:rgba(42,189,81,0.5)
  ```
>투명도를 의미하는 용어
 
 >transparent : 투명한

>alpha : 추가 채널

>opacity : 불투명도


### TEXT CSS

- color
- text-align:left, center, right, justify
- text-decoration:none, line-through, underline
- text-transform: uppercase, lowercase, Capitalize(첫글자만 대문자로)
- text-indent(들여쓰기): 20px / -20px 
- letter-spacing(자간): 2px / -2px
- line-height: 20px/ 1.8(배수의 형태로)
- word-spacing(단어별로 띄어쓰기)
- white-space: nowrap  ->줄바꿈 하지 않겠다.
- text-shadow


# font CSS
- font-family : "Times New Roman", Times, serif; 폰트종류중에 띄어쓰기가 있는 경우에만 쌍따옴표로
 - 순서대로 대체 폰트를 찾음
 - sans-serif, serif, monospace, cursive, fantasy 5개의 기본 폰트는 font-family 사용시 종류에 맞게 항상 끝에 기본적으로 사용됨
 - 웹사이트에 사용하는 폰트는 웹폰트(서버에 폰트 파일을 저장해서 사용)로 사용하는데, 업로드된 파일을 직접 사용하는 경우, 웹폰트 서비스를 사용하는 경우 2가지가 있음
 - 웹폰트 서비스의 2가지 있음
 - 대표적인 웹폰트 서비스: 구글 폰트, 눈누
- font-size
- font-style : italic
- font-weight : bold /500
 - 폰트 굵기가 다양한 경우 숫자로 굵기를 표현

### BOX Model
>구성 요소
> -width/height :너비/높이

> -padding: 안쪽 여백

> -border: 테두리

> -margin: 바깥 여백

### width/height
> width : 너비/가로길이

> height : 높이/세로길이

>auto :기본값
>-block : 너비는 부모요소를 기준으로 채워짐./ 높이는 콘텐츠를 기준으로 맞춰짐
>-inline: 너비 높이 둘다 콘텐츠 기준으로 맞춰짐. 

### padding
>안쪽 여백

>padding : 10px 20px 30px 40px (시계방향 순, top, right,bottom, left)
>padding : 10px 20px 30px(top, right/left, bottom)
>padding : 10px 20px(top/bottom, right/left)
>padding: 10px(top/right/bottom/left 모두)

>### margin
>padding과 사용방법이 같음

### margin collapse
> - 위 아래 인접하게 배치된 박스의 사이여백이 둘 중 큰 쪽으로만 적용되어 표현되는 현상

### border
> border :1px solid red; (=> 4방향 모두 적용) 
> border-top :1px solid red; (=> top에만 적용) 
> border-right
> border-bottom
> border-left

### 가로배치

※ inline요소는 박스 모델이 제대로 적용되지 않기 때문에 레이아웃 구성 요소로 사용하기 어렵다.  
※ 따라서, block요소를 레이아웃 구성요소로 사용함. => 세로 배치는 기본 구성

가로 배치 기법
- float
- flex
- grid

### float 
> float : left, float:right 부모요소를 기준으로 배치(왼쪽에 붙일건지, 오른쪽에 붙일건지)
> 일반적으로 왼쪽을 기준으로 순서대로 배치할 때 float:left사용해서 배치

> float 은 박스가 띄워지는 현상이 있으므로 인접해 있는 박스의 배치가 깨질 수 있다. 
> float 박스를 부모요소로 감싸서(div태그) 인접해 있는 박스와 float박스를 감싸고 있는 부모요소와의 관계로 만들어준다.
> float 박스를 감싸는 부모요소는 높이가 0이 될 수 있으므로, clear할 수 있는 비어있는 자식요소를 추가해준다. 
```
<html>
<head>
<style>

img {
float:left;
}

div{
border: 1px solid red;
}
.clearfix{
clear:both;
}
</style>
</head>

<body>
<div class="float-container>
<img src="pineapple.jpg" alt="Pineapple" style="width:170px;height:170px;">
<div class="clearfix"></div>
</div>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum, nisi lorem egestas odio, vitae scelerisque enim ligula venenatis dolor. </p>
</body>
</html>

```

### display 속성

>요소의 기본속성을 변형하지 않고 화면에 표시되는 속성을 변형
> block, inline, inline-block

```div{
display:inline;
}
=> div : inline 속성으로 화면에 표시 
```
> inline-block : inline 의 속성(한 줄에 나란히 표시)과 block의 속성(박스모델 적용)을 모두 표시 

### 폼 요소
> 웸페이지에서 사용자 입력을 받을 사용하는 요소

```
<input type="text"> :일반 텍스트
<input type="password"> : 비밀번호 입력 

<input type="button" value="확인버튼"> 
<button type="button">확인버튼</button> 
```

### 이미지 표현 방법
> 콘텐츠로 표현
> - img태그로 

> 디자인 요소로 표현
> -background-image

> IR(Image Replacement) 기법
> - HTML Element에는 텍스트로 표시
> - 화면(브라우저)에 표시할때는 이미지로 표현

### background 
>background-color

>background-image

> background-repeat
> - repeat-x (가로만 반복) repeat-y(세로만 반복) no-repeat(반복없음)

> background-position
> -left, center, right/ top, center, bottom
> -px 좌표 표시 할 수 있음
```
div{
background-position:left top; 
background-position: 100px 200px; (가로방향으로 100px 세로방향으로 200px위치에) 
}
```
>background-attachment
>- 배경이미지를 고정시키는 기능(스크롤을 내려도) 

>background 축약표현
```
background:#fff;
background:url("image.jpg");

```

## 반응형 웹

> OSMU(One Source Multi Use)
>  - One Source: Html
>  - Multi use: CSS, Javascript

> 변경점(break point)
> - 기준 해상도를 설정하고 범위 구간으로 설정

> @media
```
@media 디바이스 and (구간 해상도){
디바이스 스타일
}

@media screen and (max-width:300px){}
@media screen and (min-width:300px){}

// 독립된 구간으로 설정
@media screen and (min-width:360px) and (max-width:700px){
/* 스마트폰 css*/ } 
@media screen and (min-width:701px) and (max-width:1920px){
/* pc css */} 

// 포함된 구간으로 설정
/*pc css */
@media screen and (max-width:700px){
/*스마트폰 css*/}

```

### Javascript

### DOM

### Event 
> 상황 변화에 따라 발생되는 신호

### EVent 발생
- Event 감지: 종류, 상황
- 감지한 event에 맞는 기능, 동작 실행 
-
> Event 종류
> -Mouse Event : click, mouse over, mouse out
> - Keyvord Event: key 입력

> Event 감지 함수
> - javascript: addEventListener()
> - jquery: on()
