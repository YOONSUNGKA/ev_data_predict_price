이 Jupyter Notebook은 전기차 가격 예측을 위한 머신러닝 모델 개발 및 평가를 다룹니다. 다음과 같은 주요 단계를 포함합니다:

1. **라이브러리 임포트**  
   머신러닝과 딥러닝을 위한 주요 라이브러리(SciKit-Learn, XGBoost, LightGBM, CatBoost 등)와 데이터 처리 라이브러리(Pandas, NumPy 등)를 사용합니다.

2. **데이터 로드**  
   - `train.csv`: 학습 데이터셋
   - `test.csv`: 테스트 데이터셋
   - `sample_submission.csv`: 제출 형식 데이터셋

3. **데이터 전처리**  
   - 결측치 처리: 배터리 용량의 결측치를 중앙값으로 대체.
   - 파생 변수 생성: 에너지 효율(배터리 용량 대비 주행거리)과 차량 나이(현재 연도에서 차량 연식 차감)를 계산.
   - 원-핫 인코딩: 범주형 변수(제조사, 모델 등)를 원-핫 인코딩으로 변환.
   - 데이터 분할: 학습 데이터와 검증 데이터를 80:20으로 분할.
   - 데이터 스케일링: `StandardScaler`를 사용해 데이터 정규화.

4. **머신러닝 모델 정의**  
   다음과 같은 다양한 회귀 모델을 정의합니다:
   - XGBoost
   - CatBoost
   - LightGBM
   - Random Forest
   - Extra Trees
   - Gradient Boosting

5. **모델 학습 및 평가**  
   - 각 모델을 학습하고 검증 데이터에 대해 예측 수행.
   - RMSE(Root Mean Squared Error)를 사용해 모델 성능 평가.

---

### README.md 초안

```markdown
# EV Price Prediction

이 프로젝트는 전기차(EV) 가격 예측을 위해 다양한 머신러닝 알고리즘을 활용하는 과정을 포함합니다. 주요 내용은 다음과 같습니다.

## 1. 프로젝트 개요
전기차의 가격을 예측하여 중고차 시장에서의 가격 형성 요인을 분석하고, 예측 정확도를 개선하는 것이 목표입니다.

## 2. 데이터
- **학습 데이터(train.csv)**: EV의 가격과 관련된 다양한 특성이 포함된 데이터셋.
- **테스트 데이터(test.csv)**: 예측을 위한 데이터셋.
- **제출 샘플(sample_submission.csv)**: 제출 형식의 예제 파일.

## 3. 주요 단계
1. **데이터 전처리**:
   - 결측치 처리
   - 파생 변수 생성 (에너지 효율, 차량 나이 등)
   - 범주형 변수 인코딩
   - 데이터 정규화 및 분할

2. **모델 정의**:
   - XGBoost, CatBoost, LightGBM 등 다양한 머신러닝 알고리즘 사용.

3. **모델 학습 및 평가**:
   - 검증 데이터에 대해 RMSE 기반 성능 평가.

## 4. 주요 결과
- 각 모델의 RMSE:
  - XGBoost: 1.6297
  - CatBoost: 1.6484
  - LightGBM: 1.3639
  - Random Forest: 1.5423
  - Extra Trees: 1.6601
  - Gradient Boosting: 1.6498

## 5. 사용법
### 의존성 설치
```bash
pip install -r requirements.txt
```

### 코드 실행
```bash
jupyter notebook ev_price_predict_10.ipynb
```

### 데이터 파일
- `train.csv`, `test.csv`, `sample_submission.csv`를 프로젝트 루트 디렉토리에 저장 후 실행하세요.

## 6. 라이센스
본 프로젝트는 [MIT 라이센스](LICENSE)를 따릅니다.
```

위 README는 추가적인 설명이나 데이터 소스 링크를 포함하도록 확장 가능합니다. 더 필요한 내용이 있다면 알려주세요!
