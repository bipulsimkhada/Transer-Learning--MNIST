# Transer-Learning--MNIST
Transfer Learning on MNIST dataset

## Description
To illustrate the power and concept of transfer learning, we will train a CNN on just the digits 5,6,7,8,9. Then we will train just the last layer(s) of the network on the digits 0,1,2,3,4 and see how well the features learned on 5-9 help with classifying 0-4.

## Libraries 
* Keras
* numpy
* pandas
* matplotlib

## Tool
* Google Colab

## Network parameters

```python
batch_size = 128
num_classes = 5
epochs = 5
img_rows, img_cols = 28, 28
filters = 32
pool_size = 2
kernel_size = 3
```

## Model Arhitecture for digits 5-9
```python
# model is a 3-layer MLP with ReLU and dropout after each layer
model = Sequential()
model.add(Dense(hidden_units,activation="relu",input_dim=input_size))
model.add(Dropout(dropout))
model.add(Dense(hidden_units,activation="relu"))
model.add(Dropout(dropout))
model.add(Dense(num_labels))
model.add(Activation('softmax'))
```

## Model Compile
```python
model.compile(loss='categorical_crossentropy',
              optimizer='adam',
              metrics=['accuracy'])
```

## Training the model
```python
model.fit(x_train,y_train,epochs=20, batch_size = batch_size)
```
