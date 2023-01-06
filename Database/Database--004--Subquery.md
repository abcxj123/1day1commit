# Subquery
- 서브쿼리(Subquery)란 하나의 SQL 문 안에 포함되어 있는 또 다른 SQL문을 말한다.
- 서브쿼리는 메인쿼리가 서브쿼리를 포함하는 종속적인 관계이다.
***
### 서브쿼리를 사용할 때 주의할 점
1. 서브쿼리를 괄호로 감싸서 사용한다.
2. 서브쿼리는 단일 행 또는 복수 행 비교 연산자와 함께 사용 가능하다.
3. 서브쿼리에서는 ORDER BY를 사용하지 못한다. 
### 서브쿼리가 사용이 가능한 곳
- SELECT
- FROM
- WHERE
- HAVING
- ORDER BY
- INSERT문의 VALUES
- UPDATE문의 SET
***
### 단일행 서브쿼리
```
SELECT * FROM PLAYER
WHERE Team_ID = (
        SELECT Team_ID
        FROM PLAYER
        WHERE Player_name = "geon"
        )
ORDER BY Team_name;
```
### 다중행 서브쿼리
```
SELECT * FROM TEAM
WHERE Team_ID IN (
        SELECT Team_ID
        FROM PLAYER
        WHERE Player_name = "geon"
        )
ORDER BY Team_name;
```
### 다중컬럼 서브쿼리
```
SELECT * FROM PLAYER
WHERE (Team_ID, Height) IN (
        SELECT Team_ID, Min(Height)
        FROM PLAYER
        GROUP BY Team_ID
        )
ORDER BY Team_ID, Player_name;
```
***
### SELECT 절에서 사용되는 서브쿼리
```
SELECT Player_name, Height, (
        SELECT AVG(Height)
        FROM PLAYER p
        WHERE p.Team_ID = x.Team_ID) as AVG_Height
FROM PLAYER x
```

<br>
출처 : https://snowple.tistory.com/360
