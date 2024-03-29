
# 📚 관계 데이터 연산

## 📌 관계 데이터 연산의 개념

### 데이터 모델

- 데이터 구조
- 제약조건 
- 연산

### 관계 데이터 모델에서 연산

- 원하는 데이터를 얻기 위해 릴레이션에 필요한 처리 요구를 수행, 데이터베이스 시스템의 구성 요소 중 데이터 언어의 역할

### 관계 데이터 연산의 종류

- 관계 대수 => 원하는 결과를 얻기 위해 데이터의 처리 과정을 순서대로 기술한 언어. 간단히 말해 릴레이션을 처리하는 연산자들의 모임
    - 일반 집합 연산자
    - 순수 관계 연산자
- 관계 해석

## 📌 관계 대수

### 일반 집합 연산자

- 합집합
- 교집합
- 차집합(-)
- 카티션 프로덕트(X)

### 순수 관계 연산자

- 셀렉트   => 릴레이션에서 조건을 만족하는 튜플을 구한다.
- 프로젝트 => 릴레이션에서 주어진 속성들의 값으로만 구성된 튜플을 구한다.
- 조인    => 공통 속성을 이용해 두 릴레이션의 튜플들을 연결하여 생성된 튜플을 구한다 
- 디비전  => 나누는 릴레이션의 모든 튜플과 관련이 있는 튜플을 구한다.

### 확장된 대수 연산자

- 세미 조인 => 조인 속성으로 프로젝트한 릴레이션을 이용해 조인
- 외부 조인 => 조인 연산에서 제외되었던 모든 튜플 결과 릴레이션에 포함시킨다.

## 📌 관계 해석

### 관계 해석

- 원하는 결과를 얻기 위해 처리를 원하는 데이터가 무엇인지만 기술하는 비절차 언어
- 데이터를 처리하는 기능과 처리를 요구하는 표현력에서 관계 대수와 관계 해석은 능력이 모두 동일
- 수학의 프레디킷 해석에 기반을 둔다.
- 튜플 관계 해석과 도메인 관계 해석으로 분류된다.
