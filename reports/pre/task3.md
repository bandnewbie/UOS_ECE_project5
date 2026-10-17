# STM32_1_과제3 · ISR 기반 LED 간격 변경 · 실험 전 레포트

**작성자:** 박건우 (2025440050) · G조  
**저장소:** https://github.com/bandnewbie/UOS_ECE_project5 · 태그 `lab5-pre` · 커밋 `(push 후 기입)`

## 소스
[`task3_ece2_474_routine.c`](../../stm32_1_tasks/task3_ece2_474_routine.c) → `stm32_lab/Core/Src/ece2_474_routine.c`에 붙여넣기

## 설계와 예상 결과
버튼 ISR에서 간격 1→2→4→8→1초, TIM6 ISR(100 ms)에서 횟수를 세어 PA5 반전. init에서 TIM6 시작.

## 사전 확인
arm-none-eabi-gcc로 `cmake --preset Debug && cmake --build build/Debug` 경고 없이 링크 완료.

## 보드
`evidence/task3/board/`에 시연 자료 추가 예정.

## 참고문헌
[1] Glaysia, ece2_474 STM32 실습 매뉴얼 v1.1.0, https://github.com/Glaysia/ece2_474
