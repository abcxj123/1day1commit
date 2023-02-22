# JavaScript
- 자바스크립트(JavaScript)는 객체 기반의 스크립트 프로그래밍 언어이다.
- 자바스크립트는 웹사이트를 디자인하고, 웹페이지가 어떻게 작동할지 제어한다.
- HTML이 웹 문서의 구조(layout)을 결정한다면, CSS는 웹 문서가 어떻게 보일지를 결정하고, JavaScript는 웹 문서가 어떻게 행동할지 제어한다.
- 자바스크립트는 웹 문서가 로드될 때, 브라우저 엔진에 의해 번역되어 자바스크립트가 지원되지 않는 브라우저를 사용하면 작동하지 않을 수 있다.

### 자바와 자바스크립트
- 자바와 자바스크립트는 유사한 점도 있지만, 이는 두 언어 모두 C언의 기본 구문을 바탕으로 했기 때문이다.
- 자바와 자바스크립트는 직접적인 관련성이 없다.

### 자바스크립트 예시
- 자바스크립트는 HTML안에 코드를 넣을 수도 있고, 따로 파일로 저장해서 링크로 연결시킬 수도 있다.

#### 1. HTML 안에 자바스크립트 넣기
```
<html>
  <head>
    <title>
      자바스크립트
    </title>
    <script type="text/javascript">
      alert("This is JavaScript");
    </script>
  </head>
  <body>
  </body>
</html>
```

#### 2. 자바스크립트 파일을 확장자(.js)로 저장하기
1. 확장자 .js로 저장(ex: test.js)
```
alert("This is JavaScript");
```
2. 확장자 .html로 저장(ex: main.html)
```
<html>
  <head>
    <title>
      자바스크립트
    </title>
    <script type="text/javascript" src="test.js"></script>
  </head>
  <body>
  </body>
</html>
```
