### 주제 : #DML #DataManipulationLanguage #조작어

___

### 설명 : 

> DML은 데이터베이스에서 데이터를 검색하거나 조작하는 데 사용되는 데이터 조작 언어입니다. 
> 데이터베이스의 테이블에서 레코드를 추가, 수정, 삭제하거나 데이터를 조회하는데 사용됩니다. 
> DML은 데이터베이스의 내용을 변경하고 조작하는데 중점을 둡니다.

### 명령어 :

>[!note] SELECT :
> 데이터베이스에서 데이터를 조회하는데 사용됩니다. 특정 열이나 레코드를 선택하여 가져오거나 필터링하여 데이터를 검색할 수 있습니다.
> 
> ```
> SELECT count(\*) FROM 테이블명 ;
> ```
>```
> SELECT FirstName, LastName
> FROM Employees
> WHERE Department = 'Sales';
>```

>[!note] INSERT :
> 새로운 데이터를 데이터베이스 테이블에 추가하는데 사용됩니다.
>
> ```
> INSERT INTO 테이블명 VALUES (); 
> INSERT INTO 테이블명() VALUES ();
> ```
> 
>```
> INSERT INTO Employees (FirstName, LastName, Department)
> VALUES ('John', 'Doe', 'Marketing');
>```

>[!note] UPDATE : 
> 데이터베이스 테이블의 기존 데이터를 수정하는데 사용됩니다.
> 
> ```
> UPDATE 테이블명 SET 컬럼명 = 튜플변경값;  
> UPDATE 테이블명 SET 컬럼명 = 튜플변경값 WHERE 조건;
> ```
> 
> ```
> UPDATE Employees
> SET Salary = Salary * 1.1
> WHERE Department = 'Sales';
> ```

>[!note] DELETE :
> 데이터베이스 테이블에서 데이터를 삭제하는데 사용됩니다.
>  개발 프로젝트의 표준은 모든 삭제 데이터에 대한 로그를 남기는 것을 원칙으로 한다. (TRUNCATE, DROP은 로그를 안 남긴다.)
> 
>```
> DELETE FROM 테이블명
> WHERE 조건;
>```
>```
> DELETE FROM Employees
> WHERE Department = 'HR';
>```

>[!note] MERGE : 
> 주로 Oracle에서 사용되며, INSERT, UPDATE, DELETE를 하나의 명령어로 처리할 때 사용됩니다.
> 
>```
> MERGE INTO TargetTable AS T
> USING SourceTable AS S
> ON T.ID = S.ID
> WHEN MATCHED THEN
> UPDATE SET T.Value = S.Value
> WHEN NOT MATCHED THEN
> INSERT (ID, Value) VALUES (S.ID, S.Value);
>```

>[!note] 옵션 : 
> 
> DISTINCT : 중복된 데이터가 있는 경우 1건으로 처리해서 출력
> 
> ```
> SELECT DISTINCT 컬럼명 
> FROM 테이블명 ;
> ```
> 
> GROUP BY : 중복된 데이터가 있는 경우 1건으로 처리해서 출력
> 
> ``` 
> SELECT  컬럼명 
> FROM 테이블명 ;
> GROUP BY 컬럼명 ;
> ```
>
> IS : NULL과 관련될 경우 사용
> 
> ```
> 오라클
> WHERE 컬럼명 IS NULL
> SQL Server
> WHERE 컬럼명 = ''
> ```
> 
> BETWEEN : A~B 사이를 찾을 때(A, B 포함)
> 
> ```
> WHERE 컬럼명 BETWEEN 'A' AND 'B'
> ```
> ```
> WHERE 컬럼명 = '조건' AND 컬럼명 BETWEEN 'A' AND 'B'
> ```


___

### 출처(참고문헌)

- [SQL 쿼리문 보기 좋게 정렬해주는 사이트](https://zzznara2.tistory.com/663)

___

### 연결문서

- [[SQL문]]
- [[과목 2-0]]
- [[과목 2-1]]
