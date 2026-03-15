# 설명 가능한 인공지능(XAI)을 활용한 네트워크 침입 탐지 시스템

**Development of an Explainable AI-based Network Intrusion Detection System**

> 동국대학교 WISE캠퍼스 컴퓨터공학과 졸업 논문
> 지도교수: 김진석 교수님

---

## 프로젝트 개요

머신러닝 기반 침입 탐지 모델의 **블랙박스 문제**를 해결하기 위해,  
LIME과 SHAP을 활용한 XAI 기법을 통합한 IDS 시스템 프로토타입입니다.

- **데이터셋**: UNSW-NB15
- **모델**: Decision Tree / MLP / XGBoost
- **XAI 기법**: LIME (MLP), SHAP (XGBoost)

---

## 모델 성능 요약

| 모델 | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|------|----------|-----------|--------|----------|---------|
| Decision Tree | 0.86 | 0.85 | 0.84 | 0.84 | 0.87 |
| MLP | 0.90 | 0.91 | 0.89 | 0.90 | 0.92 |
| XGBoost | 0.97 | 0.96 | 0.95 | 0.95 | 0.97 |

---

## 파일 구조
```
├── XAI_based_Network_Intrusion_Detection_System_UNSW.ipynb
├── docs/
│   ├── report_설명 가능한 인공지능(XAI)을 활용한 네트워크 침입 탐지 시스템의 개발_김성연 # 졸업자격실험보고서 (졸업논문)
│   ├── poster_설명-가능한-인공지능_XAI_을-활용한-네트워크-침입-탐지-시스템의-개발 #논문 포스터
│   └── presentation_설명-가능한-인공지능_XAI_을-활용한-네트워크-침입-탐지-시스템의-개발 #발표 슬라이드
└── README.md
```

---

## 실행 환경

- Python 3.10 (Google Colab)
- pandas, numpy, scikit-learn, xgboost, lime, shap, matplotlib, seaborn
```bash
pip install pandas numpy scikit-learn xgboost lime shap matplotlib seaborn
```

---

## 실행 방법

1. [UNSW-NB15 데이터셋](https://research.unsw.edu.au/projects/unsw-nb15-dataset) 다운로드
2. Google Drive에 데이터 업로드
3. `XAI_based_...UNSW.ipynb` 노트북 실행

---

## 산출물

| 구분 | 내용 |
|------|------|
| 보고서 | 졸업자격실험보고서 (설계, 구현, 실험 결과) |
| 발표자료 | 연구 포스터 및 PPT |
| 코드 | Jupyter Notebook (Colab 환경) |
