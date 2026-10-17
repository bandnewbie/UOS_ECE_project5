# STM32_1_과제4 · 버튼으로 PWM 비율 변경 · 실험 전 레포트

**작성자:** 박건우 (2025440050) · G조  
**저장소:** https://github.com/bandnewbie/UOS_ECE_project5 · 태그 `lab5-pre` · 커밋 `(push 후 기입)`

## 소스
[`task4_ece2_474_routine.c`](../../stm32_1_tasks/task4_ece2_474_routine.c) → `stm32_lab/Core/Src/ece2_474_routine.c`에 붙여넣기

## 설계와 예상 결과
버튼 ISR에서 PB4 PWM 비교값 250→500→750→250 (25→50→75→25%). init에서 PWM 시작, TIM6는 주석.

## 사전 확인
arm-none-eabi-gcc로 `cmake --preset Debug && cmake --build build/Debug` 경고 없이 링크 완료.

## 보드
`evidence/task4/board/`에 시연 자료 추가 예정.

## 참고문헌
[1] Glaysia, ece2_474 STM32 실습 매뉴얼 v1.1.0, https://github.com/Glaysia/ece2_474
