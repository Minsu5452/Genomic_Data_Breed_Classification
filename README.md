# 유전체 정보 품종 분류

SNP 유전체 정보를 활용해 품종을 분류한 DACON 경진대회 1위 솔루션입니다. 제한된 표본 수와 클래스 불균형이 있는 조건에서 피처 엔지니어링, 불균형 보정, 모델 비교, 앙상블을 단계적으로 실험했습니다.

## 개요

| 항목 | 내용 |
| --- | --- |
| 대회 | 유전체 정보 품종 분류 AI 경진대회 |
| 기간 | 2022.12.12 - 2023.01.16 |
| 주최 / 주관 | 충남대학교 바이오AI융합연구센터 / DACON |
| 결과 | 1st |
| 과제 | SNP 기반 multi-class 품종 분류 |
| 평가지표 | Macro F1 |

## 접근

- SNP 이름, 염색체, 위치, 유전 거리, 염기 조합에서 파생 변수를 만들었습니다.
- 고차원 범주형 SNP 정보를 CatBoost Encoder 등으로 변환해 모델 입력으로 사용했습니다.
- SMOTE, BorderlineSMOTE 등 불균형 보정 방법을 비교했습니다.
- CatBoost, LightGBM, XGBoost, Random Forest, Extra Trees, SVC, MLP를 넓게 실험했습니다.
- 최종 제출에는 강한 모델들의 weighted hard-voting ensemble을 사용했습니다.

## 저장소 구성

```text
.
├── assets/
│   └── award_photo.jpeg
├── notebooks/
│   ├── 01_feature_engineering_baseline.ipynb
│   ├── ...
│   └── 13_final_competition_solution.ipynb
├── reports/
│   ├── award_certificate.pdf
│   └── final_competition_solution.pdf
└── requirements.txt
```

## 수상 자료

![수상 사진](assets/award_photo.jpeg)

- 수상 확인서: [`reports/award_certificate.pdf`](reports/award_certificate.pdf)
- 최종 솔루션: [`reports/final_competition_solution.pdf`](reports/final_competition_solution.pdf)

## 공개 범위

대회 원본 데이터, 생성된 피처 테이블, 학습된 모델, 제출 파일은 포함하지 않았습니다. 공개 포트폴리오용으로 노트북 출력과 로컬 실행 메타데이터를 정리했습니다.

## 링크

- [DACON 대회 페이지](https://dacon.io/competitions/official/236035/overview/description)
- [DACON 코드 공유](https://dacon.io/competitions/official/236035/codeshare/7430)
- [연계 학술대회 기록](https://github.com/Minsu5452/AI_Frenz_2023_Publication)
