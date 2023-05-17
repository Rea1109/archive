## SQL 시작하기

- Structured Query Language <b>RDBMS</b> 표준 사용법  
  
- RDBMS
  - Relational Database Management System 
  - 관게형 데이터베이스를 생성하고 수정하고 관리할 수 있는 소프트웨어
    ![](./images/RDBMS.png)*RDBMS*

- RDB
  - Relational Database 관계형 데이터 모델
  - 데이터를 2차원의 테이블 형태로 표현
    ![](./images/RDB.png)*RDB*

## sql query 종류

  ```sql
    c/n : column name
    t/n : table name
    -- : SQL 주석
    keyword : 대문자

    SELECT
    c/n[,c/n]
    FROM t/n[,t/n]
    [WHERE 조건[AND 조건]]
    [GROUP BY c/n[,c/n]]
    [HAVING 조건[AND 조건]]
    [ORDER BY c/n [,c/n]]
  ```

  ### 조회, 검색 / Select ⇒ Query

  ```sql
      SELECT 
      c/n
      FROM 
      t/n ;

      SELECT SYSDATE 
      FROM DUAL;

      SELECT * -- *는 모든값을 뜻함
      FROM t/n 
  ```

  ### 입력, 수정, 삭제 / Insert, Update, Delete ⇒ DML : Data Manipulation Language

  ```sql
      INSERT
      INTO t/n (c/n[,c/n])
      VALUES (각 칼럼에 값,[칼럼 값])

      INSERT
      INTO t/n --각 칼럼의 값을 모두 넣을때는 칼럼명 생략 가능 단 순서중요
      VALUES (칼럽값,[칼럽값]) 
  ```

  ```sql
      UPDATE t/n
      SET 바꿀 c/n = 바꿀 값 --해당 c/n의 값을 바꾸겠다.
      WHERE 조건 --해당 c/n의 조건

      UPDATE emp_test
      SET dept_name = '관리부' --SQL에서 문자는 ''표현
      WHERE title = '영업부';

      UPDATE emp_test
      SET dept_name = '대기발령'
      WHERE dept_name IS NULL; --NULL의 비교는 false , IS 사용

      UPDATE emp_test
      SET dept_name = '대기발령'
      WHERE dept_name IS NOT NULL;
  ```

  ```sql
      UPDATE t/n
      SET 바꿀 c/n = 바꿀 값 --해당 c/n의 값을 바꾸겠다.
      WHERE 조건 --해당 c/n의 조건

      UPDATE emp_test
      SET dept_name = '관리부' --SQL에서 문자는 ''표현
      WHERE title = '영업부';

      UPDATE emp_test
      SET dept_name = '대기발령'
      WHERE dept_name IS NULL; --NULL의 비교는 false , IS 사용

      UPDATE emp_test
      SET dept_name = '대기발령'
      WHERE dept_name IS NOT NULL;
  ```
  
  ### table 생성, 삭제, 수정 / Create, Drop, Alter ⇒ DDL : Data Definition Language

  ```sql
      UPDATE t/n
      SET 바꿀 c/n = 바꿀 값 --해당 c/n의 값을 바꾸겠다.
      WHERE 조건 --해당 c/n의 조건

      UPDATE emp_test
      SET dept_name = '관리부' --SQL에서 문자는 ''표현
      WHERE title = '영업부';

      UPDATE emp_test
      SET dept_name = '대기발령'
      WHERE dept_name IS NULL; --NULL의 비교는 false , IS 사용

      UPDATE emp_test
      SET dept_name = '대기발령'
      WHERE dept_name IS NOT NULL;      
  ```