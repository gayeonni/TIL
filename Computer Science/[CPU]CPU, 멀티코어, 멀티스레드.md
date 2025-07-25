## CPU 클럭 속도
### 클럭
- 컴퓨터의 부품을 움직일 수 있게 하는 시간 단위
- 클럭 속도는 Hz 단위로 측정한다.
- Hz는 클럭이 1초에 몇 번 반복되는지 나타낸다.

## 멀티코어
### 코어
- CPU 내에서 명령어를 읽거나 해석, 실행하는 부품을 의미한다.
- 이 코어는 여러개 존재할 수 있다.
- 코어가 2개 이상이면 멀티코어 CPU(멀티코어 프로세서)로 부른다.

---

## 멀티스레드
### 스레드
- 실행 흐름의 단위
- 하드웨어 스레드와 소프트웨어 스레드(스레드)로 나눌 수 있다.

### 하드웨어 스레드 (=논리 프로세서)
- 하나의 코어가 동시에 처리하는 명령의 단위
- CPU 내의 명령어를 읽고, 해석하고, 실행하는 부품 **하나**가 한 번에 하나의 명령어를 처리한다면 **1코어 1스레드 CPU**
- CPU 내의 명령어를 읽고, 해석하고, 실행하는 부품 **두 개**가 한 번에 네 개의 명령어를 처리한다면 **2코어 4스레드 CPU**

### 소프트웨어 스레드
- 하나의 프로그램에서 독립적으로 실행되는 단위
- 운영체제에서 사용하는 개념
- 어떤 프로그램이 여러 스레드를 통해 실행될 수 있다. == 메모리에 적재된 해당 프로그램을 구성하는 여러 부분이 동시에 실행될 수 있다.
