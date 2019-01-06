# 07. 아래 그림들은 10개 데이터에 대해 M차 다항함수를 학습시킨 결과이다. 그림 1은 학습된 함수들의 개형을, 그림 2는 Training / Test error를, 그림 3은 학습된 Parameter들의 값을 표로 나타낸 것이다. 이를 보고 다음 물음들에 답하여라. (출처 : Pattern Recognition and Machine Learning)

![](../images/ml-questions-01-07.png)

- 그림 1에서 가장 적절한 M의 값을 찾고 그 이유를 설명하라.
  - M=3이다. 
  - M=0 과 M=1인 경우는 트레이닝 데이터에 대해서 오차가 큰 함수를 찾게 되었으므로 variance가 큰, unerfit이 된 모형을 학습하게 되었다.
  - M=9인 경우 트레이닝 데이터를 오차없이 완벽하게 계산해내는 variance가 거의 없는 함수를 찾게 되었다. 그러나 이 함수는 bias가 매우 강하므로 실제 일반화된 데이터에 대해서는 좋은 결과를 보이지 못한다. 즉, variance는 낮으나 bias는 매우 높은 함수 (overfit) 를 찾게 되었다.
- 그림 3을 보고, L1 / L2 Regularization의 적용이 필요해 보이는 상황과 그 이유에 대해 설명하라.
  - L1 Regularization 이 필요한 경우는 M=9 이다. 계수의 절댓값의 합이 M=9 일 때부터 크게 증가하기 때문이다. 이 경우 Regularized Cost Function 의 값이 매우 크게 증가하게 됨으로써 M=9 이상으로 훈련된 모델을 선택하지 않게 될 것이다.
  - L2 Regularization 이 필요한 경우는 M=6, M=9 이다. 계수의 제곱의 합이 M=6 일 때부터 크게 증가하기 때문이다. 이 경우 Regularized Cost Function 의 값이 매우 크게 증가하게 됨으로써 M=6 이상으로 훈련된 모델을 선택하지 않게 될 것이다.
- 그림 2에서 Test Error가 가장 낮은 모형을 선택해도 되는가?
  - Test Error가 가장 낮더라도 그 모형이 Training Error가 큰 경우에는 선택하지 않아야 한다. 왜냐하면 기대 일반화 오류 (Expected Generalization Error)  는 편향 (Bias) 과 분산 (Variance) 의 합이기 때문이다. Test Error가 낮다는 것은 편향이 낮다는 것을 의미하지만, Training Error가 크다면 분산이 높다는 것을 의미하기 때문에, 편향이 낮더라도 분산이 높다면 기대 일반화 오류 값은 증가하게 될 것이다.
  - [그림 2]에서는 M=7이 가장 적합한 모형으로 보인다. 왜냐하면 M=3부터 M=7까지는 Test Error가 거의 차이가 없지만, M=3부터 M=7까지 미세하게 Training Error가 감소하고 있어서 Test Error와 Training Error의 합이 가장 낮은 것은 M=7의 모형으로 보이기 때문이다.
- Hyperparameter란 무엇인가? 위 그림들에서 Hyperparameter와 Parameter는 어떤 것들인지 찾아라.
  - Hyperparamter는 모형 학습을 통해서 최적화해야 하는 변수가 아닌, 기존 지식을 통해 직접 설정하거나 외부 모형을 통해서 자동으로 설정이 되는 변수를 의미한다.
  - 위 그림에서 Hyperparamter는 M이고, Parameter는 w(0) * ~ w(m) * 이다.
  - M은 모형을 학습하면서 변하는 함수가 아니라 모형을 학습하기 전 직접 설정한 변수이다. 반면 Parameter인 w(i) * 는 학습을 진행하면서 그 값이 변화된다. 