### EX NO : 08
### DATE  :16.05.2022
# <p align="center"> XOR GATE IMPLEMENTATION </p>
## Aim:
   To implement multi layer artificial neural network using back propagation algorithm.
   

<br>

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## Related Theory Concept:
The XOR gate stands for the Exclusive-OR gate. This gate is a special type of gate used in different types of computational circuits. Apart from the AND, OR, NOT, NAND, and NOR gate, there are two special gates, i.e., Ex-OR and Ex-NOR.
This neural network will deal with the XOR logic problem. An XOR (exclusive OR gate) is a digital logic gate that gives a true output only when both its inputs differ from each other.


<br>

## Algorithm:
1.Import the required libraries.<br>
2.Create the training dataset.<br>
3.Create the neural network model with one hidden layer.<br>
4.Train the model with training data.<br>
5.Now test the model with testing data.<br>


## Program:
```
/*
Program to implement XOR Logic Gate.
Developed by   : SARAN M
RegisterNumber : 212220230044
*/
```
```python
import numpy as np
from keras.models import Sequential
from keras.layers.core import Dense

training_data=np.array([[0,0],[0,1],[1,0],[1,1]],"float32")
target_data=np.array([[0],[1],[1],[0]],"float32")

model=Sequential()
model.add(Dense(16,input_dim=2,activation='relu'))
model.add(Dense(1,activation='sigmoid'))
model.compile(loss='mean_squared_error',
                    optimizer='adam',
                    metrics=['binary_accuracy'])
model.fit(training_data,target_data,epochs=1000)
scores=model.evaluate(training_data,target_data)

print("\n%s: %.2f%%" % (model.metrics_names[1],scores[1]*100))
print(model.predict(training_data).round())
```

## Output:

![image](https://user-images.githubusercontent.com/75235427/171100816-0900e8a0-d0ab-4d08-95b6-a91f74fdfc38.png)

![image](https://user-images.githubusercontent.com/75235427/171100834-9ced5e14-4d30-40cb-836b-c9afc7277571.png)



## Result:
Thus the python program successully implemented XOR logic gate.
