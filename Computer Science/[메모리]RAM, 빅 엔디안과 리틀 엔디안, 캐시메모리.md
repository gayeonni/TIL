## 메모리
- 휘발성 저장장치
- 비휘발성 저장장치
---

### RAM
- 메인 메모리와 상동
- 휘발성 저장장치
- 저장장치에 순차적 접근 필요 없이 곧장 접근 가능한 방식
- 임의 접근 메모리, 직접 접근
<br/>

### RAM의 종류
**1) DRAM**
- 시간이 지남에 따라 저장된 데이터가 사라지는 RAM
- 일반적으로 사용하는 메모리
<br/>

**2) SRAM**
- 시간이 지나도 저장된 데이터가 사라지지 않는 RAM
- 전원이 끊기면 내용이 소실되기 때문에 비휘발성 저장장치
- 보통 캐시 메모리로 사용된다.(DRAM보다 빠르고 비싸다.)
<br/>

**3) SDRAM**
- 클럭 신호에 맞게 CPU와 정보를 주고받을 수 있는 DRAM
<br/>

**4) DDR SDRAM**
- 데이터를 주고 받는 길의 너비인 **대역폭**을 넓혀 속도가 보다 빠른 SDRAM
<br/>
아래의 RAM들은 각각 대역폭이 두 배씩 차이난다. <br/>
DDR4 SDRAM > DDR3 SDRAM > DDR2 SDRAM > DDR SDRAM > SDRAM <br/>
DDR4 SDRAM은 SDRAM에 비해 대역폭이 16배 넓다. <br/>

---

## 빅 엔디안과 리틀 엔디안
- 메모리는 데이터를 바이트 단위로 저장한다.
- 메모리는 CPU로부터 데이터를 워드 단위로 받아(4바이트, 8바이트) 한 주소에 1바이트씩 저장한다.
<br/>

### 빅 엔디안
- 낮은 번지의 주소에 상위 바이트부터 저장하는 방식
- ex) a1a2a3a4는 아래와 같이 저장된다. <br/>

| 메모리 |       |
|----|----------|
| a4 | 높은 번지 |
| a3 |           |
| a2 |           |
| a1 | 낮은 번지 |

<br/>

### 리틀 엔디안
- 낮은 번지의 주소에 하위 바이트부터 저장하는 방식
- ex) a1a2a3a4는 아래와 같이 저장된다. <br/>

| 메모리 |       |
|----|----------|
| a1 | 높은 번지 |
| a2 |           |
| a3 |           |
| a4 | 낮은 번지 |
---
## 캐시 메모리
- CPU의 연산 속도와 메모리 접근 속도의 차이를 줄이기 위한 SRAM 기반의 저장장치
- CPU가 사용할 법한 것을 저장한다.
- 데이터 접근에 있어 단독 DRAM 사용에 비해 빠른 성능은 보장할 수 있으나 메모리와 캐시메모리, 코어별 캐시 메모리의 **불일치**가 발생할 수 있어 **데이터의 일관성**을 유지하는 것이 중요하다.
- L1 캐시: 코어와 가장 가까운 캐시 메모리
- L2 캐시: 그 다음으로 가까운 캐시 메모리
- L3 캐시: L2 다음으로 가까운 캐시 메모리
- L1, L2는 코어 내부, L3는 외부에 위치한다. <br/>

**캐시 메모리의 크기와 속도 비교** <br/>
크기: L1 < L2 < L3 <br/>
속도: L3 < L2 < L1 <br/><br/>

**L1 캐시**
- L1I 캐시: 명령어만 저장하는 L1 캐시
- L1D 캐시: 데이터만 저장하는 L1 캐시
<br/>

**캐시 히트**
- 캐시 메모리가 예측해서 저장한 데이터가 CPU가 사용했을 경우
- 참조 지역성의 원리에 따라 메모리에서 가져올 데이터를 결정한다.
- **`시간 지역성과 공간 지역성`**
- 시간 지역성: CPU는 최근 접근한 메모리 공간에 다시 접근하려는 경향이 있다.
- 공간 지역성: CPU는 접근한 메모리 공간 근처에 접근하려는 경향이 있다.
<br/>

**캐시 미스**
- 캐시 메모리가 예측에 실패해 CPU가 메모리에서 필요한 데이터를 직접 가져와야 하는 경우
<br/>
