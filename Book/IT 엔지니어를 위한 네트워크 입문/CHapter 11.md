
# 📚 이중화 기술

## 📌 이중화 기술 개요

### SPoF (Single Point of Failure, 단일 장애점)

- 시스템 구성 요소 중 동작하지 않으면 전체 시스템이 중단되는 요소

### 이중화의 목적

- 안정적인 서비스 제공

## 📌 LACP

### LACP(Link Aggregation Control Protocol)

- 상호호환 가능한 연결 계층 표준화
- 대역폭 확장 => 링크 사용률 향상, 향상된 장애 회복

### LACP 동작 방식

- LACPDU(LACP Data Unit)라는 프레임을 사용
- LACPDU에는 LACP를 구성하기 위한 출발지 주소, 목적지 주소, 타입, 서브 타입, 버전 정보 등을 포함해 매초마다 주고받음
- LACP가 연결되려면 LACPDU를 주고받는 장비가 한 장비여야 한다.

### PXE (Pre-boot eXecution Environment, 사전 부팅 실행 환경)

- 네트워크 인터페이스를 이용하여 컴퓨터를 부팅할 수 있게 만들어 주는 기술
- CD-ROM이나 USB와 같은 데이터 저장소에 구애받지 않고 운영체제 설치 가능
- 수 많은 컴퓨터가 있을때 일일이 저장장치(USB,CD)로 OS를 설치하는 것은 불편하다 => PXE 계기

## 📌 서버의 네트워크 이중화 설정(Windows, Linux)

### 이중화 기술명

- 윈도 : 팀\/team\/티밍\/teaming
- 리눅스 : 본드\/bond\/본딩\/bonding

## 📌 MC-LAG

### MC-LAG(Multi-Chassis Link Aggregation Group)

- 서로 다른 스위치 간의 실제 MAC 주소 대신 가상 MAC 주소를 만들어 논리 인터페이스로 LACP를 구성
- 벤더 별로 기술명이 다름

## 📌 게이트웨이 이중화

### FHRP (First Hop Redundancy Protocol)

- 게이트웨이 이중화 프로토콜
- 두 라우터는 실제 IP 외에 추가로 가상 IP 주소와 가상 IP에 대한 MAC 주소를 동일하게 갖는다.

