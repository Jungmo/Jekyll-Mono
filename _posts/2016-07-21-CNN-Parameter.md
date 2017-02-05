---
layout: post
title: CNN Parameter
data: 2016-07-21
categories: python
---
## Convolution Layer

![alt text](https://github.com/Jungmo/jungmo.github.com/blob/master/_posts/img/cnn_para.png?raw=true "CNN parameter")

* W는 이미지 배열의 width

* H는 이미지 배열의 height

* D는 이미지 배열의 dimension(RGB면 3, Grayscale이면 1)

* K는 필터의 수 - 몇 겹으로 할건지

* F는 필터의 크기. 3\*3, 5\*5 ..

* S는 stride - 몇 칸씩 건너뛸건지

* P는 모서리를 0으로 채우는 걸 몇 겹으로 할 건지

```
K는 대개 2의 제곱을 사용하고, 

F = 3, S = 1, P = 1
F = 5, S = 1, P = 2
F = 5, S = 2, P = ?(whatever fits)
F = 1, S = 1, P = 0

이렇게 많이 쓰인다.
```
두 번째 레이어의 크기를 구하는 공식은 다음과 같다.

Wn = (Wn-1 - F + 2P)/S + 1

Hn = (Hn-1 - F + 2P)/S + 1

Dn = K

**Tensorflow에서 padding='SAME'을 해주면, 알아서 패딩을 정해준다. 이것은 패딩을 적용하고 난 다음의 결과의 레이어 크기와 그 전의 레이어 크기를 동일하게 한다는 것이다.**

## Pooling Layer

![alt text](https://github.com/Jungmo/jungmo.github.com/blob/master/_posts/img/max_pool.png?raw=true "Max pooling example")

![alt text](https://github.com/Jungmo/jungmo.github.com/blob/master/_posts/img/pool_para.png?raw=true "Pooling parameter")

Convolution Layer에서 다음 Conv Layer로 갈 때, 샘플을 뽑는다는 느낌.

다루기 좋고 작게 만드는것..

Max Pooling을 쓴다.

W1 H1 D1은 convolution Layer

W2 H2 D2는 Pooling Layer

F는 Pooling slice 크기 (예제에선 2)
S는 Stride

* W2 = (W1-F)/S + 1
* H2 = (H1-F)/S + 1
* D2 = D1

