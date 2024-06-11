
MSE, MAE, RMSE, MSLE, RMSLE 등의 지표는 머신러닝 모델의 성능을 평가하는 데 사용되는 다양한 손실 함수 또는 오류 지표입니다.
이 지표들은 모델이 예측한 값과 실제 값 간의 차이를 측정하여 모델의 정확성을 평가하는 데 도움을 줍니다. 각 지표는 서로 다른 방식으로 오류를 계산하며, 특정 상황에서 더 적합할 수 있습니다. 각 지표의 정의와 용도는 다음과 같습니다:

### 1. Mean Squared Error (MSE, 평균 제곱 오차)

- **정의**: MSE는 예측 값과 실제 값 간의 차이의 제곱을 평균한 것입니다. 수식으로는 다음과 같습니다:
  \[
  \text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
  \]
  여기서 \(y_i\)는 실제 값, \(\hat{y}_i\)는 예측 값입니다.
- **용도**: MSE는 큰 오류에 더 큰 패널티를 부여합니다. 따라서 큰 오류를 중점적으로 줄이고자 할 때 유용합니다.
- **특징**: 제곱된 오류 때문에 이상치(outliers)에 민감합니다.

### 2. Mean Absolute Error (MAE, 평균 절대 오차)

- **정의**: MAE는 예측 값과 실제 값 간의 절대적인 차이를 평균한 것입니다. 수식으로는 다음과 같습니다:
  \[
  \text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
  \]
- **용도**: MAE는 모든 오류에 대해 동일한 가중치를 부여하므로, 이상치에 덜 민감합니다.
- **특징**: 해석이 쉽고, 오류의 절대적인 크기를 측정하는 데 유용합니다.

### 3. Root Mean Squared Error (RMSE, 평균 제곱근 오차)

- **정의**: RMSE는 MSE의 제곱근을 취한 것입니다. 수식으로는 다음과 같습니다:
  \[
  \text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
  \]
- **용도**: MSE와 유사하지만, 단위가 실제 값과 동일하여 해석이 용이합니다.
- **특징**: MSE와 마찬가지로 큰 오류에 민감하며, 모델의 성능을 직관적으로 이해하는 데 도움을 줍니다.

### 4. Mean Squared Logarithmic Error (MSLE, 평균 제곱 로그 오차)

- **정의**: MSLE는 예측 값과 실제 값의 로그 차이의 제곱을 평균한 것입니다. 수식으로는 다음과 같습니다:
  \[
  \text{MSLE} = \frac{1}{n} \sum_{i=1}^{n} (\log(1 + y_i) - \log(1 + \hat{y}_i))^2
  \]
- **용도**: 예측 값과 실제 값의 비율을 비교하고, 큰 값보다는 작은 값의 상대적인 차이를 중요시할 때 유용합니다.
- **특징**: 오류의 상대적인 크기를 평가하는 데 유용하며, 음수 값을 다룰 수 없습니다.

### 5. Root Mean Squared Logarithmic Error (RMSLE, 평균 제곱근 로그 오차)

- **정의**: RMSLE는 MSLE의 제곱근을 취한 것입니다. 수식으로는 다음과 같습니다:
  \[
  \text{RMSLE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (\log(1 + y_i) - \log(1 + \hat{y}_i))^2}
  \]
- **용도**: MSLE와 유사하지만, 해석이 더 직관적입니다. 주로 예측 값과 실제 값의 비율 차이를 평가하는 데 사용됩니다.
- **특징**: 비율 기반의 오류 평가에 유용하며, 음수 값을 다룰 수 없습니다.

### 요약

이 지표들은 모델의 성능을 평가할 때 서로 다른 측면에서 유용합니다:

- **MSE와 RMSE**: 큰 오류에 민감하며, 연속적인 출력 값을 다루는 회귀 문제에서 자주 사용됩니다.
- **MAE**: 이상치에 덜 민감하며, 모든 오류를 동일하게 취급합니다.
- **MSLE와 RMSLE**: 상대적인 오류를 평가하며, 작은 값의 차이에 더 민감합니다. 주로 성장률이나 비율을 예측하는 데 사용됩니다.

이러한 지표들을 사용함으로써 모델의 예측 성능을 다각적으로 평가할 수 있으며, 특정 지표가 모델의 강점이나 약점을 더 잘 드러낼 수 있습니다. 따라서 각 지표의 특성과 모델의 특성을 고려하여 적절한 지표를 선택하는 것이 중요합니다.
