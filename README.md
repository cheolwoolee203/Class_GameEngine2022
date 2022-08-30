# Class_GameEngine2022

2022년 1학기 GameEngine 수업을 따라한다면 누구나 IK를 구현할수있습니다

https://lcwoo0707.tistory.com/category/

## 1. IK2D

![image2](https://user-images.githubusercontent.com/71004742/187351271-7c2711b0-97a2-45a2-8877-9090d26f16ef.gif)

IK를 간단한 2D평면만을 고려하여 만든 예제입니다.

Target actor에 아무 target을 넣어줘야 동작합니다 실행할때 나오는 default pawn과 헷갈려서
pawn을 움직이셔도 target이 아니라면 움직이지 않습니다.

loss는 L2 loss를, optimizer는 Gradient descent를 이용해 구현했습니다

## 2. IK3DGD

![IK3D](https://user-images.githubusercontent.com/71004742/187354140-33ed8efe-8fed-4a0b-8a2e-7bf5b0a75520.gif)

가장 간단하게 3D에서 구현한 IK입니다

1에서 구현한 3D버전입니다. 위와는 다른점은 3차원이 되었기 때문에 Jacobian을 이용하여 gradent를 구합니다.

loss는 L2 loss를, optimizer는 Jacobain을 이용한 Gradient descent를 이용하여 구현했습니다

## 3. IK3DNewton

![image40](https://user-images.githubusercontent.com/71004742/187354831-48239484-dd49-4675-95ae-597967909430.gif)

IK를 Gauss-Newton method와 Levenberg-Marquardt Method를 이용하여 구현했습니다.

Gauss-Newton을 사용하기 위해 Jacobian의 psudo-inverse를 구현하였습니다.

loss는 residual error를, optimizer는 Leverberg-Marquardt method를 사용하였습니다.

## 4. IK3DFABRIK

![image30](https://user-images.githubusercontent.com/71004742/187361700-3af23a68-aa1e-4c84-abb9-bce724ca3689.png)

FABRIK을 이용하여 IK를 구현하였습니다

적은 처리능력으로 빠르게 IK를 계산할 수 있다보니 많은 곳에서 사용하는 방법입니다.

Regression 방법이 아니기에 사용한 loss와 optimizer가 없습니다.
