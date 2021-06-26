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





