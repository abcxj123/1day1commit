# 사용자 정의 함수
- 사용자 정의 함수(User-Defined Function)란 절차형 SQL을 활용하여 일련의 SQL 처리를 수행하고, 수행 결과를 단일 값으로 반환할 수 있는 절차형 SQL이다.
- DBMS에서 제공되는 공통적 함수 이외에 사용자가 직접 정의하고 작성할 수있다.
***
### 사용자 정의 함수 구성
- 기본적인 개념 및 사용법, 문법 등은 프로시저와 동일하다.
- **종료 시 단일 값을 반환한다는 것**이 프로시저와 가장 큰 차이점이다.
- 사용자 정의함수의 호출을 통해 실행되며, 반환되는 단일 값을 조회 또는 삽입, 수정 작업에 이용하는 것이 일반적이다.
#### 사용자 정의 함수 구성 요소
1. 선언부(DECLARE) : 사용자 정의 함수의 명칭, 변수와 인수 그리고 그에 대한 데이터 타입을 정의하는 부분
2. 시작/종료부(BEGIN/END) : 사용자 정의 함수의 시작과 종료를 표현하는데 필수적이며 BEGIN/END가 쌍을 이루어 추가되므로  
  블록으로 구성, 다수 실행을 제어하는 기본적 단위가 되며 논리적 프로세스를 구성
4. 제어부(CONTROL) : 기본적으로는 순차적으로 처리, 비교 조건에 따라 블록 또는 문장을 실행, 조건에 따라 반복 실행
5. SQL : 조회 용도로 SELECT 문을 사용, 데이터를 조작하는 INSERT, UPDATE, DELETE는 사용할 수 없음
6. 예외부(EXCEPTION) : BEGIN~END 절에서 실행되는 SQL문이 실행될 때 예외 발생 시 예외 처리 방법을 정의하는 처리부
7. 반환부(RETURN) : 호출문에 대한 함수 값을 반환
***
#### 1. 선언부(DECLARE)
```
CREATE FUNCTION 함수명
(
파라미터_명 MODE 데이터_타입
)
IS
RETURN 데이터_타입
변수 선언

CREATE OR REPLACE FUNCTION 함수명
(
파라미터_명 MODE 데이터_타입
)
AS
RETURN 데이터_타입
변수 선언
```
1. CREATE : DBMS 내에 객체(트리거, 함수, 프로시저)를 생성, OR REPLACE는 기존 사용자 정의함수가 존재 시 현재 컴파일하는 내용으로 덮어쓴다.
2. FUNCTION : 사용자 정의 함수(FUNCTION)를 사용한다는 의미
3. 함수명 : 해당 사용자 정의함수를 지칭하는 이름
4. 파라미터_명 : 사용자 정의함수와 운영체제 간 필요한 값을 전송하기 위한 인자
5. MODE : 변수의 입출력을 구분, IN(사용자 정의함수로 값 전달), OUT(사용자 정의함수에서 처리된 결과), INOUT(IN과 OUT의 두 가지 기능을 모두 수행) 3가지로 구성
6. 데이터_타입 : 파라미터에 대한 데이터 타입
7. IS/AS : PL/SQL의 블록을 시작, IS 또는 AS를 작성
8. 변수 선언 : 사용자 정의함수 내에서 사용할 변수와 변수에 대한 초깃값을 설정
#### 2. 시작/종료부(BEGIN/END)
- 사용자 정의함수의 실행과 종료를 알려주는 부분으로 사용자 정의함수에 BEGIN, END는 반드시 포함되어야 한다.
#### 3. 제어부(CONTROL)
- 단위 블록별 실행흐름을 제어하는 부분으로 크게 IF문과 CASE문으로 나뉜다.
#### 4. SQL
- 데이터 관리를 위한 조회, 추가, 수정, 삭제를 수행하는 부분이다.
- INSERT, UPDATE, DELETE를 통한 데이터 조작은 할 수 없다.
- **SELECT를 통한 조회만 가능하다.**
#### 5. 예외부(EXCEPTION)
- 실행 중 발생 가능한 예외상황을 수행하는 부분이다.
#### 6. 반환부(RETURN)
- RETURN 명령을 통해 사용자 정의함수 종료 시 사용자 정의함수를 호출한 쿼리에 반환하는 단일 값을 정의한다.
#### 7. 사용자 정의함수 호출문
- 함수명(파라미터1, 파라미터2...)
***
### 사용자 정의함수 예시
1. 작성
```
-- 선언부
CREATE FUNCTION TEST_FUNC
(
V_DATE IN CHAR(8)
)
IS

-- 시작/종료부
BEGIN
  V_CURR_YEAR CHAR(4);
  V_BIRTH_YEAR CHAR(4);
  V_AGE NUMBER;

-- 제어부
IF V_DATE > "21210216" THEN
SET
  V_DATE = "20191231";
END IF;

-- SQL
SELECT TO_CHAR(SYSDATE, 'YYYY'), SUBSTR(V_DATE, 1, 4)
INTO V_CURR_YEAR, V_BIRTH_YEAR
FROM DUAL;

SET V_AGE = TO_NUMBER(V_CURR_YEAR) - TO_NUMBER(V_BIRTH_YEAR) + 1;

-- 반환부
RETURN V_AGE;

END;
```
2. 실행 방법
```
SELECT TEST_FUNC('19900101') FROM DUAL;

UPDATE TABLE_NAME 
SET COL_1 = TEST_FUNC(COL_2)
WHERE COL_2 = '20201031';
```

<br>
출처 : https://benggri.tistory.com/77
