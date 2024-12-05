#  RISC-V based system software development for open ecosystem of SDR

<br>

## Overview
 * 오픈소스를 활용한 지능형 SDR 응용 프로그램의 실행을 위하여 RISC-V를 지원 하도록 운영.
 * 리눅스 커널, 시스템 라이브러리, 각종 관리 도구 등을 포함하는 시스템 소프트웨어 배포판 관련 레포지토리로 구성.
 * 배포판과 ROS2를 연계하여 운영할 수 있도록 하는 개발 환경 구축을 위한 레포지토리로 구성.

<br>

## What is Vela
 * 개방형 SDR 소프트웨어 생태계 강화를 위하여 RISC-V 하드웨어 확장 기술 연계 저전력,고효율, 고신뢰, 고가용 실행환경 지원 개방형 시스템 소프트웨어 기술 개발

### 운영체제 
 * 원활한 지능형 SDR 응용실행을 위해 RISC-V 지원 리눅스 커널,시스템 라이브러리, 각종 관리 도구 등을 포함하는 시스템 소프트웨어 배포판 개발 및 통합
### 검증환경
 * RISC-V ISA 및 non-ISA 확장 기능의 개발과 기능/성능 검증을위한 에뮬레이터/시뮬레이터/FPGA 기반 개발 및 검증 환경 개발
### 저전력
 * RISC-V 코어와 다수의 AI실행엔진으로 구성되는 이기종 환경에서성능 모니터링 정보 기반 정적/동적 전력 절감 및 발열 관리 기술 개발
### 고효율
 * SDR을 위한 ISA확장 AI실행엔진, 지능형 로봇 응용의 멀티모델 통합 스케줄링과 전력/발열인지 스케줄링 기반 고효율 컴퓨팅 기술 개발
###고신뢰
 * 코드의 수정 또는 재컴파일 없이 안전한 응용 실행이 가능한 신뢰VM 제공 기술 및 RISC-V코어와 AI실행엔진 그리고 다른 노드/시스템의 자원까지 고신뢰 컴퓨팅 확장이 가능한 고성능 신뢰실행환경 기술 개발
### 고가용
 * 오류 상황에서 시스템 가용성을 높이기 위해 RERI(RAS Error-recordRegister Interface)기반 에러 분석/보고 기능과 에러 예측/분리 지원 기술 개발
### 툴체인
 * AI실행엔진 및 저전력/고효율/고신뢰/고가용 지원 확장 ISA 코드 생성을 위한 컴파일러 포함 툴체인 도구와 성능최적화 지원 프로파일러 개발
### 응용최적화
 * SDR의 응용특성 분석 기반 응용 최적화 시나리오 개발과 지능형 SDR응용간 메시지 통신가속 지원 응용 최적화 기술 개발


<br>

## Getting Started
<br>

### System Install 

### Cloning the Source Repositories 

```shell
$ git clone https://github.com/riscv-vela/ubuntu-ros2-dev
   blabla
```

### Building 

```shell
$ cd ubuntu-ros2-dev
$ ./build.sh
   blabla
```

### Test 
```shell
$ Test
   blabla
```
