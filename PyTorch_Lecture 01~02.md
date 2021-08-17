![](https://images.velog.io/images/mingii4922/post/89345dfe-7bf9-4b8b-bbcc-f0951168a08b/image.png)
----
----

> ## Machine Learning
Human intelligence : 사람은 어떠한 결정을 할 때 많은 지식 또는 정보를 토대로 추론과 예측을 한다.
머신러닝이란? Human intelligence와 동일하지만 기계학습(train)을 거쳐야 제대로 예측할 수 있다.
머신러닝은 어떤 데이터를 분류하거나 값을 예측하는 것 ( 확률과 통계)

_**목표 : 어떠한 정보(input)를 가지고 컴퓨터를 학습시켜 
예측한 값이 실제output과 같도록 하는것**_

![](https://images.velog.io/images/mingii4922/post/eeb2009f-835f-4b63-9e17-5e220bb0e041/image.png)
--
이미지에 대해서 해당 픽셀의 너비와 해당하는 이미지의 라벨을 통해 학습시킨다.

머신러닝 학습 방법 : 지도학습(supervised), 비지도학습(unsupervised), 강화학습(Reinforcement)

|학습 종류|정의|기법|
|---|---|---|
|지도 학습|정답을 알려주며 학습(분류/회귀)|k-최근접이웃 / 선형회귀 / 로지스틱회귀(분류)|
|비지도 학습|비슷한 데이터들을 군집화|K-means / PCA  |
|강화학습|상과 벌(보상)을 주며 학습 ex) 알파고|온라인(미니배치-추가학습) / 배치(오프라인 학습)/ 사례기반 / 모델기반|
 
---------------
> representation learning(표현학습) : 최적의 특징을 자동으로 알아내는 접근방식
Logistic Regression(논리회귀) : 어떤 범주에 속할 확률을 0에서 1사이의 값으로 예측(2진분류)
MLP(Multilayer Perceptron)(다층 퍼셉트론) : 일부 입력값 집합을 출력값에 매핑하는 수학함수
MLR(Multiple Linear Regression)(다중 선형회귀) : x와 y관계를 선형이라 가정하고 오차가 가장 작은 직선을 찾는 것

--------
AI : 사고나 학습 등 인간이 가진 지적 능력을 컴퓨터를 통해 구현하는 기술
딥러닝 : 신경망을 사용하는 알고리즘의 그룹으로 여러 비선형 변환기법의 조합으로 높은 수준의 기계학습 알고리즘
보통 신경망은 정말로 많은 층을 가지고 있다.
머신러닝 vs 딥러닝 : 데이터 의존도, 하드웨어 의존도, feature engineering, 문제 해결 접근법
인공신경망(Artificial Neural Network) : 뉴런이 서로 연결된 네트워크

----------
 
![](https://images.velog.io/images/mingii4922/post/c4d4907f-295d-48ed-a9fc-cbbc8a554f73/image.png)
--
------
> ## **Pytorch**
심층 신경망에서 사용되는 framework, 간결하고 구현이 빠르다.
**define-by-run** : 코드를 직접 돌리는 환경인 세션을 만들고, 계산 그래프를 만든 후(define), 코드를 실행하는 시점에 데이터를 넣어 실행(run)하는 방식
깔끔하고 직관적이고 빠름
파이썬 라이브러리와 높은 호환성을 가진다.

---------

> ## pytorch VS tensorflow
손실함수 : 실제값과 예측값의 차이(loss, cost)를 수치화해주는 함수
--> 학습은 실제로 이러한 경우의 손실을 최소화하는 weight값을 식별하기 위한 것입니다.
회귀 : 평균제곱오차(MSE) / 분류 : 크로스 엔트로피(Cross-Entropy)
--> y(head) : x를 input받아 y를 예측한 값 => x*w+b
MSE(Mean Square Error) : 평균 제곱 오차
--> 제곱을 하는 이유 : 오차가 양수와 음수로 섞여있어서 부호를 없애 제대로 된 전체 오차의 크기를 알 수 있다.
RMSE(root) : 오차의 값이 너무 커서 계산 속도가 느려지는 것을 방지하여 제곱근을 씌운 것

|Network|Definition|Characteristics|
|---|---|---|
|(ANN) Artificial Neural Network|사람의 신경망 원리와 구조를 모방하여 만든 기계학습 알고리즘|overfitting에 따른 문제  /  학습 시간이 느림|
|(DNN) Deep Neural Network|input layer과 output layer 사이에 여러개의 hidden layer들로 이루어진 ANN|
|(RNN) Recurrent Neural Network|입력과 출력을 Sequence단위로 처리|지속적 / 반복적 / 순차적|
|(CNN) Convolutional Neural Network|(raw input)이미지를 그대로 받음으로써 공간적/지역적 정보를 유지한 채 특성(feature)들의 계층을 빌드업|주변 픽셀과의 연관성을 찾아냄|
