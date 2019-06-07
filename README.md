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








