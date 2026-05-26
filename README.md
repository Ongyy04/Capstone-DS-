# Financial Fraud Detection System (FDS)

금융 거래 데이터 기반 이상거래 탐지 프로젝트입니다.

## Project Goal
실제 금융 거래 데이터를 기반으로 정상 거래와 사기 거래를 분류하는 이상거래 탐지 모델을 구축합니다.
- Data Leakage 제거
- 시계열 무결성 검증
- 행동 기반 Feature Engineering
- Hybrid Ensemble Architecture
를 중심으로 실제 운영 가능한 구조를 설계하고자 했습니다. 


## Main Tasks
- Data Preprocessing
- Feature Engineering
- XGBoost / LightGBM 기반 지도학습
- Threshold Tuning
- SHAP 기반 해석
- Autoencoder 기반 이상탐지
- Stacking Ensemble
- PRC-AUC 기반 성능 평가


## Key Issues
### 1. Data Leakage
초기 모델에서 Risk_Score 및 일부 집계 변수에 대한 과도한 의존이 발견되었습니다.

Leakage 의심 변수를 제거하자 성능이 급감하였으며,
이를 통해 기존 모델이 실제 패턴이 아닌 정답지를 학습했음을 확인했습니다.

### 2. Time-series Integrity
Failed_Transaction_Count_7d 등 집계 변수에 대해
미래 정보가 포함되지 않도록 시계열 무결성을 검증하였습니다.

## Models
- XGBoost
- LightGBM
- RandomForest
- Autoencoder
- Stacking Ensemble
## Evaluation Metrics
- PRC-AUC
- Recall
- Precision
- F1-score
- ROC-AUC

## Team
- 오은서
- 강지원
- 최소현
