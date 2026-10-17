# FPGA 신호등 제어 · 실험 전 레포트

**작성자:** 박건우 (2025440050) · G조  
**저장소:** https://github.com/bandnewbie/UOS_ECE_project5 · 태그 `lab5-pre` · 커밋 `(push 후 기입)`

## 소스
- 설계: [`second_tick.v`](../../lab5_02_traffic/src/second_tick.v), [`traffic.v`](../../lab5_02_traffic/src/traffic.v), [`traffic_lights.v`](../../lab5_02_traffic/src/traffic_lights.v), [`traffic_sequence.v`](../../lab5_02_traffic/src/traffic_sequence.v)
- 최상위: `traffic`
- 테스트벤치: [`sim/tb.sv`](../../lab5_02_traffic/sim/tb.sv) (교안 TB에 파형 덤프 두 줄만 추가)

## 설계와 예상 결과
방향마다 phase 0~10 초록, 11~12 노랑. 보행자 0~3 초록, 4~10 점멸. flicker=1이면 노랑·보행자 빨강 점멸.

## 시뮬레이션 결과
- 로그: [`simulation.txt`](../../evidence/02/vscode/simulation.txt) → `PASS traffic: full cycle, pedestrian blink, flicker, reset`
- 파형: [`wave.vcd`](../../evidence/02/vscode/wave.vcd), `wave.png`(VaporView 캡처 예정)
- CLK_HZ=4(1초=40 ns). direction 525/1045/1565/2085 ns 전환(13초=520 ns). 2090 ns flicker 시 yellow 20 ns 간격 점멸.

## 보드
핀(XDC)은 교안에 없음. 보드 시연 때 연결.

## 참고문헌
[1] Glaysia, ece2_474 STM32 실습 매뉴얼 v1.1.0, https://github.com/Glaysia/ece2_474
