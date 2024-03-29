

# 📚 라우터/L3 스위치: 3계층 장비

## 📌 라우터의 동작 방식과 역할

### 라우터 동작 방식

- 경로 지정
- 브로드캐스트 컨트롤
- 프로토콜 변환

### 경로 지정

- 경로 정보를 모아 라우팅 테이블을 만들고 패킷이 라우터에 들어오면 패킷의 IP 주소를 확인해 경로를 지정하고 패킷을 포워딩
- 목적지 주소가 라우팅 테이블에 없으면 버림

### 브로드 캐스트\/멀티캐스트 컨트롤

- 라우터는 멀티캐스트 정보를 습득하지 않고 브로드캐스트 패킷을 전달하지 않음
- 이 기능을 이용해 브로드캐스트가 다른 네트워크로 전파되는 것을 막을 수 있다 => 브로드캐스트\/멀티캐스트 컨트롤

### 프로토콜 변환

- LAN 구간엔 이더넷 프로토콜 => WAN 구간은 PPP와 같은 WAN 프로토콜로 변환이 가능

## 📌 경로 지정 - 라우팅\/스위칭

### 홉-바이-홉(Hop-by-Hop) 라우팅

- 라우터는 목적지까지의 경로를 모두 책임지는 것이 아니라 인접한 라우터까지만 최적의 경로를 지정하면  
인접 라우터에서 최적의 경로를 다시 파악한 후 라우터로 패킷을 포워딩한다.
- 인접한 라우터를 넥스트 홉(Next Hop)이라고 부름

### 라우팅 테이블 구성요소

- 목적지 주소
- 넥스트 홉 IP 주소, 나가는 로컬 인터페이스(선택 가능)

### TTL (Time To Live)

- TTL은 실제 초와 같은 시간이 아니라 홉을 지칭. 하나의 홉을 지날때마다 TTL 값은 1씩 감소

### 라우팅(라우터가 경로 정보를 얻는 방법)

- 다이렉트 커넥티드
- 스태틱 라우팅
- 다이나믹 라우팅

### 다이렉트 커넥티드

- 라우터의 인터페이스에 IP를 설정하면 자동 생성되는 정보

### 스태틱 라우팅

- 관리자가 목적지 네트워크와 넥스트 홉을 라우터에 직접 지정해 경로 정보를 입력하는 것
- 직관적으로 설정, 관리 가능
- 네트워크 수가 많아지면 관리자가 직접 관리하기 한계가 있음

### 다이나믹 라우팅

- 라우터끼리 자신이 알고 있는 경로 정보나 링크 상태 정보를 교환해 전체 네트워크 정보를 학습
- 주기적으로 또는 상태 정보가 변경될 때 라우터끼리 경로 정보를 교환

### 라우팅과 스위칭

- 라우팅 : 다양한 방법으로 경로 정보를 얻고 그 정보 중 최적의 경로로 생각되는 경로를 라우팅 테이블에 올려 유지하는 과정
- 스위칭 : 패킷이 들어와 라우팅 테이블을 참조하고 최적의 경로를 찾아 라우터 외부로 포워딩하는 작업

### 롱기스트 프리픽스 매칭 (Longest Prefix Match)

- 라우터가 패킷을 포워딩할 때 자신이 갖고 있는 라우팅 테이블에서 가장 좋은 항목을 찾는 알고리즘
- 목적지와 가장 유사한 라우팅 경로를 선택하는 알고리즘

### 경로설정 우선순위

1. 롱기스트 매치
2. AD(관리 거리)
3. 코스트
4. 부하 분산(ECMP)

## 📌 라우팅 설정 방법

### 디폴트 라우팅

- 디폴트 게이트웨이와 같은 의미
- 인터넷으로 향하는 경로나 자신에게 경로 정보가 없는 경우, 마지막 대체 경로로 디폴트 라우팅을 사용
- 서버에서 디폴트 게이트웨이를 설정하면 서버의 라우팅 테이블에서 디폴트 라우팅이 생성

