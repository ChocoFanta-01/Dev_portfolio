
Fashion-MNIST CNN Classification

PyTorch 기반 CNN 모델로 의류 이미지(10 class)를 분류하는 프로젝트입니다.
총 94.96% 정확도를 달성했으며, 데이터 전처리, CNN 구조 설계, 학습 및 평가 전 과정 모두 직접 수행하였습니다.

1. 프로젝트 개요

Fashion-MNIST 데이터셋을 활용하여

CNN 기반 이미지 분류 모델 설계

90% 이상의 정확도 달성

PyTorch 기반 학습/평가 파이프라인 구축
을 목표로 수행한 프로젝트입니다.

최종적으로 94.96%의 테스트 정확도를 기록했습니다.

2. 사용 기술

Language: Python

Framework: PyTorch

Dataset: Fashion-MNIST

Training Environment: Google Colab

Techniques: CNN, ReLU, MaxPooling, Dropout, Softmax

Batch Size: 200

Learning Rate: 0.001

Epochs: 50

3. 모델 구조 (Convolutional Neural Network)
Convolution Layers

1) Conv Block 1

Conv2D(in=1, out=32, kernel=3, padding=1)

ReLU

MaxPool(2, 2)

Output: B × 32 × 14 × 14

2) Conv Block 2

Conv2D(in=32, out=64, kernel=3, padding=1)

ReLU

MaxPool(2, 2)

Output: B × 64 × 7 × 7

Fully Connected Layers

Flatten(64 × 7 × 7)

Linear

ReLU

Linear

Softmax

4. 데이터셋

Fashion-MNIST 이미지 데이터셋 정보:

Train: 60,000 images

Test: 10,000 images

이미지 크기: 28 × 28 (흑백)

총 10개 클래스

Label	Class
0	T-shirt/Top
1	Trouser
2	Pullover
3	Dress
4	Coat
5	Sandal
6	Shirt
7	Sneaker
8	Bag
9	Ankle Boot
5. 학습 결과

최종 Test Accuracy: 94.96%

예측 예시

임의의 테스트 이미지를 모델에 입력했을 때

모델 출력: 2

라벨 2 = Pullover(스웨터)

실제 이미지도 스웨터 → 정상 분류

다른 테스트 샘플에서도 안정적으로 높은 정확도 확인.

6. 결론

Fashion-MNIST 데이터셋 기반 CNN 분류 모델을 성공적으로 구현

95% 수준의 높은 정확도 달성

데이터 로딩 → 모델 설계 → 학습 → 평가까지 전체 머신러닝 파이프라인 구축 경험 확보
