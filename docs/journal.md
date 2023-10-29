# 텐서플로 / 파이토치

## 텐서플로

### 란?

- 구글에서 만들어진 딥러닝 프레임워크
- 데이터 플로우 그래프 구조를 사용
- 주로 이미지나 반복 신경망 구성, 기계 번역, 필기 숫자 판별 등을 위한 각종 신경망 학습에 사용
  -Python, C++, Go, Java, R 지원

### 장점

- 특히 대규모 예츨 모델 구성에 뛰어나 사실상 거의 모든 딥러닝 프로젝트에 범용적으로 사용할 수 있다.
- 구글에서 지원하고 있기 때문에 성능 개선과 지원에서 타 프레임워크들보다 바르고 안정적이다.
- 텐서보드(TensorBoard)를 통해서 파라미터 변화 양상이나 DNN의 구조를 알 수 있다.

### 단점

- 메모리를 효율적으로 사용하지 못 하고 있다.
- 딥러닝 모델을 만드는 데에 있어 기초 레벨부터 직접 작업해야 하기 때문에 초보자에겐 어려울 수 있다.
- 유기적으로 신경망을 만들 수 없다.

## 케라스

- 빠른 실험을 가능하게 하도록 만들어졌다.

### 란?

- 구글에서 프로젝트 연구적 노력의 목적으로 개발된 프레임워크
- 텐서플로의 문제를 해결하기 위해 보다 단순한 인터페이스를 제공
- 케라스에서 제공하는 시퀀스 모델로 원하는 레이어를 순차적으로 쌓을 수 있으며, 다중 출력 등 더 복잡한 모델일 구성할 때는 케라스 함수 API를 사용하여 쉽게 구성할 수 있다.
- 딥러닝 초급자도 각자 분야에서 손쉽게 딥러닝 모델을 개발하고 활용할 수 있도록 직관적인 API를 제공한다.
- 텐서플로에서도 쓸 수 있다

### 장점

- 일반 사용 사례에 최적화된 간단하고 일관된 인터페이스를 제공한다.
- 사용자 오류에 대해 명확하고 실용적인 피드백을 제공
- 케라스의 구성 요소는 모듈 형태로, 각 모듈이 독립성을 갖기 때문에 새로운 모델을 만들 때 각 모듈을 조합해 쉽게 새로운 모델을 만들 수 있다.

### 단점

- 모듈화의 한계로 복잡한 프로젝트에 구현 범위가 다소 좁다
- 다양한 백엔드 위에서 동작하기 때문에 어떤 오류가 발생했을 때 케라스 자체의 문제인지, 백엔드의 문제인지 특정하기 어렵다
- 문서화가 제대로 되어 있지 않고 이용자의 수가 적어 참고할 곳이 부족하다.

## 파이토치

### 란?

- 토치라는 머신러닝 라이브러리를 바탕으로 만들어 진
- 페이스북의 AI 연구 팀이 개발한 파이썬 기반 오픈소스 머신러닝 라이브러리

### 장점

- 코드를 깔끔하고 직관적으로 작성할 수 있다.
- 난이도가 낮아 학습 속도가 빠르다.
- 메모리에서 연산을 하면서도 신경망 사이즈를 최적으로 바꾸면서 동작시킬 수 있어 속도 대비 빠른 최적화가 가능하다.

### 단점

- 사용자층이 얕다
- 학습에 필요한 자료와 예제를 구하기 어렵다.

## 비교

### 텐플

- 거의 모든 딥러닝 프로젝트에서 활용도가 높은 만능 프레임워크
- 딥러닝 모델을 구축하는 단계에서 기초 레벨부터 직접 만들어 나가야 하므로 초보자에게는 추천하지 않는

### 케라스

- 배우기 쉽고 모델을 구축하기 쉽다
- 오류가 발생했을 시 케라스 자체의 문제인지, 백엔드의 문제인지 알 수 없다.

### 파토

- 텐플보다 비교적 절차가 간단하고 그래프가 동적으로 변화할 수 있으며 코드 자체도 파이썬과 유사해 진입 장벽이 낮다.
- 하지만 딥러닝에 대한 이해도가 부족하거나 코딩 지식이 없으면 파이토치 또한 난이도가 높다
- 비교적 디테일한 모델링이 불가능하다.

## 정리

- 딥러닝 입문자는 케라스 -> 파이토치 -> 텐서플로 순으로 공부하면 좋다.