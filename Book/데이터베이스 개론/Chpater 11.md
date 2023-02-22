
# 📚 보안과 권한 관리

## 📌 보안

### 데이터베이스 보안의 목표

- 조직에서 허가한 사용자만 데이터베이스에 접근할 수 있도록 통제하여 보안을 유지하는 것

### 데이터베이스 보안의 유형

- 물리적 환경에 대한 보안 => 자연 재해 등으로부터 보호
- 권한 관리를 통한 보안 => 권한이 없는 사용자로부터 보호
- 운영 관리를 통한 보안 => 권한이 있는 사용자로부터 보호

## 📌 권한 관리

### 권한 관리

- 객체에 대한 권한은 해당 객체의 소유자가 부여하지만 시스템 권한은 데이터베이스 관리자가 부여할 수 있다.

### 권한의 부여 및 취소

- 객체의 소유자가 다른 사용자에게 객체에 대한 사용권한을 부여 및 취소
- WITH GRANT OPTION => 권한을 부여받은 사용자가 자신이 부여받은 권한을 다른 사용자에게도 부여가능
- CASCADE => 권한이 취소 당할 사용자가 다른사람에게 부여했던 권한도 연쇄적으로 함께 취소
- RESTRICT => 권한 취소 될 사용자만 취소

- GRANT 권한 ON 객체 TO 사용자 \[WITH GRANT OPTION]
    - GRANT SELECT ON 고객 TO Hong
- REVOKE 권한 ON 객체 FROM 사용자 CASCADE | RESTRICT
    - REVOKE SELECT ON 고객 FROM Hong CASCADE

### 시스템 권한과 관련된 권한 작업

- 데이터베이스 관리자만 가능
- 시스템 권한은 특정 객체에 한 작업이 아닌, 데이터베이스 관리와 관련된 작업에 대한 권한
- 테이블 생성할 수 있는 CREATE TABLE, 뷰를 생성할 수 있는 CREATE VIEW 등 데이터 정의어(DDL)과 관련된 작업에 대한 권한들

- GRANT 권한 TO 사용자
    - GRANT CREATE TABLE TO Song
- REVOKE 권한 FROM 사용자
    - REVOKE CREATE TABLE FROM Hong

### 역할의 부여와 취소

- 역할을 생성, 역할을 사용자에게 부여, 사용자에게 부여한 역할을 취소, 역할 삭제 => 데이터베이스 관리자

- CREATE ROLE 롤이름
- DROP ROLE 롤이름
- GRANT 롤이름 TO 사용자
- REVOKE 롤이름 FROM 사용자

- 역할에 객체와 관련된 권한을 넣는 작업 => 객체의 소유자

- GRANT 권한 ON 객체 TO 롤이름


