# 06. 아래 그래프를 보고 물음에 답하여라. (출처 : [Deep Learning Book](https://www.deeplearningbook.org/))

![](../images/ml-questions-01-06.png)

- 어느 지점 이후에서 Overfitting이 발생했다고 이야기 할 수 있는가?
  - Generalization error의 기울기가 음에서 양으로 변하는 시점부터 Overfitting이 발생했다고 볼 수 있다. 이 경우 모델의 Capacity가 늘어나도 Generalization error는 계속해서 증가하게 될 것이다. 최소의 Generalization error를 갖는 모델을 찾는 것이 머신러닝의 궁극적인 목표이므로 이 시점 이후의 모델을 학습하는 것은 무의미하다.
- Generalization Gap이란 무엇인가?
  - Generalization error - Training error
- Early Stopping이란 무엇인가? Early Stopping의 맥락에서 x축에 들어가야 할 변수는 무엇이겠는가?
  - Early Stopping이란 Gradient descent와 같이 되풀이하는 (iterative) 방법의 알고리즘에서 더 이상의 반복이 오버핏을 야기할 뿐이라고 판단되었을 때 학습을 중단시키는 것을 말한다. Early Stopping 의 맥락에서 x축에는 Iteration Count와 같이 학습이 반복될 때마다 그 수가 증가하는 변수가 들어가야 한다.
- 위 그래프에서 Capacity 대신 x축에 들어갈 수 있는 변수들을 최대한 많이 적어라.
  - Learning Time, Iteration Count
- Generalization Error를 직접 측정할 수 있는가? 만약 아니라면 어떻게 추정할 수 있는가?
  - Generalization Error를 직접 측정할 수는 없다. 한 번도 보지 못한 데이터를 처리한다는 것 자체가 불가능하기 때문이다. 그 대신 훈련과 모델 선택 과정에서 한 번도 사용되지 않은 데이터인 Test Set을 따로 두어 학습된 모델이 테스트 데이터를 처리하는 것으로 Test Error를 측정할 수 있고, 이 값을 Generalization Error로 추정할 수 있다.