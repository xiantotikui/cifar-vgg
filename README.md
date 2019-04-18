# cifar-vgg
This is a Keras model based on VGG16 architecture for CIFAR-10 and CIFAR-100. it can be used either with pretrained weights file or trained from scratch.

This package contains 2 classes one for each datasets, the architecture is based on the VGG-16 [1] with adaptation to CIFAR datasets based on [2]. By running the py files you can get a sample of a trining and estimation of validation error.

The CIFAR-10 reaches a validation accuracy of 93.56%
CIFAR-100 reaches validation accuracy of 70.48%.
On instantiation the model can either be trained or loaded from previous saved weight file.

[cifar-100 weights](https://drive.google.com/open?id=0B4odNGNGJ56qTEdnT1RjTU44Zms)
[cifar-10 weights](https://drive.google.com/open?id=0B4odNGNGJ56qVW9JdkthbzBsX28)


References:

[1] Karen Simonyan and Andrew Zisserman. Very deep convolutional networks for large-scale image recognition. arXiv preprint arXiv:1409.1556, 2014.

[2] Shuying Liu and Weihong Deng. Very deep convolutional neural network based image classifi- cation using small training sample size. In Pattern Recognition (ACPR), 2015 3rd IAPR Asian Conference on, pages 730–734. IEEE, 2015.


VGG16e

`model.add(Lambda(lambda x: K.switch(K.less(x, K.constant(0.1)), x * 0.0, x)))`

```
Epoch 10/250
390/390 [==============================] - 248s 636ms/step - loss: 3.9793 - acc: 0.1266 - val_loss: 4.1855 - val_acc: 0.1124
Epoch 11/250
390/390 [==============================] - 248s 636ms/step - loss: 3.8986 - acc: 0.1450 - val_loss: 3.9052 - val_acc: 0.1544
Epoch 12/250
390/390 [==============================] - 248s 636ms/step - loss: 3.8370 - acc: 0.1640 - val_loss: 3.9623 - val_acc: 0.1631
Epoch 13/250
390/390 [==============================] - 248s 636ms/step - loss: 3.7987 - acc: 0.1831 - val_loss: 3.6244 - val_acc: 0.2155
Epoch 14/250
390/390 [==============================] - 248s 636ms/step - loss: 3.7634 - acc: 0.1994 - val_loss: 3.7997 - val_acc: 0.2169
Epoch 15/250
390/390 [==============================] - 248s 636ms/step - loss: 3.7442 - acc: 0.2162 - val_loss: 3.7472 - val_acc: 0.2285
Epoch 16/250
390/390 [==============================] - 248s 637ms/step - loss: 3.7245 - acc: 0.2321 - val_loss: 3.6718 - val_acc: 0.2545
Epoch 17/250
390/390 [==============================] - 248s 637ms/step - loss: 3.7151 - acc: 0.2442 - val_loss: 3.7044 - val_acc: 0.2504
Epoch 18/250
390/390 [==============================] - 248s 637ms/step - loss: 3.7144 - acc: 0.2536 - val_loss: 3.6002 - val_acc: 0.2688
Epoch 19/250
390/390 [==============================] - 248s 637ms/step - loss: 3.7160 - acc: 0.2648 - val_loss: 3.7225 - val_acc: 0.2723
Epoch 20/250
390/390 [==============================] - 249s 639ms/step - loss: 3.7089 - acc: 0.2705 - val_loss: 3.6805 - val_acc: 0.2957
```

```
Epoch 50/250
390/390 [==============================] - 262s 672ms/step - loss: 2.7999 - acc: 0.4983 - val_loss: 2.9226 - val_acc: 0.4891
Epoch 51/250
390/390 [==============================] - 257s 659ms/step - loss: 2.8112 - acc: 0.4985 - val_loss: 2.9996 - val_acc: 0.4776
Epoch 52/250
390/390 [==============================] - 247s 634ms/step - loss: 2.8106 - acc: 0.5007 - val_loss: 2.8499 - val_acc: 0.5057
Epoch 53/250
390/390 [==============================] - 247s 634ms/step - loss: 2.8036 - acc: 0.5043 - val_loss: 2.6911 - val_acc: 0.5268
Epoch 54/250
390/390 [==============================] - 248s 635ms/step - loss: 2.8021 - acc: 0.5073 - val_loss: 3.3209 - val_acc: 0.4315
Epoch 55/250
390/390 [==============================] - 248s 636ms/step - loss: 2.7996 - acc: 0.5111 - val_loss: 2.7062 - val_acc: 0.5396
Epoch 56/250
390/390 [==============================] - 248s 635ms/step - loss: 2.8056 - acc: 0.5098 - val_loss: 3.0701 - val_acc: 0.4697
Epoch 57/250
390/390 [==============================] - 263s 673ms/step - loss: 2.8117 - acc: 0.5104 - val_loss: 2.9177 - val_acc: 0.5047
Epoch 58/250
390/390 [==============================] - 251s 642ms/step - loss: 2.8068 - acc: 0.5108 - val_loss: 2.6759 - val_acc: 0.5467
Epoch 59/250
390/390 [==============================] - 250s 642ms/step - loss: 2.8081 - acc: 0.5162 - val_loss: 2.9655 - val_acc: 0.4925
Epoch 60/250
390/390 [==============================] - 248s 637ms/step - loss: 2.8142 - acc: 0.5151 - val_loss: 2.7468 - val_acc: 0.5314
Epoch 61/250
390/390 [==============================] - 248s 636ms/step - loss: 2.6278 - acc: 0.5545 - val_loss: 2.5488 - val_acc: 0.5727
Epoch 62/250
390/390 [==============================] - 248s 636ms/step - loss: 2.5070 - acc: 0.5750 - val_loss: 2.6045 - val_acc: 0.5616
Epoch 63/250
390/390 [==============================] - 248s 636ms/step - loss: 2.4701 - acc: 0.5750 - val_loss: 2.7277 - val_acc: 0.5474
Epoch 64/250
390/390 [==============================] - 248s 636ms/step - loss: 2.4355 - acc: 0.5810 - val_loss: 2.4629 - val_acc: 0.5719
Epoch 65/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3977 - acc: 0.5834 - val_loss: 2.4274 - val_acc: 0.5812
Epoch 66/250
390/390 [==============================] - 248s 636ms/step - loss: 2.3922 - acc: 0.5816 - val_loss: 2.5962 - val_acc: 0.5551
Epoch 67/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3763 - acc: 0.5841 - val_loss: 2.4075 - val_acc: 0.5812
Epoch 68/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3779 - acc: 0.5813 - val_loss: 2.4861 - val_acc: 0.5684
Epoch 69/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3579 - acc: 0.5872 - val_loss: 2.5598 - val_acc: 0.5539
Epoch 70/250
390/390 [==============================] - 248s 636ms/step - loss: 2.3634 - acc: 0.5835 - val_loss: 2.3557 - val_acc: 0.5935
Epoch 71/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3504 - acc: 0.5873 - val_loss: 2.4086 - val_acc: 0.5896
Epoch 72/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3427 - acc: 0.5892 - val_loss: 2.3798 - val_acc: 0.5871
Epoch 73/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3477 - acc: 0.5865 - val_loss: 2.3875 - val_acc: 0.5859
Epoch 74/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3474 - acc: 0.5888 - val_loss: 2.7676 - val_acc: 0.5462
Epoch 75/250
390/390 [==============================] - 248s 636ms/step - loss: 2.3412 - acc: 0.5918 - val_loss: 2.6444 - val_acc: 0.5418
Epoch 76/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3338 - acc: 0.5948 - val_loss: 2.5049 - val_acc: 0.5661
Epoch 77/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3449 - acc: 0.5923 - val_loss: 2.4329 - val_acc: 0.5832
Epoch 78/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3463 - acc: 0.5931 - val_loss: 2.3671 - val_acc: 0.5960
Epoch 79/250
390/390 [==============================] - 248s 635ms/step - loss: 2.3380 - acc: 0.5969 - val_loss: 2.4626 - val_acc: 0.5824
Epoch 80/250
390/390 [==============================] - 248s 636ms/step - loss: 2.3378 - acc: 0.5985 - val_loss: 2.3751 - val_acc: 0.5972
Epoch 81/250
390/390 [==============================] - 248s 635ms/step - loss: 2.2058 - acc: 0.6275 - val_loss: 2.2899 - val_acc: 0.6222
Epoch 82/250
390/390 [==============================] - 248s 635ms/step - loss: 2.1208 - acc: 0.6443 - val_loss: 2.2562 - val_acc: 0.6228
Epoch 83/250
390/390 [==============================] - 249s 639ms/step - loss: 2.0801 - acc: 0.6480 - val_loss: 2.2276 - val_acc: 0.6254
```
