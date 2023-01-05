# Join
- Join은 두 개 이상의 테이블을 묶어서 하나의 결과 집합으로 만들어 내는 것이다.
- 즉, 서로 다른 테이블에서 데이터를 가져올 때 사용하는 것이 Join이다.
***
### INNER JOIN(내부 조인)
- INNER JOIN은 조인 중 가장 많이 사용된다. 보통 JOIN을 얘기할 때는 INNER JOIN을 말하는 것이다.
```
SELECT <열 목록>
FROM <기준 테이블> INNER JOIN <참조 테이블>
ON <조인 조건>
WHERE <검색 조건>;
```
위 형식에서 INNER JOIN이 아닌 그냥 JOIN으로 써도 INNER JOIN으로 인식한다.
실제 테이블에서 예시는 다음과 같다.
```
SELECT H.userID, H.prodID, H.amount, U.name, U.addr, U.phone
FROM Trade History H JOIN User U
ON H.userID = U.userID;
```
"userID"라는 항목이 같다면 ON이 아닌 <code>USING (userID)</code>과 같이 사용해도 된다.
***
### OUTER JOIN(외부 조인)
- INNER JOIN은 양쪽 테이블에 모두 내용이 있는 경우에만 결과가 검색되고, OUTER JOIN은 한쪽 테이블에만 내용이 있어도 결과가 검색된다.
```
SELECT <열 목록>
FROM <첫 번째 테이블(LEFT)>
    <LEFT | RIGHT | FULL> [OUTER] JOIN <두 번째 테이블(RIGHT)>
    ON <조인 조건>
WHERE <검색 조건>;
```
OUTER JOIN은 기준 테이블 내용의 누락 없이 검색하면서도, 대상 테이블의 내용을 가져올 수 있다.  
두 가지 테이블의 내용을 한 번에 가져올 수도 있다.  
<br>
OUTER JOIN 앞에 LEFT를 쓰면 첫 번째 테이블의 내용은 두 번째 테이블과 연계되는 내용이 없더라도 모두 검색되어야 한다는 뜻이다.  
RIGHT를 쓰면 두 번째 테이블의 내용은 모두 검색되어야 한다는 뜻이고,  
FULL은 모든 테이블의 내용이 모두 검색되어야 한다는 뜻이다. <code>OUTER</code>는 생략 가능하다.  
실제 테이블에서 예시는 다음과 같다.
```
SELECT H.prodID, U.userID, U.addr, U.phone
FROM User U LEFT OUTER JOIN History H
ON U.userID = H.userID
WHERE H.prodID IS NULL
ORDER BY U.userID;
```
OUTER JOIN을 이용하면 구매내역이 없는 유저만을 검색할 수 있다.
***
### CROSS JOIN(상호 조인)
- CROSS JOIN은 한쪽 테이블의 행 하나당 다른 쪽 테이블의 모든 행 하나씩 모든 행들을 각각 조인한다.  
- CORSS JOIN의 결과 행의 개수는 [A 테이블 행의 개수 X B 테이블 행의 개수]가 된다.
```
SELECT * FROM ATable
CROSS JOIN BTable;
```
INNER와 OUTER 조인과 달리 ON 구문은 사용하지 않는다.
***
### SELF JOIN (자체 조인)
- SELF JOIN은 자신에게 조인하는 것이다. 같은 테이블에 두 번 참조해야 하는 경우도 있다.
곤충 도감 테이블에서 '메뚜기'의 천적 곤충의 이름, 천적, 수명을 검색하려면 다음과 같이 작성해야 한다.
```
SELECT 이름, 천적, 수명
FROM 곤충테이블
WHERE 이름 = ( SELECT 천적
               FROM 곤충테이블
               WHERE 곤충 = '메뚜기');
```
위의 형식으로 서브 쿼리문을 이용할 수 있지만,
```
SELECT B.곤충, B.천적, B.수명
FROM 곤충도감 A
    INNER JOIN 곤충도감 B
    ON A.천적 = B.곤충
WHERE A.곤충 = '메뚜기';
```
위와 같이 SELF JOIN을 사용하여 정보를 확인할 수도 있다.  
SELFT JOIN을 사용할 때에는 반드시 별칭을 이용해서 논리적으로 두 개의 테이블을 분리시켜야 한다.  
<br>
출처 : https://jaehoney.tistory.com/55
