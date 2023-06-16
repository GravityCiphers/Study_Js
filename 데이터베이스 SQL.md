# 데이터베이스 SQL

## SQL (Structured Query Language)

ㄴ**관계형 데이터베이스에 정보를 저장하고 처리하기 위한 프로그래밍 언어**입니다.

![img.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cb9f059e-2012-4ec9-bda0-dfb2ab333832/img.png)

## **SQL문의 종류**

SQL 문은 DML문, TCL문, DDL문, DCL문으로 구분된다.

| 종류                              | 구문                          | 설명                                                                                                      |
| --------------------------------- | ----------------------------- | --------------------------------------------------------------------------------------------------------- |
| DML(Data Manipulation Language)   | SELECTINSERTUPDATEDELETEMERGE | 테이블에 저장된 데이터를 조작(조회, 입력, 수정, 삭제)하기 위한 구문                                       |
| TCL(Transaction Control Language) | COMMITROLLBACKSAVEPOINT       | DML문에 의한 데이터의 변경 사항을 데이터베이스에 영구히 반영하거나 취소하기 위해 트랜잭션을 제어하는 구문 |
| DDL(Data Definition Language)     | CREATEALTERDROPRENAMETRUNCATE | 테이블, 인덱스와 같은 데이터베이스 오브젝트의 구조를 정의(생성, 변경, 삭제)하기 위한 구문                 |
| DCL(Data Control Language)        | GRANTREVOKE                   | 데이터에 대한 권한을 부여하거나 취소하기 위한 구문                                                        |

## **SQL의 언어적 특징**

각 프로그래밍 언어가 가진 고유의 특성은 꼭 구별지어 알아두어야 사용할 때 오류를 줄일 수 있습니다. SQL은 다음과 같은 언어적 특성을 갖습니다.

1. SQL은 **대소문자**를 가리지 않습니다.

   (단, 서버 환경이나 DBMS 종류에 따라 데잍터베이스 또는 필드명에 대해 대소문자를 구분하기도 합니다.

2. SQL 명령은 **반드시 세미콜론(;)으로 끝**나야 합니다.
3. **고유의 값**은 **따옴표(”)**로 감싸줍니다.

   ex)

   ```sql
   SELECT * FROM EMP WHERE NAME = 'James';
   ```

4. SQL에서 **객체**를 나타낼 때는 **백틱(``)**으로 감싸줍니다.

   ex)

   ```sql
   SELECT `COST`, `TYPE` FROM `INVOICE`;
   ```

5. **주석**은 일종의 도움말로, 주석 처리된 문장은 프로그램에서 동작하지 않습니다. 한 줄 주석은 문장 앞에 — 를 붙여서 사용합니다.

   ex)

   ```sql
   -- SELECT * FROM EMP; 이 쿼리는 실행되지 않습니다.
   ```

6. 여러 줄 주석은

   ```sql
   /* */
   ```

   로 감싸줍니다.

   ex)

   ```sql
   /*
   SELECT * FROM EMP WHERE EMPID=(SELECT * FROM EMP WHERE NAME='홍길동');
   */
   ```
