
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

## Model Arhitecture
|<img src="https://github.com/bipulsimkhada/Image/blob/main/modelsummary.png">|

