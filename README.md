# Tensorflow_Basic
The basic program to understand the Tensorflow

This program show how the neural network works

Normal programming=> Data+Rule->Result

Machine Learning Programming=> Data+Result->Result



the code is explained as follows:


import tensorflow as tf
import numpy as np
from tensorflow import keras
---------------import statements--------------


model = tf.keras.Sequential([keras.layers.Dense(units=1, input_shape=[1])])
---------------neural network structure with one node and one layer and one input----------------


model.compile(optimizer='sgd',loss='mean_squared_error')
--------------------------------using gradient descent for optimization and mean square method for loss calculation--------------


xs = np.array([1.0,2.0,3.0,4.0,5.0,6.0])
ys = np.array([2.0,3.0,4.0,5.0,6.0,7.0])
--------------------------giving input x and ouput y in form of y=x+1-------------------------------


model.fit(xs,ys,epochs=5000)
--------------fitting data and result into model with 500 iterations of training---------

print(model.predict([7.0]))
--------------predicting output for new value-----------------------
