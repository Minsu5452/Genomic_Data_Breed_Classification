# 유전체 품종 분류 | DACON 1위

> SNP 기반 가축 품종 분류 문제에서 feature engineering, 불균형 대응, ensemble 설계로 1위를 기록한 솔루션입니다.

## 한눈에 보기

| 항목 | 내용 |
| --- | --- |
| 유형 | Competition solution |
| 결과 | 1위 / 716팀 |
| 문제 | SNP 기반 가축 품종 다중 분류 |
| 핵심 접근 | CatBoost Encoder, oversampling, voting ensemble |
| 이 저장소가 증명하는 것 | structured ML 문제 해결력과 일반화 중심 실험 설계 역량 |

## 제가 맡은 일

- feature engineering 흐름을 설계했습니다.
- CatBoost Encoder와 oversampling 전략을 적용했습니다.
- voting ensemble로 최종 제출 구조를 만들었습니다.
- 수상 이후 코드 논문 작성에도 참여했습니다.

## 이 저장소에서 읽히는 강점

- high-cardinality categorical feature를 다루는 feature engineering 역량이 보입니다.
- class imbalance 대응을 포함한 structured ML problem solving 경험이 정리되어 있습니다.
- leaderboard용 과적합보다 최종 일반화 성능을 노린 ensemble design을 확인할 수 있습니다.

## 저장소 구성

- `Feature/`: SNP feature engineering 실험
- `Modeling/`: feature selection, boosting, ensemble 비교
- `[Private 1위]  CatboostEncoder + OverSampling + VotingClassfier.ipynb`: 최종 제출 노트북

## 링크

- [DACON competition page](https://dacon.io/competitions/official/236035/overview/description)
- [AAiCON 2023 record](https://github.com/Minsu5452/AAiCON2023)
