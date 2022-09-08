# HTML 기본 구조
![image](https://user-images.githubusercontent.com/99263360/189117891-9830a7e7-a63a-4401-831e-d3a0fbc5de6f.png)
***
### 독 타입 (Doctype)
독타입(Doctype)은 HTML문서의 맨 처음에 명시하는 부분으로 문서의 버전에 관한 정보를 나타낸다.  
＜!DOCTYPE html＞은 이 문서가 HTML5 라는 것을 명시한다. 독타입은 문서 처음에 반드시 작성을 해야한다.  

### HTML
문서의 시작과 끝을 알리는 태그 시작 ＜html＞ 끝 ＜/html＞ 해당 웹 문서가 HTML 언어로 작성된 문서임을 브라우저에게 알리는 역할  
lang 속성으로 문서의 언어를 설정할 수 있다.  
```
<html lang="ko">
</html>
```

### 헤드 (head)
헤드(head)는 '문서의 메타데이터 집합'이다. '문서의 메타데이터 집합'은 웹 페이지에는 직접적으로 보이지 않는 정보이다.  
예를 들어, 이 페이지의 제목이나 검색엔진에 노출이 될 지 안될지, 이페이지에 대한 소개글, css파일과 js파일을 연결하는 것들도 ＜head＞에서 이뤄진다.  
#### 1. title
문서의 제목이나 이름을 나타낸다. 안에는 텍스트만 넣을 수 있으며, 문서내에 한번만 사용한다.  
브라우저 창 제목에 나타나며 검색엔진에서는 검색된 페이지의 이름으로 나타난다. title 내용은 적절하고 명료하게 넣어야 한다.  
```
<title>이것은 제목입니다.</title>
```
#### 2. meta
메타에서 담을 수 있는 종류는 여러 종류가 있다. 대표적으로 페이지의 인코딩 방식이나 검색엔진에 관한 정보들,  
다른 브라우저들과의 크로스 브라우징, 반응형, CSS / JS 문서 연결 등등  
```
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" href="css/index.css">
<script src="js/index.js"></script>
<meta name="Keywords" content="키워드의 나열">
<meta name="robots" content="noindex, nofollow">
```

### 바디 (body)
바디(body) 태그는 브라우저 화면에 보이는 것들이 주로 들어간다. 해당 HTML 문서의 텍스트,하이퍼링크,이미지,리스트 등과 같은  
모든 콘텐츠를 포함하는 영역을 정의할 때 사용한다. HTML 문서에는 단 하나의 ＜body＞만 존재할 수 있다.  
```
<body>바디</body>
```

### 주석 (comment)
주석은 브라우저에서 표시되지 않지만, 문서 정리에 도움을 준다.  
HTML의 여러 라인을 한 번에 주석 처리가 가능함으로, 오류 검색을 위한 디버깅에 아주 좋다.  
  
출처 : https://velog.io/@chyori/HTML
