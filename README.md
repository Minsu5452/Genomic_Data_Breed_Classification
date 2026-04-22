# Genomic Classification | DACON 1st Place

SNP 기반 가축 품종 분류 문제를 다룬 DACON 1위 솔루션입니다. 고차원 범주형 데이터를 안정적으로 다루기 위한 인코딩, 클래스 불균형 대응, 앙상블 설계를 중심으로 정리했습니다.

## What This Repo Shows

- high-cardinality categorical feature를 다루는 feature engineering
- class imbalance 대응을 포함한 structured ML problem solving
- leaderboard용 튜닝이 아니라 최종 일반화 성능을 노린 ensemble design

## Result

- 1st / 716 teams
- AAiCON 2023 공동 저자 논문으로 확장

## My Role

- feature engineering 흐름을 설계했습니다.
- CatBoost Encoder와 oversampling 전략을 적용했습니다.
- voting ensemble로 최종 제출 구조를 만들었습니다.
- 수상 이후 코드 논문 작성에도 참여했습니다.

## Repository Layout

- `Feature/`: SNP feature engineering 실험
- `Modeling/`: feature selection, boosting, ensemble 비교
- `[Private 1위]  CatboostEncoder + OverSampling + VotingClassfier.ipynb`: 최종 제출 노트북

## Links

- [DACON competition page](https://dacon.io/competitions/official/236035/overview/description)
- [AAiCON 2023 record](https://github.com/Minsu5452/AAiCON2023)
