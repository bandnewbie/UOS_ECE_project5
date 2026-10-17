# FPGA ADC · 실험 전 레포트

**작성자:** 박건우 (2025440050) · G조  
**저장소:** https://github.com/bandnewbie/UOS_ECE_project5 · 태그 `lab5-pre` · 커밋 `(push 후 기입)`

## 소스
- 설계: [`adc.v`](../../lab5_03_adc/src/adc.v), [`adc_command.v`](../../lab5_03_adc/src/adc_command.v), [`serial_frame16.v`](../../lab5_03_adc/src/serial_frame16.v)
- 최상위: `adc`
- 테스트벤치: [`sim/tb.sv`](../../lab5_03_adc/sim/tb.sv) (교안 TB에 파형 덤프 두 줄만 추가)

## 설계와 예상 결과
채널 명령 16비트를 직렬로 보내고 응답 하위 12비트를 sample, sample[11:4]를 LED로 낸다.

## 시뮬레이션 결과
- 로그: [`simulation.txt`](../../evidence/03/vscode/simulation.txt) → `PASS ADC: 3 serial frames, command bits, sample, reset`
- 파형: [`wave.vcd`](../../evidence/03/vscode/wave.vcd), `wave.png`(VaporView 캡처 예정)
- HALF_CYCLES=2. 프레임 35~675 ns, 명령 16'hAB70(채널 2), 685 ns data_valid, sample=12'h5C3, led=8'h5C.

## 보드
핀(XDC)은 교안에 없음. 보드 시연 때 연결.

## 참고문헌
[1] Glaysia, ece2_474 STM32 실습 매뉴얼 v1.1.0, https://github.com/Glaysia/ece2_474
