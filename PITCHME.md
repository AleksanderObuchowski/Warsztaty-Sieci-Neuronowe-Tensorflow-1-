+++?color=gray


# Sieci Neuronowe i Tensorflow 1: Prosta sieć neuronowa


**Aleksander Obuchowski**

---?color=gray

# Import Biblioteki
``` Python
import tensorflow as tf
```
---?color=gray
# Prosty graf
``` Python
x1 = tf.constant(5)
x2 = tf.constant(6)

result = tf.multiply(x1,x2)


with tf.Session() as sess:
    output = sess.run(result)
    print(output)

```
@[1-2](Definiowanie stałych) 
@[4](Węzeł obliczniowy) 
@[7-9](Wywołanie sesji)

---?color=gray
@color[white](#Import danych)
``` Python
from tensorflow.contrib.learn.python.learn.datasets.mnist import read_data_sets

mnist = read_data_sets("/tmp/data",one_hot = True)
```
---?color=gray
@color[white](#Wyświetlanie obrazka)

```Python
import matplotlib.pyplot as plt

img= mnist.test.images[3].reshape((28,28))
plt.imshow(img,cmap="Greys")

plt.show()
'''
@[1](Import Biblioteki)
@[3](Przekształcenie elementu ze zbioru na macierz o wymiarach 28x28
@[4](Przedstawienie macierzy jako mape szarości)
@[6](Wyświetlenie obrazka)
