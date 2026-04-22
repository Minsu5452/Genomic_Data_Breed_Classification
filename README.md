# 🧬 Genomic Breed Classification — 유전체 정보 기반 품종 분류 AI

![Rank](https://img.shields.io/badge/🥇%201st-716%20teams-gold)
![Competition](https://img.shields.io/badge/DACON-Official%20Competition-blue)
![Host](https://img.shields.io/badge/Host-충남대%20바이오AI융합연구센터%20%7C%20티엔티리써치%20%7C%20AI%20Frenz-green)
![Domain](https://img.shields.io/badge/Domain-Bioinformatics%20%7C%20SNP-purple)
![Publication](https://img.shields.io/badge/📄%20Published-AAiCON2023-red)

> **1st / 716팀 (상위 0.14%)** — SNP(단일염기다형성) 유전체 데이터를 활용한 가축 품종 다중 분류. **CatBoost Encoder + Over-sampling + Voting Classifier** 앙상블로 최종 우승. 수상 후 **에이아이프렌즈학회(AI Frenz) 2023년 제2차 실용 인공지능 학술대회에 코드 논문 공동 저자**로 등재.

---

## 🏆 Awards & Publication

- 🥇 **1st Place** · DACON · 716팀 · 2022.12.12 ~ 2023.01.16
- 📄 **공식 학술대회 논문 기재** (공동 저자 / 코드 논문 작성 기여) — [AAiCON2023](https://github.com/Minsu5452/AAiCON2023)
- 주최: 충남대학교 바이오AI융합연구센터 · 티엔티리써치 · AI Frenz · 주관: DACON

## 🔍 Overview

- **배경**: 축산 분야에서 SNP(Single Nucleotide Polymorphism) 유전체 마커 기반 품종 식별은 사육·검역·연구 전반에 핵심. 수작업 유전학 분석을 ML로 대체할 때의 정확도·일반화 확보가 과제.
- **문제 정의**: 고차원 SNP 특성으로부터 **가축 품종 다중 분류** (multi-class classification).
- **난점**:
  1. **클래스 불균형** — 일부 품종 샘플 희소
  2. **고차원 범주형** — SNP 각 위치가 범주형 변수, 원-핫 폭발 위험
  3. **모델 일반화** — 오버피팅 쉽게 일어남

## 🧠 Approach

### 핵심 아이디어 3가지
1. **CatBoost Encoder**: 고차원 범주형 SNP를 target-mean 기반으로 인코딩 (원-핫보다 차원 효율 + 정보 보존)
2. **Over-sampling**: 소수 품종 클래스 업샘플링으로 편향 완화
3. **Voting Classifier**: 이질적 모델 조합으로 일반화 성능 확보

### 파이프라인
```
SNP raw data
    │
    ▼  Feature Engineering (CatBoost Encoder)
범주형 SNP → 연속형 표현
    │
    ▼  Over-sampling (소수 클래스 보강)
균형 잡힌 학습셋
    │
    ▼  Voting Classifier (ensemble)
최종 품종 예측
```

### 모델 상세
- **Encoder**: CatBoost Encoder (target-statistic 기반)
- **Sampler**: OverSampling 기법 (SMOTE 계열)
- **Ensemble**: Voting Classifier — 이질 모델 혼합 (개별 base learner → soft voting)

## 📈 Results

| 리더보드 | 순위 | 비고 |
|---------|------|------|
| **Private** | **🥇 1위** | 716팀 중 1위 (상위 0.14%) |

## 🛠 Tech Stack

- **Language**: Python 3.8+
- **ML**: scikit-learn · CatBoost · imbalanced-learn (SMOTE 계열)
- **Data**: Pandas · NumPy
- **Env**: Jupyter Notebook

## 📁 Structure

```
Genomic_Data_Breed_Classification/
├── Feature/                                  # 피처 엔지니어링 노트북
├── Modeling/                                 # 모델링 노트북 (tune·ensemble 실험)
├── [Private 1위] CatboostEncoder + OverSampling + VotingClassifier.ipynb
├── [Private 1위] ...pdf                       # 최종 솔루션 리포트
└── README.md
```

## 👤 Role / Team

- **역할**: 팀장 (3인 팀)
- **기여**: 피처 엔지니어링 설계 · CatBoost Encoder 적용 · 앙상블 전략 / 수상 후 **학술대회 코드 논문 작성**

## 🔗 Links

- [DACON 대회 페이지](https://dacon.io/competitions/official/236035/overview/description)
- [AAiCON2023 논문 기재 레포](https://github.com/Minsu5452/AAiCON2023)

---

> 🔗 Portfolio: [Minsu5452](https://github.com/Minsu5452)
