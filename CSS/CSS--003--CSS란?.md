# CSS
- CSS(Cascading Style Sheets)는 HTML, XML 같은 문서의 스타일을 꾸밀 때 사용하는 스타일 시트 언어이다.
- HTML로 문서의 뼈대를 만든다면 CSS로는 문서를 꾸밀 수 있다.
- 글꼴이나 배경색, 너비와 높이, 위치 등을 지정하거나 웹 브라우저, 스크린 크기, 장치에 따라 화면을 다르게 표시될 수 있도록 지정할 수도 있다.
- CSS는 문서의 내용(content)와 표현(presentation)을 분리하여 CSS 파일 하나만 수정하면 스타일에 해당하는 HTML 문서가 한 번에 수정되는 장점을 가지고 있다.

### CSS 적용법
- 속성처럼 style 적용
- style tag 사용
- css 파일을 별도로 만들어 html 문서에 연결

### 1. HTML 문서 안에 style 속성 사용(in-line)
```
<html>
  <head>
    <title>문서 제목</title>
  </head>
  <body>
    <h1 style = "color : gray; text-align : center;>
      CSS 스타일 적용하기
    </h1>
  </body>
</html>
```

### 2. style 태그 사용(Internal)
```
<html>
  <head>
    <title>문서 제목</title>
    <style type="text/css">
      h1 {
          color : gray;
          text-align : center;
          }
     </style>
  </head>
  <body>
    <h1>
      CSS 스타일 적용하기
    </h1>
  </body>
</html>
```

### 3. CSS 파일을 별도로 만들어 HTML 문서에 연결(External)
1. 확장자 .css로 저장(ex: text.css)
```
h1 {
    color : gray;
    text-align : center;
    }
```
2. 확장자 .html로 저장(ex: main.html)
```
<html>
  <head>
    <title>문서 제목</title>
    <link rel="stylesheet" type="text/css" href="text.css" />
  </head>
  <body>
    <h1>
      CSS 스타일 적용하기
    </h1>
  </body>
</html>
```
