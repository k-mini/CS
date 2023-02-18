
# 📚 데이터베이스 언어 SQL

## 📌 SQL의 소개

### SQL

- 관계 데이터베이스를 위한 표준 질의어. 기능에 따라 데이터 정의어, 데이터 조작어, 데이터 제어어로 나눈다.
- SQL의 분류
    - 데이터 정의어(DDL, Data Definition Language)
    - 데이터 조작어(DML, Data Muanipulation Language)
    - 데이터 제어어(DCL, Data Control Language)

## 📌 SQL을 이용한 데이터 정의

### CREATE TABLE (테이블 생성)

CREATE TABLE 테이블 이름(  
&nbsp;&nbsp;&nbsp;&nbsp;속성_이름 데이터_타입 \[NOT NULL\] \[DEFAULT 기본값\]  
&nbsp;&nbsp;&nbsp;&nbsp;    \[PRIMARY KEY (속성 리스트)\]  
&nbsp;&nbsp;&nbsp;&nbsp;    \[UNIQUE (속성 리스트)\]  
&nbsp;&nbsp;&nbsp;&nbsp;    \[FOREIGN KEY (속성 리스트) REFERENCES 테이블 이름(속성 리스트)\] \[ON DELETE 옵션\] \[ON UPDATE 옵션\]  
&nbsp;&nbsp;&nbsp;&nbsp;    \[CONSTRAINT 이름\] \[CHECK(조건)\]  
);

### ALTER TABLE (테이블 변경)

- ALTER TABLE 테이블_이름 ADD 속성_이름 데이터_타입 \[NOT NULL\] \[DEFAULT 기본 값\];
  
- ALTER TABLE 테이블_이름 DROP COLUMN 속성_이름;

- ALTER TABLE 테이블_이름 ADD CONSTRAINT 제약조건_이름 제약조건_내용;

- ALTER TABLE 테이블_이름 DROP CONSTRAINT 제약조건_이름;

### DROP TABLE (테이블 삭제)

- DROP TABLE 테이블_이름;

## 📌 SQL을 이용한 데이터 조작

### SELECT (데이터 검색)

SELECT \[ ALL | DISTINCT \] 속성_리스트  
&nbsp;&nbsp;&nbsp;&nbsp;    FROM 테이블_리스트  
&nbsp;&nbsp;&nbsp;&nbsp;    \[ WHERE 조건 \]  
&nbsp;&nbsp;&nbsp;&nbsp;    \[ GROUP BY 속성_리스트 \[ HAVING 조건 \] \]  
&nbsp;&nbsp;&nbsp;&nbsp;    \[ ORDER BY 속성_리스트 \[ ASC | DESC \] \]  
;

SELECT 속성_리스트  
&nbsp;&nbsp;&nbsp;&nbsp;    FROM 테이블1 INNER JOIN 테이블2 ON 조인조건  
\[ WHERE 검색조건 \]  

SELECT 속성_리스트  
&nbsp;&nbsp;&nbsp;&nbsp;    FROM 테이블1 LEFT|RIGHT|FULL OUTER JOIN ON 테이블2 ON 조인조건  
\[ WHERE 검색조건 \]  

### INSERT (데이터 삽입)

INSERT INTO 테이블_이름\[(속성_리스트)\] VALUES (속성값_리스트);

INSERT INTO 테이블_이름\[(속성_리스트)\] SELECT 문;

### UPDATE (데이터 수정)

UPDATE 테이블_이름  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;     SET 속성_이름1 = 값1, 속성_이름2 = 값, ...  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;     \[ WHERE 조건 \];

### DELETE (데이터 삭제)

DELETE  
&nbsp;    FROM 테이블_이름  
&nbsp;    \[ WHERE 조건\];

## 📌 뷰

### 뷰

- 다른 테이블을 기반으로 만들어진 가상 테이블. 기반이 되는 물리적인 테이블을 기본 테이블이라 부른다.
- 일반 테이블 처럼 검색,삽입,수정,삭제가 가능 => 기본 테이블의 데이터에 영향을 끼친다.

### 뷰 주의점

- 기본 테이블에서 어떤 튜플을 어떻게 변경해야 할지 명확히 제시하지 못하는 뷰는 변경이 허용되지 않는다.
- 기본 테이블의 기본키를 구성하는 속성이 포함되어 있지 않은 뷰는 변경할 수 없다.
- 집계 함수처럼 새로 계산된 내용을 포함하고 있는 뷰는 변경할 수 없다.
- DISTINCT 키워드를 포함하여 정의한 뷰는 변경할 수 없다.
- GROUP BY 절을 포함하여 정의한 뷰는 변경할 수 없다.
- 여러 개의 테이블을 조인하여 정의한 뷰는 변경할 수 없는 경우가 많다.

### 뷰의 장점

- 질의문을 좀 더 쉽게 작성할 수 있다.
- 데이터의 보안 유지에 도움이 된다.
- 데이터를 좀 더 편리하게 관리할 수 있다.

### 뷰의 생성

CREATE VIEW 뷰_이름\[(속성_리스트)\]  
&nbsp;&nbsp;&nbsp;&nbsp;  AS SELECT 문  
&nbsp;&nbsp;&nbsp;&nbsp;\[ WITH CHECK OPTION \];

### 뷰의 삭제

- DROP VIEW 뷰_이름;

## 📌 삽입 SQL

### 삽입 SQL

- 커서 : 수행 결과로 반환된 행들을 한 번에 하나씩 가리키는 포인터
- 커서가 필요 없는 삽입 SQL : CREATE TABLE / INSERT / DELETE / UPDATE / 행 하나를 결과로 반환하는 SELECT
- 커서가 필요한 삽입 SQL : 여러 행을 결과로 반환하는 SELECT  




