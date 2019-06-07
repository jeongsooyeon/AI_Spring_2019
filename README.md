# AI_Spring_2019

인공지능개론 2019 봄학기

* __03_hello_dataset1_MNIST.ipynb__ 

<div>

![image](https://user-images.githubusercontent.com/45751310/59107033-be178400-8972-11e9-96b7-c186c1e58c5e.png)

![image](https://user-images.githubusercontent.com/45751310/59107127-e606e780-8972-11e9-87ee-c0cd770ba75b.png)

</div>

pixels = img1.reshape((28, 28)) # shape을 바꾼다. # 28*28 = 784, 각각의 글자는 28*28이다. 정보가 784개고 28개로 쪼갠다.

plt.imshow(pixels, cmap='gray') #plt에게 흑백으로 그리도록 한다.

plt.title('mnist.test.images[{}]'.format(idx)) # 이미지로 저장하게 해준다.

plt.show() # 그림을 그린다.

---

* __04_2_ActivationFunctions.ipynb__

![image](https://user-images.githubusercontent.com/45751310/59103371-9d96fc00-8969-11e9-9e0c-7de704a4a361.png)

plt.title('relu')

![image](https://user-images.githubusercontent.com/45751310/59103449-cfa85e00-8969-11e9-9d87-c78fbfc63a7e.png)

plt.title('sigmoid')

![image](https://user-images.githubusercontent.com/45751310/59103456-dd5de380-8969-11e9-853e-dd84889b65c9.png)

plt.title('step function')

---

* __05_Linear_regression_course.ipynb__

cost = tf.reduce_mean(tf.square(hypothesis - y_train)) 

#가장 기초적인 cost #가설값과 y값의 거리의차이를 제곱을 통해 +, - 구분없이 절대적인 거리를 구하고 그값을 cost에 저장한다.

optimizer = tf.train.GradientDescentOptimizer(learning_rate=0.01)  #optimizer를 통해 에러를 보며 train을 풀어간다. 

train = optimizer.minimize(cost) #cost를 최소화 한다.

---

* __06_1_Perceptron_prediction_gates.ipynb__

Perceptrons - Making Predictions

AND Gate, NAND Gate, OR Gate, XOR Gate

XOR cannot be expressed as a single layer Perceptron. #XOR은 단일 레이어 퍼셉트론으로 표현 될 수 없다.

---

* __06_2_Perceptrons_prediction.ipynb__

![image](https://user-images.githubusercontent.com/45751310/59107525-cde39800-8973-11e9-86eb-209be37f76d3.png)

퍼세트론으로 공간을 나눈다. 점의 밀도를 높일수록 경계값이 명확해진다.

---

* __06_3_Perceptrons_training_AND_v1.ipynb__

![image](https://user-images.githubusercontent.com/45751310/59107842-77c32480-8974-11e9-9c9d-b373f60da811.png)

partial derivative with respect to m #웨이트로 미분한다. 바이어스로 미분 할 때와는 다르게 x를 곱한다.

![image](https://user-images.githubusercontent.com/45751310/59107876-8c9fb800-8974-11e9-9ae4-dca570fa8e8b.png)

partial derivative with respect to b #바이어스로 미분한다.

---

* __07_0_TF_reduce_mean.ipynb__

import numpy as np #수학을 다루기 쉽게 해준다. #보통 이걸로 평균내는데, 굳이 텐서플로우에서 평균내는거 또 만들었다.

import tensorflow as tf #텐서플로우로 평균내는 것

m2 = tf.reduce_mean(c, axis = 1) #reduce_mean은 평균을 구하는것

---

* __07_1_TF_AND_simplest.ipynb__

AND학습하기 아까 같은 문제를 텐서플로우로 풀어보기

---

* __07_2_TF_XOR.ipynb__

![image](https://user-images.githubusercontent.com/45751310/59109865-d12d5280-8978-11e9-8816-3031e603e411.png)

코스트도 feed를 해주고 천번마다 출력한다. 결과보면, 코스트가 점점 줄어든다.

---

* __07_3_TF_MNIST_hello_keras_ipynb.ipynb__

![image](https://user-images.githubusercontent.com/45751310/59110412-0a19f700-897a-11e9-926e-84974ccfc489.png)

(784 * 512) + 512 = 401920

(512 * 10) + 10 = 5130

((784 * 512) + 512) + ((512 * 10) + 10) = 407050

Test accuracy, Training accuracy

---

* __07_4_Keras_MNIST_CNN_keras.ipynb__

![image](https://user-images.githubusercontent.com/45751310/59110614-7563c900-897a-11e9-9a10-ce1a423dc0e0.png)

MLNN의 문제를 해결하고자 만들어진 것이 합성곱 계층(CNN)이다. 

MNIST 데이터 같은 이미지 데이터는 일반적으로 채널, 세로, 가로 이렇게 3차원으로 구성된 데이터이다. 

합성곱에서는 3차원 데이터를 입력하고 3차원의 데이터로 출력하므로 형상을 유지할 수 있다

---

* __Neural_network.ipynb__

![image](https://user-images.githubusercontent.com/45751310/59110791-c96ead80-897a-11e9-97be-225041cfc95d.png)

뉴럴 네트워크

draw_neural_net(ax, .1, .9, .1, .9, [6, 7, 3]) #뉴런의 수를 늘릴 수 있다.
