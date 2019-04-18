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


Added denoiser to cifar100

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
