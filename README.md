# 26-Fall-Adap

적응신호처리 수업 과제 정리 저장소

수업 과제로 수행한 개념 정리/실험 코드/리포트를 정리한다.

## 과제 목록

| 과제 | 주제 | 상태 |
| --- | --- | --- |
| [HW01](./HW01/) | 3-tap FIR 필터를 이용한 음성 신호 필터링 | 완료 |
| [HW02](./HW02/) | 128-tap NLMS 필터를 이용한 음향 에코 제거 | 완료 |
| [HW03](./HW03/) | lattice filter를 이용한 음성 예측 모델링 | 완료 |

### HW01. 3-tap FIR 필터를 이용한 음성 신호 필터링

입력 음성 `a.wav`에 계수가 모두 $1/3$인 3-tap FIR 필터를 적용하고, 필터링 결과를 `a_out.wav`로 저장 후 청취 결과를 분석하여 다음 결과물을 얻었다.

- [실험 코드 및 실행 결과](./HW01/hw01.ipynb)
- [HW01 리포트](./HW01/Adap_HW01_20261099.pdf)
- [입력 음성](./HW01/a.wav)
- [출력 음성](./HW01/a_out.wav)

### HW02. 128-tap NLMS 필터를 이용한 음향 에코 제거

`ref.wav`를 기준 입력으로 사용해 `pri.wav`와 `pri2.wav`의 에코를 각각 추정·제거했다. 여러 하이퍼파라미터 조합의 결과를 비교하고, `pri2.wav`의 double-talk 구간에서 에코 제거와 여성 화자 음성 보존을 함께 고려해 최종 파라미터를 선택했다.

- [실험 코드 및 실행 결과](./HW02/hw02.ipynb)
- [HW02 리포트](./HW02/Adap_HW02_20261099.pdf)
- 입력 음성: [ref.wav](./HW02/ref.wav), [pri.wav](./HW02/pri.wav), [pri2.wav](./HW02/pri2.wav)
- 출력 음성: [err.wav](./HW02/err.wav), [err2.wav](./HW02/err2.wav)

### HW03. Lattice filter를 이용한 음성 예측 모델링

`a.wav` 전체에서 구한 10차 모델의 합성 결과와 한계를 분석한 뒤, 20 ms 청크별 모델링을 추가했다. 두 방식 모두 prediction error와 white noise를 all-pole lattice filter에 입력하고, 복원 결과와 시간에 따른 주파수·에너지 변화를 비교했다.

- [실험 코드 및 실행 결과](./HW03/hw03.ipynb)
- [비교 보고서](./HW03/Adap_HW03_20261099.pdf)
- 입력 음성: [a.wav](./HW03/a.wav)
- 전체 모델 출력: [syn_f10.wav](./HW03/syn_f10.wav), [syn_noise.wav](./HW03/syn_noise.wav)
- 청크별 모델 출력: [syn_f10_chunk.wav](./HW03/syn_f10_chunk.wav), [syn_noise_chunk.wav](./HW03/syn_noise_chunk.wav)
