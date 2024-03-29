
# 📚 프로세스와 스레드

## 📌 프로세스의 개요

### 프로그램과 프로세스

- 프로그램은 저장장치에 저장되어 있는 정적인 상태
- 프로세스는 실행을 위해 메모리에 올라온 동적인 상태

### 태스크(task)

- 프로세스는 컴퓨터 시스템의 작업 단위로 태스크(task)라고도 부른다

### 프로그램에서 프로세스로의 전환

- 프로그램이 프로세스가 된다 => 운영체제로부터 프로세스 제어 블록을 얻는다
- 프로세스가 종료된다 => 해당 프로세스 제어 블록이 폐기된다.

### 프로세스 상태

- 생성 상태 => 메모리 할당,  프로세스 제어 블록 생성
- 준비 상태 => 실행을 기다리는 모든 프로세스가 자기 차례를 기다리는 상태. 실행될 프로세스를 CPU 스케줄러가 선택 (dispatch 준비 -> 실행)
- 실행 상태 => 선택된 프로세스가 타임 슬라이스를 얻어 CPU를 사용하는 상태. 프로세스 사이의 문맥 교환이 일어난다. (timeout:실행->준비, exit:실행->완료, block:실행->대기)
- 대기 상태 => 실행 상태에 있는 프로세스가 입출력을 요청하면 입출력이 완료될 떄까지 기다리는 상태. 입출력이 완료되면 준비 상태로 이동. (wakeup: 대기 -> 준비)
- 완료 상태 => 프로세스가 종료된 상태. 사용하던 모든 데이터가 정리된다.

### 활성상태와 보류상태

- 활성상태 : 생성,준비,실행,대기,완료
- 보류상태 : 보류준비상태, 보류대기상태

### 휴식상태와 보류상태

- 휴식 상태 : 메모리에 있으나 멈춘 상태
- 보류 상태 : 메모리에서 잠시 쫓겨난 상태. 메모리 밖으로 쫓겨나 스왑 영역에 보관

## 📌 프로세스 제어 블록과 문맥 교환

### 프로세스 제어 블록(PCB)

- 프로세스를 실행하는 데 필요한 중요 정보를 보관하는 자료 구조(Task Control Block)

### 프로세스 제어 블록의 구성

- 포인터
- 프로세스 상태
- 프로세스 구분자(PID)
- 프로그램 카운터
- 프로세스 우선순위
- 각종 레지스터 정보 : 레지스터의 중간값 저장
- 메모리 관리 정보
- 할당된 자원 정보 : 프로세스를 실행하기 위해 사용하는 입출력 자원이나 오픈 파일 등에 대한 정보
- 계정 정보
- 부모 프로세스 구분자와 자식 프로세스 구분자

### 문맥 교환(context switching)

- CPU를 차지하던 프로세스가 나가고 새로운 프로세스를 받아들이는 작업
- 두 프로세스의 프로세스 제어블록을 교환하는 작업
- 기존 실행하던 프로세스(P1)를 PCB1에저장. 실행할 P2를 PCB2에서 상태를 가져옴.

## 📌 프로세스의 연산

### 프로세스 구조

- 코드 영역 : 프로그램의 본문이 기술(프로그램의 코드. 읽기 전용)
- 데이터 영역 : 변수나 파일 등의 각종 데이터 (상수는 읽기 전용이지만 대부분의 변수는 읽기와 쓰기 가능)
- 스택 영역 : 운영체제가 프로세스를 실행하기 위해 부수적으로 필요한 데이터를 모아놓은 곳 ex) 함수를 호출하고 원래 프로그램으로 되돌아올 위치 (사용자에게는 보이지 않음)

### 프로세스 복사

- fork() => 프로세스를 복사

### fork() 시스템 호출의 장점

- 프로세스 생성 속도가 빠름
- 추가 자원 없이 자원을 상속할 수 있다. ex) 부모 프로세스가 파일 A를 사용하기 위해 초기화 했다면 자식프로세스는 파일 A를 바로 사용할 수 있다.
- 시스템 관리를 효율적으로 가능

### 프로세스 전환

- exec() => 기존 프로세스를 새로운 프로세스로 전환. 프로세스는 그대로 둔채 내용만 바꾸는 시스템 호출. 현재의 프로세스가 완전히 다른 프로세스로 전환된다.

### exec() 시스템 호출의 장점

- 프로세스 구조체를 재활용 (이미 만들어진 프로세스 제어 블록, 메모리 영역, 부모-자식 관계를 그대로 사용)
- 코드 영역만 가져오면 되기 때문에 운영체제의 작업 수월

### 프로세스 계층 구조의 장점

- 여러 작업의 동시 처리
- 자원 회수 용이 => 프로세스 간의 책임관계가 분명(부모 프로세스가 자식 프로세스를 회수하면 됨)

# 고아 프로세스, 좀비프로세스

- 고아 프로세스 : 부모 프로세스가 자식 프로세스보다 먼저 종료
- 좀비 프로세스 : 자식 프로세스가 종료 했음에도 부모가 자원회수 x

## 📌 스레드

### 스레드

- 프로세스 코드에 정의된 절차에 따라 CPU에 작업 요청을 하는 실행 단위
- 프로세스끼리는 약하게 연결되어 있는 반면 스레드끼리는 강하게 연결되어 있다.

### 스레드 관련 용어

- 멀티스레드 : 프로세스 내 작업을 여러 개의 스레드로 분할
- 멀티태스킹 : 운영체제가 CPU에 작업을 줄 때 시간을 잘게 나누어 배분하는 기법(시분할 시스템). 시분할 시스템에서 운영체제가 CPU에 전달하는 작업은 프로세스가 아니라 스레드
- 멀티프로세싱 : CPU를 여러 개 사용하여 여러 개의 스레드를 동시 처리하는 작업. (병렬처리에서의 슈퍼스칼라 기법)
- CPU 멀티스레드 : 하드웨어적인 방법으로 하나의 CPU에서 여러 개의 스레드를 동시 처리하는 병렬 처리 기법

###  멀티스레드 장단점

- 응답성 향상 : 한 스레드가 입출력으로 작업이 진행되지 않더라고 다른 스레드는 작업을 계속 진행.
- 자원 공유 : 한 프로세스 내에서 독립적인 스레드를 생성하면 프로세스가 가진 자원을 모든 스레드가 공유하게 되어 작업을 원활하게 진행
- 효율성 향상 : 프로세스를 여러개 사용할 때보다 자원의 중복을 막음
- 다중 CPU 지원 : 2개 이상의 CPU를 가진 컴퓨터에서 멀티스레드를 동시에 처리하여 CPU 사용량 증가 및 프로세스 처리 시간 감소

### 멀티스레드 모델

- 커널 스레드: 커널이 직접 생성하고 관리하는 스레드
- 사용자 스레드: 라이브러리에 의해 구현된 일반적인 스레드(대기 상태에 들어가면 모든 사용자 스레드가 같이 대기 => 커널 입장에서는 하나의 프로세스 또한 여러개 CPU 사용불가)
- 멀티레벨 스레드: 사용자 스레드 + 커널 스레드

## 📌 [심화] 동적 할당 영역과 시스템 호출

### 프로세스 영역

- 정적 할당 영역 : 코드영역, 데이터 영역
- 동적 할당 영역 : 힙 영역, 스택 영역

### exit()

- 자식 프로세스가 끝났음을 부모 프로세스에 알려주기 위함

### wait()

- 자식 프로세스가 끝나기를 기다렸다가 자식 프로세스가 종료되면 다음 문장을 실행
