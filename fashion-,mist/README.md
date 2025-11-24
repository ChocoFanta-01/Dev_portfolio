Fashion-MNIST CNN Classification

PyTorch 기반 CNN 모델로 의류 이미지(10 class)를 분류하는 프로젝트입니다.
총 94.96% 정확도를 달성했으며, 데이터를 처리하고 CNN 구조를 설계하는 과정 전반을 직접 구현했습니다.

1. 프로젝트 개요

Fashion-MNIST 데이터셋을 활용하여

CNN 기반 이미지 분류 모델을 직접 설계하고

90% 이상 정확도를 목표로 학습하며

모델 구조 설계 및 튜닝 과정을 수행한 프로젝트입니다.

최종적으로 94.96%의 테스트 정확도를 달성했습니다.

2. 사용 기술

Language: Python

Framework: PyTorch

Dataset: Fashion-MNIST

Training Env: Google Colab

ML Techniques: CNN, ReLU, MaxPooling, Dropout, Softmax

Batch Size: 200

Learning Rate: 0.001

Epochs: 50

3. 모델 구조
Convolution Layers

1) Conv Block 1

Conv2D (in=1, out=32, kernel=3, padding=1)

ReLU

MaxPool(2,2)

Output: B × 32 × 14 × 14

2) Conv Block 2

Conv2D (in=32, out=64, kernel=3, padding=1)

ReLU

MaxPool(2,2)

Output: B × 64 × 7 × 7

Fully Connected Layers

Flatten(64×7×7)

Linear

ReLU

Linear

Softmax

4. 데이터셋

Fashion-MNIST:

Train: 60,000 images

Test: 10,000 images

Gray-scale 28×28

라벨 10종류

0: T-shirt/Top

1: Trouser

2: Pullover

3: Dress

4: Coat

5: Sandal

6: Shirt

7: Sneaker

8: Bag

9: Ankle Boot

5. 학습 결과

최종 Test Accuracy: 94.96%

예측 예시

임의의 테스트 이미지를 입력했을 때 모델 출력이 2였고, 라벨표에서 2는 Pullover(스웨터).
실제 이미지도 스웨터로 확인되어 정상적으로 분류됨.
여러 샘플에 대해 일관된 정확도 확인.

6. 결론

CNN 기반 의류 이미지 분류 모델을 설계 및 구현

95% 수준의 분류 성능 달성

데이터 로딩, 모델 설계, 학습 및 평가 전 과정을 직접 수행

신입 개발자로서 기본적인 머신러닝 워크플로우 이해와 구현 역량 확보
