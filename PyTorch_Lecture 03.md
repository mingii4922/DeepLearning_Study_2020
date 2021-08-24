# 03. Gradient Descent

------------------
### 대표적인 loss 그래프
![](https://images.velog.io/images/mingii4922/post/a509e64d-137a-4317-a59e-708d978b018f/image.png)

이 Loss라는 함수를 사용해서 어떤 Weight(w)와 bias(b)가 잘 학습된 모델인지를 확인할 수 있다.

_**gradient descent(경사 하강법) : 랜덤의 위치에서 시작해서 기울기를 계산하며 경사의 절댓값이 낮은 쪽으로 계속 이동시켜서 극값에 이를때까지 반복하는 체계적인 방법이다.**_

여기서 w의 값을 찾는 과정은 weight에서 learning rate(lr)과 gradient(미분 값==기울기)을 곱해준 결과를 빼준다.

![](https://images.velog.io/images/mingii4922/post/5f6fd42b-ef40-46f1-b258-faa1ec74ef48/image.png)

$ w = w - lr*gradient $
-----------------
---------------
## Gradient Descent 종류

|경사하강법 종류| 특징 |
|---|---|
|batch Gradient Descent|오래 걸리고 메모리가 크게 요구하나, 전역 최소값을 찾을 수 있다.|
|Stochastic Gradient Descent|랜덤으로 선택한 하나의 데이터에 대해서만 계산하는 방법 -> 빠르지만 배치보다 정확도가 낮을 수 있다.|
|mini-batch Gradient Descent|정해준 데이터 양에 대해서만 계산하여 매개변수 값을 조정 -> 계산이 빠르고 SGD보다 안정적, **가장 많이 사용되는 경사 하강법**|

#### Momentum : 관성이라는 물리학 법칙을 응용한 방법
-> 전 step의 접선의 기울기 값을 일정한 비율만큼 반영 
-> 지역최소값에서 관성의 힘으로 빠져나올 수 있다.

#### Adam : RMSprop와 모멘텀을 합친 방법
-> 방향+학습률을 모두 잡기위한 방법
-> **가장 많이 사용되는 경사 하강법**
