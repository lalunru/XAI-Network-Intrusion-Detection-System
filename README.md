# XAI-Based Network Intrusion Detection System

> 한국어 설명은 [여기](#korean)를 참고하세요.

**Development of an Explainable AI-based Network Intrusion Detection System**

Graduation thesis — Department of Computer Science, Dongguk University WISE Campus  
Advisor: Prof. Kim Jin-seok

---

## Overview

Most ML-based intrusion detection systems are black boxes —
they produce predictions without explaining *why* a connection is flagged as malicious.
This makes them difficult to trust and audit in real security environments.

This project integrates **LIME** and **SHAP** into an IDS pipeline,
making model decisions interpretable for security analysts.

- **Dataset**: UNSW-NB15
- **Models**: Decision Tree / MLP / XGBoost
- **XAI methods**: LIME (applied to MLP), SHAP (applied to XGBoost)

---

## Results

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|---|
| Decision Tree | 0.86 | 0.85 | 0.84 | 0.84 | 0.87 |
| MLP | 0.90 | 0.91 | 0.89 | 0.90 | 0.92 |
| **XGBoost** | **0.97** | **0.96** | **0.95** | **0.95** | **0.97** |

XGBoost achieved the highest performance across all metrics.
SHAP analysis revealed that features such as packet duration, service type,
and source bytes were the strongest predictors of intrusion.

---

## Repository Structure

```
├── XAI_based_Network_Intrusion_Detection_System_UNSW.ipynb
├── docs/
│   ├── report    — graduation thesis (design, implementation, results)
│   ├── poster    — research poster
│   └── presentation — slide deck
└── README.md
```

---

## Environment

- Python 3.10 (Google Colab)
- pandas, numpy, scikit-learn, xgboost, lime, shap, matplotlib, seaborn

```bash
pip install pandas numpy scikit-learn xgboost lime shap matplotlib seaborn
```

---

## How to run

1. Download the [UNSW-NB15 dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset)
2. Upload to Google Drive
3. Open and run `XAI_based_...UNSW.ipynb` in Colab

---

## Deliverables

| Type | Content |
|---|---|
| Thesis | Graduation experiment report — design, implementation, evaluation |
| Poster | Research summary poster |
| Slides | Presentation deck |
| Code | Jupyter Notebook (Colab) |

---

## License

Academic project — not licensed for commercial use.

---

<a name="korean"></a>
## 한국어 요약

머신러닝 기반 침입 탐지 모델의 블랙박스 문제를 해결하기 위해, LIME과 SHAP을 활용한 XAI 기법을 통합한 IDS 시스템 프로토타입입니다. 동국대학교 WISE캠퍼스 컴퓨터공학과 졸업 논문으로 제출했습니다.

**핵심 내용**
- Decision Tree / MLP / XGBoost 세 모델 비교 (XGBoost F1 0.95로 최고 성능)
- LIME: MLP 개별 예측 설명 — 특정 연결이 왜 침입으로 분류됐는지 시각화
- SHAP: XGBoost 전역 특성 중요도 분석 — 패킷 지속 시간, 서비스 유형, 소스 바이트가 핵심 예측 변수로 확인
- 데이터셋: UNSW-NB15
