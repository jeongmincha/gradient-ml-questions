# 10. 다음 상황들에서 발생할 수 있는 문제들에 대해 생각해보아라.

- Model Selection 과정을 마친 후, 선택된 모형을 Test Set을 이용해 평가했더니 만족할만한 수치가 나오지 않았다. 그래서 더 많은 모형을 Training 시킨 후 Model Selection 과정을 반복해 선택된 모형을 평가했더니 만족할만한 수치가 나왔다.  이렇게 Assessment 과정까지 마친 후, 선택된 Model의 Generalization Error는 두 번째 Test Error와 비슷할 것이라는 결론을 내렸다.

- 2011-2018년의 주가 데이터를 이용해 예측 모델링을 하기 위해, Train / Validation / Test를 랜덤하게 8:1:1로 나누어 모형을 만들었다. 그랬더니 Test Set에 대해 높은 예측 성능을 보인다. (읽을거리 : [Backtesting](https://en.wikipedia.org/wiki/Backtesting))

- 웹에서 고해상도 이미지를 크롤링해 이미지 분류 모형을 만들었다. 이 모형을 모바일 기기에 탑재하여 상대적으로 해상도가 낮은 이미지를 분류할 때 사용할 것이다.

- 서울시 전체의 데이터를 이용해 교통량을 예측하는 모형을 만들었다. 이 모형을 강남역 부근의 교통량을 예측하는데 사용할 것이다.