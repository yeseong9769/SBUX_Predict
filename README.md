# SBUX Stock Price Prediction using LSTM
이 프로젝트는 LSTM(Long Short-Term Memory) 신경망을 사용하여 스타벅스(SBUX) 주가를 예측하는 딥러닝 모델을 구현합니다.

## 주요 구성
### 1. 데이터 전처리
- pandas를 사용한 주가 데이터 로드 및 정제
- MinMaxScaler를 통한 데이터 정규화
- Sliding Window 기법을 활용한 시계열 데이터 생성
- 학습/테스트 데이터 분리
   
### 2. LSTM 모델 아키텍처
- 주요 하이퍼파라미터:
  - Input size: 3 (Open, High, Low)
  - Hidden size: 32
  - Number of layers: 2
  - Output size: 1 (Close price prediction)
  - Sequence length: 7
- PyTorch 프레임워크 기반 구현

### 3. 모델 학습
- 손실 함수: MSE(Mean Squared Error)
- 최적화 알고리즘: Adam optimizer
- 학습률(Learning rate): 0.01
- 에포크(Epochs): 1000

### 4. 성능 평가
- RMSE(Root Mean Square Error)를 통한 예측 정확도 평가
- 실제 주가와 예측 주가의 시각화 비교

## 실행 방법
1. 필요한 라이브러리 설치
```bash
pip install numpy pandas matplotlib torch scikit-learn
```

2. 주피터 노트북 실행
```bash
jupyter notebook SBUX_Prediction.ipynb
```

## 향후 개선 방향
1. 추가적인 특성(거래량, 기술적 지표 등) 활용
2. 하이퍼파라미터 최적화
3. 다양한 시계열 모델과의 성능 비교
4. 더 긴 예측 기간에 대한 모델 확장