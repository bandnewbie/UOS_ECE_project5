# FPGA 피아노 · 실험 전 레포트

**작성자:** 박건우 (2025440050) · G조  
**저장소:** https://github.com/bandnewbie/UOS_ECE_project5 · 태그 `lab5-pre` · 커밋 `(push 후 기입)`

## 소스
- 설계: [`note_select.v`](../../lab5_01_piano/src/note_select.v), [`piano.v`](../../lab5_01_piano/src/piano.v), [`square_tone.v`](../../lab5_01_piano/src/square_tone.v)
- 최상위: `piano`
- 테스트벤치: [`sim/tb.sv`](../../lab5_01_piano/sim/tb.sv) (교안 TB에 파형 덤프 두 줄만 추가)

## 설계와 예상 결과
262~523 Hz 8음을 key[7:0]으로 선택하고 CLK_HZ/(2×주파수) 클록마다 piezo를 반전한다. 무입력·여러 키는 무음.

## 시뮬레이션 결과
- 로그: [`simulation.txt`](../../evidence/01/vscode/simulation.txt) → `PASS piano: all 8 tones, silence, multiple keys, reset`
- 파형: [`wave.vcd`](../../evidence/01/vscode/wave.vcd), `wave.png`(VaporView 캡처 예정)
- 262 Hz 반주기 19클록=190 ns (215, 405, 595 ns 반전), 523 Hz는 90 ns. 4380 ns 두 키 입력 시 무음.

## 보드
핀(XDC)은 교안에 없음. 보드 시연 때 연결.

## 참고문헌
[1] Glaysia, ece2_474 STM32 실습 매뉴얼 v1.1.0, https://github.com/Glaysia/ece2_474
