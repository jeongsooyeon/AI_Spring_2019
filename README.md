# AI_Spring_2019

인공지능개론 2019 봄학기

* __03_hello_dataset1_MNIST.ipynb__ 

![image](https://user-images.githubusercontent.com/45751310/59102917-6bd16580-8968-11e9-8c30-86925524ca5a.png)

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



