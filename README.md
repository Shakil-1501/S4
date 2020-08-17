# Session : 11                  

# Basic Architecture

## Objective : Image classification using Mnist dataset

-  99.4% validation accuracy
-  Less than 20k Parameters
-  You can use anything from above you want. 
-  Less than 20 Epochs
-  No fully connected layer

## Steps

- importing all the necessary packages and modules

- Creation of model using Batch Normalization and Dropout

- Summary of model

```
Requirement already satisfied: torchsummary in /usr/local/lib/python3.6/dist-packages (1.5.1)
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1            [-1, 8, 26, 26]              80
            Conv2d-2            [-1, 8, 24, 24]             584
       BatchNorm2d-3            [-1, 8, 24, 24]              16
         MaxPool2d-4            [-1, 8, 12, 12]               0
            Conv2d-5           [-1, 16, 10, 10]           1,168
            Conv2d-6           [-1, 16, 10, 10]             272
       BatchNorm2d-7           [-1, 16, 10, 10]              32
         MaxPool2d-8             [-1, 16, 5, 5]               0
         Dropout2d-9             [-1, 16, 5, 5]               0
           Conv2d-10             [-1, 64, 3, 3]           9,280
           Conv2d-11             [-1, 32, 3, 3]           2,080
           Conv2d-12             [-1, 10, 1, 1]           2,890
================================================================
Total params: 16,402
Trainable params: 16,402
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.17
Params size (MB): 0.06
Estimated Total Size (MB): 0.24

```
- Loading of MNIST Train and test dataset
- Training of model on MNIST datset
- Testing of model 
  - Optimizer : SGD
  - Batch Size : 30
  - Epoch : 18
  - Learning Rate : 0.01
  - Momentum : 0.9
  
  ## Results
  
  - Achieved Highest test accuracy of  99.36
  - Model was not Overfitting
  
