# Sieci Neuronowe i Tensorflow 1: Prosta sieć neuronowa
**Aleksander Obuchowski**

---

# Import Biblioteki
``` Python
import tensorflow as tf
```
---
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

---
